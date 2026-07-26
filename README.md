# Zoom Phone (zoom-phone)

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
