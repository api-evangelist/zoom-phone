# Zoom Phone

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Zoom Phone is the cloud PBX / UCaaS voice product of Zoom Communications, headquartered in San Jose, California, and sold worldwide from its United States home market. It replaces on-premise telephony with a cloud calling service — extensions, auto receptionists, IVR, call queues, shared line groups, voicemail, call recording, fax, emergency (E911) addressing, and SMS/MMS — delivered either on Zoom-provided PSTN service, on a customer's own carrier through BYOC and Cloud Peering (Provider Exchange), or resold through carrier partners. In the telecom value chain Zoom Phone sits above the network as a UCaaS application layer that buys wholesale connectivity and number inventory from carriers rather than operating a mobile network, and its API posture reflects the software half of that split rather than the carrier half: the Zoom Phone API is fully self-serve, published as downloadable OpenAPI 3.0 with 391 documented operations across 46 resource groups, a 71-event webhook catalog, a separate Number Management API covering number allocation, BYOC numbers, ported number orders, SIP trunks and 10DLC SMS campaigns, OAuth 2.0 with fine-grained phone:* scopes, a public Postman workspace, and an official Node/TypeScript SDK. It is not a mobile network operator, is not a GSMA Open Gateway signatory, and exposes no CAMARA network APIs — no CAMARA reference was found anywhere in its developer surface.

**Areas:** Telecommunications · United States · UCaaS · Cloud PBX · Voice · VoIP · SIP · Messaging · SMS · Phone Numbers · Number Porting · BYOC

## Zoom Phone on APIs.io

Everything profiled for Zoom Phone is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/zoom-phone/](https://apis.io/providers/zoom-phone/)** — or go straight to one of the APIs or properties below.

### APIs (51)

- [Zoom Phone Accounts API](https://apis.io/apis/zoom-phone/zoom-phone-accounts-api/) — The Accounts API from Zoom Phone — 2 operation(s) for accounts.
- [Zoom Phone Alerts API](https://apis.io/apis/zoom-phone/zoom-phone-alerts-api/) — The Alerts API from Zoom Phone — 2 operation(s) for alerts.
- [Zoom Phone Audio Library API](https://apis.io/apis/zoom-phone/zoom-phone-audio-library-api/) — The Audio Library API from Zoom Phone — 3 operation(s) for audio library.
- [Zoom Phone Auto Receptionists API](https://apis.io/apis/zoom-phone/zoom-phone-auto-receptionists-api/) — The Auto Receptionists API from Zoom Phone — 10 operation(s) for auto receptionists.
- [Zoom Phone Billing Account API](https://apis.io/apis/zoom-phone/zoom-phone-billing-account-api/) — The Billing Account API from Zoom Phone — 2 operation(s) for billing account.
- [Zoom Phone Blocked List API](https://apis.io/apis/zoom-phone/zoom-phone-blocked-list-api/) — The Blocked List API from Zoom Phone — 2 operation(s) for blocked list.
- [Zoom Phone Call Handling API](https://apis.io/apis/zoom-phone/zoom-phone-call-handling-api/) — The Call Handling API from Zoom Phone — 2 operation(s) for call handling.
- [Zoom Phone Call Logs API](https://apis.io/apis/zoom-phone/zoom-phone-call-logs-api/) — The Call Logs API from Zoom Phone — 15 operation(s) for call logs.
- [Zoom Phone Call Queues API](https://apis.io/apis/zoom-phone/zoom-phone-call-queues-api/) — The Call Queues API from Zoom Phone — 18 operation(s) for call queues.
- [Zoom Phone Carrier Reseller API](https://apis.io/apis/zoom-phone/zoom-phone-carrier-reseller-api/) — The Carrier Reseller API from Zoom Phone — 2 operation(s) for carrier reseller.
- [Zoom Phone Cloud Peering Provider Exchange API](https://apis.io/apis/zoom-phone/zoom-phone-cloud-peering-provider-exchange-api/) — The Cloud Peering Provider Exchange API from Zoom Phone — 2 operation(s) for cloud peering provider exchange.
- [Zoom Phone Common Areas API](https://apis.io/apis/zoom-phone/zoom-phone-common-areas-api/) — The Common Areas API from Zoom Phone — 14 operation(s) for common areas.
- [Zoom Phone Dashboard API](https://apis.io/apis/zoom-phone/zoom-phone-dashboard-api/) — The Dashboard API from Zoom Phone — 11 operation(s) for dashboard.
- [Zoom Phone Device Line Keys API](https://apis.io/apis/zoom-phone/zoom-phone-device-line-keys-api/) — The Device Line Keys API from Zoom Phone — 1 operation(s) for device line keys.
- [Zoom Phone Dial by Name Directory API](https://apis.io/apis/zoom-phone/zoom-phone-dial-by-name-directory-api/) — The Dial by Name Directory API from Zoom Phone — 2 operation(s) for dial by name directory.
- [Zoom Phone Emergency Addresses API](https://apis.io/apis/zoom-phone/zoom-phone-emergency-addresses-api/) — The Emergency Addresses API from Zoom Phone — 2 operation(s) for emergency addresses.
- [Zoom Phone Emergency Service Locations API](https://apis.io/apis/zoom-phone/zoom-phone-emergency-service-locations-api/) — The Emergency Service Locations API from Zoom Phone — 3 operation(s) for emergency service locations.
- [Zoom Phone External Contacts API](https://apis.io/apis/zoom-phone/zoom-phone-external-contacts-api/) — The External Contacts API from Zoom Phone — 2 operation(s) for external contacts.
- [Zoom Phone Fax API](https://apis.io/apis/zoom-phone/zoom-phone-fax-api/) — The Fax API from Zoom Phone — 6 operation(s) for fax.
- [Zoom Phone Firmware Update Rules API](https://apis.io/apis/zoom-phone/zoom-phone-firmware-update-rules-api/) — The Firmware Update Rules API from Zoom Phone — 3 operation(s) for firmware update rules.
- [Zoom Phone Group Call Pickup API](https://apis.io/apis/zoom-phone/zoom-phone-group-call-pickup-api/) — The Group Call Pickup API from Zoom Phone — 4 operation(s) for group call pickup.
- [Zoom Phone Groups API](https://apis.io/apis/zoom-phone/zoom-phone-groups-api/) — The Groups API from Zoom Phone — 2 operation(s) for groups.
- [Zoom Phone Inbound Blocked List API](https://apis.io/apis/zoom-phone/zoom-phone-inbound-blocked-list-api/) — The Inbound Blocked List API from Zoom Phone — 5 operation(s) for inbound blocked list.
- [Zoom Phone IVR API](https://apis.io/apis/zoom-phone/zoom-phone-ivr-api/) — The IVR API from Zoom Phone — 1 operation(s) for ivr.
- [Zoom Phone Line Keys API](https://apis.io/apis/zoom-phone/zoom-phone-line-keys-api/) — The Line Keys API from Zoom Phone — 2 operation(s) for line keys.
- [Zoom Phone Monitoring Groups API](https://apis.io/apis/zoom-phone/zoom-phone-monitoring-groups-api/) — The Monitoring Groups API from Zoom Phone — 4 operation(s) for monitoring groups.
- [Zoom Phone Outbound Calling API](https://apis.io/apis/zoom-phone/zoom-phone-outbound-calling-api/) — The Outbound Calling API from Zoom Phone — 12 operation(s) for outbound calling.
- [Zoom Phone Devices API](https://apis.io/apis/zoom-phone/zoom-phone-phone-devices-api/) — The Phone Devices API from Zoom Phone — 8 operation(s) for phone devices.
- [Zoom Phone Numbers API](https://apis.io/apis/zoom-phone/zoom-phone-phone-numbers-api/) — The Phone Numbers API from Zoom Phone — 10 operation(s) for phone numbers.
- [Zoom Phone Plan API](https://apis.io/apis/zoom-phone/zoom-phone-phone-plan-api/) — The Phone Plan API from Zoom Phone — 1 operation(s) for phone plan.
- [Zoom Phone Plans API](https://apis.io/apis/zoom-phone/zoom-phone-phone-plans-api/) — The Phone Plans API from Zoom Phone — 2 operation(s) for phone plans.
- [Zoom Phone Roles API](https://apis.io/apis/zoom-phone/zoom-phone-phone-roles-api/) — The Phone Roles API from Zoom Phone — 4 operation(s) for phone roles.
- [Zoom Phone Private Directory API](https://apis.io/apis/zoom-phone/zoom-phone-private-directory-api/) — The Private Directory API from Zoom Phone — 2 operation(s) for private directory.
- [Zoom Phone Provider Exchange API](https://apis.io/apis/zoom-phone/zoom-phone-provider-exchange-api/) — The Provider Exchange API from Zoom Phone — 2 operation(s) for provider exchange.
- [Zoom Phone Provision Templates API](https://apis.io/apis/zoom-phone/zoom-phone-provision-templates-api/) — The Provision Templates API from Zoom Phone — 2 operation(s) for provision templates.
- [Zoom Phone Recordings API](https://apis.io/apis/zoom-phone/zoom-phone-recordings-api/) — The Recordings API from Zoom Phone — 8 operation(s) for recordings.
- [Zoom Phone Reports API](https://apis.io/apis/zoom-phone/zoom-phone-reports-api/) — The Reports API from Zoom Phone — 4 operation(s) for reports.
- [Zoom Phone Routing Rules API](https://apis.io/apis/zoom-phone/zoom-phone-routing-rules-api/) — The Routing Rules API from Zoom Phone — 2 operation(s) for routing rules.
- [Zoom Phone Setting API](https://apis.io/apis/zoom-phone/zoom-phone-setting-api/) — The Setting API from Zoom Phone — 4 operation(s) for setting.
- [Zoom Phone Setting Templates API](https://apis.io/apis/zoom-phone/zoom-phone-setting-templates-api/) — The Setting Templates API from Zoom Phone — 2 operation(s) for setting templates.
- [Zoom Phone Settings API](https://apis.io/apis/zoom-phone/zoom-phone-settings-api/) — The Settings API from Zoom Phone — 6 operation(s) for settings.
- [Zoom Phone Shared Line Appearance API](https://apis.io/apis/zoom-phone/zoom-phone-shared-line-appearance-api/) — The Shared Line Appearance API from Zoom Phone — 1 operation(s) for shared line appearance.
- [Zoom Phone Shared Line Group API](https://apis.io/apis/zoom-phone/zoom-phone-shared-line-group-api/) — The Shared Line Group API from Zoom Phone — 13 operation(s) for shared line group.
- [Zoom Phone Sites API](https://apis.io/apis/zoom-phone/zoom-phone-sites-api/) — The Sites API from Zoom Phone — 4 operation(s) for sites.
- [Zoom Phone SMS API](https://apis.io/apis/zoom-phone/zoom-phone-sms-api/) — The SMS API from Zoom Phone — 7 operation(s) for sms.
- [Zoom Phone SMS Campaign API](https://apis.io/apis/zoom-phone/zoom-phone-sms-campaign-api/) — The SMS Campaign API from Zoom Phone — 6 operation(s) for sms campaign.
- [Zoom Phone SMS Campaigns API](https://apis.io/apis/zoom-phone/zoom-phone-sms-campaigns-api/) — The SMS Campaigns API from Zoom Phone — 3 operation(s) for sms campaigns.
- [Zoom Phone SMS Consent API](https://apis.io/apis/zoom-phone/zoom-phone-sms-consent-api/) — The SMS Consent API from Zoom Phone — 4 operation(s) for sms consent.
- [Zoom Phone Users API](https://apis.io/apis/zoom-phone/zoom-phone-users-api/) — The Users API from Zoom Phone — 13 operation(s) for users.
- [Zoom Phone Voicemails API](https://apis.io/apis/zoom-phone/zoom-phone-voicemails-api/) — The Voicemails API from Zoom Phone — 6 operation(s) for voicemails.
- [Zoom Phone Zoom Rooms API](https://apis.io/apis/zoom-phone/zoom-phone-zoom-rooms-api/) — The Zoom Rooms API from Zoom Phone — 7 operation(s) for zoom rooms.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Zoom Phone Webhooks](https://apis.io/asyncapis/zoom-phone/zoom-phone-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Zoom MCP Server (Workspace)](https://apis.io/servers/zoom-phone/zoom-mcp-server-workspace/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Zoom Phone Agentic Access](https://apis.io/agentic-access/zoom-phone/zoom-phone-agentic-access/)

#### Collections (3)

Postman and Open Collection request collections.

- [Phone](https://apis.io/collections/zoom-phone/open-zoom-phone-api/)
- [Number Management](https://apis.io/collections/zoom-phone/open-zoom-phone-number-management/)
- [Phone](https://apis.io/collections/zoom-phone/open-zoom-phone-webhooks/)

#### Overlays (54)

OpenAPI overlays, including conversational phrasing for each operation.

- [Zoom Phone Accounts Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-accounts-api-phrasing-overlay/)
- [Zoom Phone Alerts Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-alerts-api-phrasing-overlay/)
- [Zoom Phone Api Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-api-overlay/)
- [Zoom Phone Audio Library Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-audio-library-api-phrasing-overlay/)
- [Zoom Phone Auto Receptionists Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-auto-receptionists-api-phrasing-overlay/)
- [Zoom Phone Billing Account Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-billing-account-api-phrasing-overlay/)
- [Zoom Phone Blocked List Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-blocked-list-api-phrasing-overlay/)
- [Zoom Phone Call Handling Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-call-handling-api-phrasing-overlay/)
- [Zoom Phone Call Logs Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-call-logs-api-phrasing-overlay/)
- [Zoom Phone Call Queues Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-call-queues-api-phrasing-overlay/)
- [Zoom Phone Carrier Reseller Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-carrier-reseller-api-phrasing-overlay/)
- [Zoom Phone Cloud Peering Provider Exchange Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-cloud-peering-provider-exchange-api-phrasing-overlay/)
- [Zoom Phone Common Areas Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-common-areas-api-phrasing-overlay/)
- [Zoom Phone Dashboard Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-dashboard-api-phrasing-overlay/)
- [Zoom Phone Device Line Keys Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-device-line-keys-api-phrasing-overlay/)
- [Zoom Phone Dial By Name Directory Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-dial-by-name-directory-api-phrasing-overlay/)
- [Zoom Phone Emergency Addresses Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-emergency-addresses-api-phrasing-overlay/)
- [Zoom Phone Emergency Service Locations Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-emergency-service-locations-api-phrasing-overlay/)
- [Zoom Phone External Contacts Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-external-contacts-api-phrasing-overlay/)
- [Zoom Phone Fax Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-fax-api-phrasing-overlay/)
- [Zoom Phone Firmware Update Rules Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-firmware-update-rules-api-phrasing-overlay/)
- [Zoom Phone Group Call Pickup Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-group-call-pickup-api-phrasing-overlay/)
- [Zoom Phone Groups Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-groups-api-phrasing-overlay/)
- [Zoom Phone Inbound Blocked List Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-inbound-blocked-list-api-phrasing-overlay/)
- [Zoom Phone Ivr Api Phrasing Overlay](https://apis.io/overlays/zoom-phone/zoom-phone-ivr-api-phrasing-overlay/)
- …and 29 more published on APIs.io

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Zoom Phone Authentication](https://apis.io/security/zoom-phone/zoom-phone-authentication/)
- [Zoom Phone Domain Security](https://apis.io/security/zoom-phone/zoom-phone-domain-security/)
- [Zoom Phone Trust Center](https://apis.io/security/zoom-phone/zoom-phone-trust-center/)
- [Zoom Phone Vulnerability Disclosure](https://apis.io/security/zoom-phone/zoom-phone-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Zoom Phone Scopes](https://apis.io/scopes/zoom-phone/zoom-phone-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Zoom Phone Plans Pricing](https://apis.io/plans/zoom-phone/zoom-phone-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Zoom Phone Rate Limits](https://apis.io/rate-limits/zoom-phone/zoom-phone-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.zoom.com/en/products/voip-phone/)
- [Documentation](https://developers.zoom.us/docs/api/phone/)
- [Getting started](https://developers.zoom.us/docs/phone/start/)
- [API reference](https://developers.zoom.us/docs/api/phone/)
- [Pricing](https://zoom.us/pricing/zoom-phone)
- [Sign up](https://zoom.us/signup)
- [Support](https://developers.zoom.us/support/)
- [Changelog](https://developers.zoom.us/changelog/?product=phone)
- [Blog](https://developers.zoom.us/blog/)
- [Security](https://www.zoom.com/en/trust/reporting-vulnerability/)
- [Compliance](https://www.zoom.com/en/trust/)
- [Terms of service](https://www.zoom.com/en/trust/terms/)
- [Privacy policy](https://www.zoom.com/en/trust/privacy/)
- [GitHub](https://github.com/zoom)
- [Status](https://www.zoomstatus.com/)

## API Evangelist rating

**Kin Score 67.9** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 62.9 |
| Contract governance | 18.2 |
| Operational transparency | 92.1 |
| Developer ergonomics | 73.8 |
| Access clarity | 60.5 |

**Agent readiness 54.4** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | derived (partial credit) |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | yes |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 49.2** — Telecommunications

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/zoom-phone/](https://apis.io/providers/zoom-phone/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Zoom Phone: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/zoom-phone/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
