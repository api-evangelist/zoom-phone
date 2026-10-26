# Zoom Phone (zoom-phone)

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

Zoom Phone is the cloud PBX / UCaaS voice product of Zoom Communications, headquartered in San Jose, California, and sold worldwide from its United States home market. It replaces on-premise telephony with a cloud calling service — extensions, auto receptionists, IVR, call queues, shared line groups, voicemail, call recording, fax, emergency (E911) addressing, and SMS/MMS — delivered either on Zoom-provided PSTN service, on a customer's own carrier through BYOC and Cloud Peering (Provider Exchange), or resold through carrier partners.

In the telecom value chain Zoom Phone sits above the network as a UCaaS application layer that buys wholesale connectivity and number inventory from carriers rather than operating a mobile network. Its API posture is the software half of the sector's split: a real self-serve developer portal, downloadable OpenAPI, a published event catalog, a public Postman workspace, and an official SDK — with no CAMARA network APIs, no GSMA Open Gateway membership, and no TM Forum Open API conformance, none of which apply to a company that is a carrier's customer rather than a carrier.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/zoom-phone/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/zoom-phone/refs/heads/main/apis.yml)

## Tags

- Telecommunications
- United States
- UCaaS
- Cloud PBX
- Voice
- VoIP
- SIP
- Messaging
- SMS
- Phone Numbers
- Number Porting
- BYOC
- Carrier Peering
- Contact Center
- Communications

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

### Zoom Phone API

The administrative and operational REST API for Zoom's cloud phone system — 238 paths and 391 operations across 46 resource groups, including Users, Sites, Call Queues, Auto Receptionists, Shared Line Groups, Common Areas, Phone Devices, Call Logs, Recordings, Voicemails, Fax, SMS, SMS Campaigns, Phone Numbers, Emergency Addresses and Emergency Service Locations, Outbound Calling, Routing Rules, Dashboard, Reports, Provider Exchange and Carrier Reseller.

- **Human URL:** [https://developers.zoom.us/docs/api/phone/](https://developers.zoom.us/docs/api/phone/)
- **Base URL:** `https://api.zoom.us/v2`

#### Properties

- [Documentation](https://developers.zoom.us/docs/api/phone/)
- [API Reference](https://developers.zoom.us/docs/api/phone/)
- [OpenAPI](openapi/zoom-phone-api-openapi.json) — harvested verbatim from `https://developers.zoom.us/api-hub/phone/methods/endpoints.json` (200, 2026-07-25)
- [Postman Collection](https://www.postman.com/zoom-developer/zoom-public-workspace/documentation/uba96fr/phone)

### Zoom Phone Webhooks

The Zoom Phone event catalog, published as an OpenAPI 3.1 document using the top-level `webhooks` object — 71 real-time events covering call lifecycle, transfers, recordings and transcripts, voicemail, fax, SMS delivery and 10DLC opt-in/opt-out, device registration, emergency alerts, AI call summaries, and setting changes.

- **Human URL:** [https://developers.zoom.us/docs/api/phone/events/](https://developers.zoom.us/docs/api/phone/events/)

#### Properties

- [Documentation](https://developers.zoom.us/docs/api/phone/events/)
- [OpenAPI](openapi/zoom-phone-webhooks-openapi.json) — harvested verbatim from `https://developers.zoom.us/api-hub/phone/events/webhooks.json` (200, 2026-07-25)

### Zoom Phone Number Management API

Provisions and manages phone number inventory for Zoom Phone, Zoom Contact Center and Zoom Meetings accounts — 17 paths and 28 operations covering allocation, BYOC numbers, carrier and cloud peering numbers, ported number orders, SIP trunks and SIP groups, phone plans, and 10DLC SMS campaigns and consent. The most carrier-facing surface Zoom publishes.

- **Human URL:** [https://developers.zoom.us/docs/api/number-management/](https://developers.zoom.us/docs/api/number-management/)
- **Base URL:** `https://api.zoom.us/v2`

#### Properties

- [Documentation](https://developers.zoom.us/docs/api/number-management/)
- [OpenAPI](openapi/zoom-phone-number-management-openapi.json) — harvested verbatim from `https://developers.zoom.us/api-hub/number-management/methods/endpoints.json` (200, 2026-07-25)

## Authentication

OAuth 2.0. RFC 8414 authorization server metadata is served anonymously at [https://zoom.us/.well-known/oauth-authorization-server](https://zoom.us/.well-known/oauth-authorization-server): issuer `https://zoom.us`, authorize `https://zoom.us/oauth/authorize`, token `https://zoom.us/oauth/token`, grants `authorization_code`, `refresh_token`, `client_credentials` and `urn:ietf:params:oauth:grant-type:jwt-bearer`. Scopes are granular — `phone:read:admin`, `phone:write:admin`, `phone:delete:customized_number:admin`, and so on. CIBA does not appear.

## Standards Posture

- **CAMARA:** no CAMARA reference found. Zoom Phone exposes no CAMARA network APIs.
- **GSMA Open Gateway:** not a signatory — Open Gateway signatories are mobile network operators.
- **Aduna:** no relationship found; Zoom's carrier channel is its own Provider Exchange / BYOC programme.
- **TM Forum Open APIs:** no conformance certification found.
- **3GPP:** no NEF/SCEF, network slicing, or MEC surface — Zoom operates no network.

## Links

- [Product](https://www.zoom.com/en/products/voip-phone/)
- [Developer Portal](https://developers.zoom.us/)
- [App Marketplace](https://marketplace.zoom.us/)
- [Pricing](https://zoom.us/pricing/zoom-phone)
- [Postman Workspace](https://www.postman.com/zoom-developer/zoom-public-workspace/overview)
- [GitHub](https://github.com/zoom)
- [Rivet SDK (Node/TypeScript)](https://github.com/zoom/rivet-javascript)
- [Developer Blog](https://developers.zoom.us/blog/)
- [Status](https://www.zoomstatus.com/)
