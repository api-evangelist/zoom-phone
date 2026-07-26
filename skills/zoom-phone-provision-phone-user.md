---
name: zoom-phone-provision-phone-user
description: >-
  Provision a Zoom Phone user end to end — confirm the license, set the site and extension,
  assign a calling plan, assign a phone number, set the emergency address, and verify call
  handling — using the Zoom Phone API.
api: openapi/zoom-phone-api-openapi.json
generated: '2026-07-25'
method: generated
source: >-
  derived from openapi/zoom-phone-api-openapi.json (every operationId verified in the spec),
  conventions/zoom-phone-conventions.yml, errors/zoom-phone-problem-types.yml,
  rate-limits/zoom-phone-rate-limits.yml
operations:
  - listPhoneUsers
  - phoneUser
  - updateUserProfile
  - assignCallingPlan
  - assignPhoneNumber
  - listAccountPhoneNumbers
  - listEmergencyAddresses
  - addEmergencyAddress
  - getUserCallHandlingSetting
  - updateUserCallHandlingSetting
  - batchAddUsers
---

# Provision a Zoom Phone user

Turn a licensed Zoom user into a working phone extension. Everything below maps to a real
operation in `openapi/zoom-phone-api-openapi.json`.

## Before you start

- Base URL is `https://api.zoom.us/v2`. The version lives in the path; there is no version header.
- Authenticate with OAuth 2.0. A Server-to-Server OAuth app (`account_credentials` grant) is the
  right shape for provisioning; a user-level app cannot administer other users.
- Granular scopes needed: `phone:read:list_users:admin`, `phone:read:user:admin`,
  `phone:update:user:admin`, `phone:write:calling_plan:admin`, `phone:write:phone_number:admin`,
  `phone:read:list_emergency_addresses:admin`, `phone:write:emergency_address:admin`.
  Classic equivalents are `phone:read:admin` and `phone:write:admin`.
- The account needs a Business/Enterprise plan and available Zoom Phone licenses. A `403` on any
  `/phone/**` call usually means Zoom Phone is not set up, not that the token is bad.

## Steps

1. **Find the user.** `listPhoneUsers` — `GET /phone/users`. Page with `page_size` (max 100) and
   `next_page_token`; the token expires after 15 minutes. Filter with `site_id`, `status` or
   `keyword`. Confirm the target user appears with a Zoom Phone license.
2. **Read the current state.** `phoneUser` — `GET /phone/users/{userId}`. `userId` accepts the
   Zoom user id or email address. Record the existing `extension_number`, `site` and
   `calling_plans` before changing anything — these calls are not idempotent and there is no
   retry token, so a blind re-POST can double-assign.
3. **Set profile fields.** `updateUserProfile` — `PATCH /phone/users/{userId}` to set the
   extension number, site, template, or policy-relevant profile values.
4. **Assign a calling plan.** `assignCallingPlan` — `POST /phone/users/{userId}/calling_plans`.
   Use `updateCallingPlan` (`PUT`) to change an existing assignment and `unassignCallingPlan`
   (`DELETE /phone/users/{userId}/calling_plans/{planType}`) to remove one. A missing plan is the
   usual cause of an otherwise healthy extension that cannot dial out.
5. **Find an unassigned number.** `listAccountPhoneNumbers` — `GET /phone/numbers` filtered to
   unassigned. Note: this operation is marked `deprecated: true` in the spec; the Number
   Management API (`openapi/zoom-phone-number-management-openapi.json`, `listPhoneNumbers`) is
   the forward path for inventory work.
6. **Assign the number.** `assignPhoneNumber` — `POST /phone/users/{userId}/phone_numbers`.
   Reverse with `UnassignPhoneNumber` — `DELETE /phone/users/{userId}/phone_numbers/{phoneNumberId}`.
7. **Set the emergency address.** `listEmergencyAddresses` — `GET /phone/emergency_addresses`, and
   `addEmergencyAddress` — `POST /phone/emergency_addresses` when the location is new. E911
   addressing is a legal requirement (Kari's Law / RAY BAUM'S Act) for US extensions, not an
   optional step.
8. **Verify call handling.** `getUserCallHandlingSetting` —
   `GET /phone/users/{userId}/call_handling/settings`, then
   `updateUserCallHandlingSetting` — `PATCH /phone/users/{userId}/call_handling/settings/{hourType}`
   for business hours, closed hours and holiday routing. Do **not** use `getCallHandling` /
   `addCallHandling` / `updateCallHandling` on `/phone/extension/{extensionId}/...`; those three
   are flagged deprecated in the spec.

## Doing it in bulk

`batchAddUsers` — `POST /phone/users/batch` and `updateUsersPropertiesInBatch` —
`PUT /phone/users/batch` exist for onboarding cohorts. Batch operations are capped
(error code `1003` "Too many numbers, should less than 200"; error `429` in the body means a
batch-size violation, not a rate limit).

## Errors and limits

- Errors are `{"code": <int>, "message": "<string>"}` — **not** RFC 9457 problem+json. The numeric
  code is independent of the HTTP status: `124` invalid account/token, `1001` user does not exist,
  `300` invalid user id, `2001` account does not exist.
- HTTP `429` is a real rate limit. Zoom Phone is `20/second` (Pro) or `40/second` (Business+) for
  LIGHT endpoints; most provisioning writes are MEDIUM (`10`/`20` per second). No `Retry-After` or
  `X-RateLimit-*` headers are sent — back off on your own clock.
- **There is no idempotency key on any Zoom Phone operation.** Guard every retry of an assign
  call by re-reading `phoneUser` first.

## Confirm it worked

Re-run `phoneUser` and check `calling_plans`, `phone_numbers` and `emergency_address`. For live
verification, subscribe to `phone.caller_ringing` / `phone.callee_answered`
(`asyncapi/zoom-phone-webhooks.yml`) and place a test call.
