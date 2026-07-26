---
name: zoom-phone-call-history-migration
description: >-
  Move a Zoom Phone call-record pipeline off the legacy Call Logs API and webhooks onto Call
  History and Call Elements before the April 2026 (API) and May 2026 (webhook) sunsets, and
  keep call analytics correlated on call_id / call_history_uuid / call_element_id.
api: openapi/zoom-phone-api-openapi.json
generated: '2026-07-25'
method: generated
source: >-
  derived from openapi/zoom-phone-api-openapi.json and
  openapi/zoom-phone-webhooks-openapi.json (every operationId and event name verified in the
  specs), https://developers.zoom.us/docs/phone/migrate/,
  https://developers.zoom.us/docs/phone/webhook-migrate/, lifecycle/zoom-phone-lifecycle.yml
operations:
  - accountCallHistory
  - getCallPath
  - getCallElement
  - phoneUserCallHistory
  - syncUserCallHistory
  - deleteUserCallHistory
  - addClientCodeToCallHistory
  - accountCallLogs
  - getCallLogDetails
  - phoneUserCallLogs
  - syncUserCallLogs
---

# Migrate Zoom Phone call records to Call History and Call Elements

Zoom has run this resource family through three generations in place. v1 Call Logs sunsets in
**April 2026**, the v1 call-log webhooks in **May 2026**, and the transitional `call_log` /
`call_path` response arrays in **November 2026**. This is the single highest-risk change on the
Zoom Phone surface.

## Version map

| Generation | Account records | Single record | Segment detail |
|---|---|---|---|
| v1 (deprecated, sunset 2026-04) | `accountCallLogs` `GET /phone/call_logs` | `getCallLogDetails` `GET /phone/call_logs/{callLogId}` | — |
| v2 (2023) | `accountCallHistory` `GET /phone/call_history` | `getCallPath` `GET /phone/call_history/{callHistoryUuid}` | `getCallHistoryDetail` (deprecated) |
| v3 (2025) | `accountCallHistory` | `getCallPath` returning `call_elements[]` | `getCallElement` `GET /phone/call_element/{callElementId}` |

Per-user equivalents follow the same split: `phoneUserCallLogs` / `syncUserCallLogs` /
`deleteCallLog` (all deprecated) become `phoneUserCallHistory` — `GET /phone/users/{userId}/call_history`,
`syncUserCallHistory` — `GET /phone/users/{userId}/call_history/sync`, and
`deleteUserCallHistory` — `DELETE /phone/users/{userId}/call_history/{callLogId}`.
Client-code tagging moves from `addClientCodeToCallLog` (`PUT .../call_logs/{callLogId}/client_code`)
to `addClientCodeToCallHistory` (`PATCH .../call_history/{callLogId}/client_code`).

## Field map

- `call_log[]` → `call_history[]`, and the record key `id` → `call_history_uuid`.
- `call_path[]` → `call_elements[]`, each entry keyed by `call_element_id`.
- `call_id` is unchanged and is the correlation key that also appears on the real-time
  `phone.*` webhook events — persist it first, everything else hangs off it.

## Webhook map

| Legacy (sunset 2026-05) | v2 | v3 |
|---|---|---|
| `phone.call_log_deleted` | `phone.call_history_deleted` | `phone.call_element_deleted` |
| `phone.callee_call_log_completed` | `phone.callee_call_history_completed` | `phone.callee_call_element_completed` |
| `phone.caller_call_log_completed` | `phone.caller_call_history_completed` | `phone.caller_call_element_completed` |
| `phone.call_log_permanently_deleted` | — | — |

`call_element_id` was also added to `phone.voicemail_received`,
`phone.voicemail_received_for_access_member`, `phone.voicemail_transcript_completed`,
`phone.recording_completed` and `phone.recording_completed_for_access_member`.

## Steps

1. **Inventory.** Grep the integration for `/phone/call_logs` and for the four legacy event names.
2. **Persist three identifiers**, not one: `call_id` (real-time), `call_history_uuid` (post-call
   record), `call_element_id` (per-leg). Analytics that keyed only on the old `id` will not join.
3. **Switch reads.** Replace `accountCallLogs` with `accountCallHistory`
   (`GET /phone/call_history`) and `getCallLogDetails` with `getCallPath`
   (`GET /phone/call_history/{callHistoryUuid}`). Pull segment detail with `getCallElement`.
   Both paths honour `page_size` + `next_page_token` cursor pagination and `from`/`to` date
   filtering; the call-history endpoints are HEAVY-labelled, so budget against the
   `5/second, 15,000/day` (Pro) or `10/second, 30,000/day` (Business+) Zoom Phone quota.
4. **Write a field-mapping adapter** rather than renaming fields in place, so both payload
   shapes can be consumed while the v2 arrays are still returned (they survive until Nov 2026).
5. **Resubscribe webhooks** to the `call_element` events in the Marketplace app, validate
   `x-zm-signature` (HMAC-SHA256 over `v0:{x-zm-request-timestamp}:{raw body}`), and
   **deduplicate on your side** — Zoom retries deliveries and sends no idempotency key.
6. **Backfill.** Use `syncUserCallHistory` to reconcile a window rather than replaying paginated
   reads, which will hit the daily cap on a large account.

## Watch for

- `getCallHistoryDetail` (`GET /phone/call_history_detail/{callHistoryId}`) is itself deprecated —
  do not land on it as the migration target; go to `getCallElement`.
- A `404` with code `404` on a call-history read frequently means the record aged out of the
  retention window, not that the id is wrong.
- Recordings and voicemails are fetched through a dynamically generated `download_url`; send the
  OAuth access token (or `download_access_token`) as a Bearer token and follow redirects.
