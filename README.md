# Pusher (pusher)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Pusher is a realtime communication platform owned by MessageBird/Bird. Its primary product Channels provides pub/sub messaging over WebSocket and HTTP; Beams provides device push notifications. Authentication uses an app key + secret per Pusher app. Channels and Beams are still actively sold; the older Chatkit product was sunset.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/pusher/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/pusher/refs/heads/main/apis.yml)

## Tags

- Realtime
- WebSockets
- Pub/Sub
- Push Notifications
- Messaging

## Timestamps

- **Created:** 2026-05-08
- **Modified:** 2026-05-29

## APIs

### Pusher Channels API

Pub/sub channels over WebSocket (client) and HTTP (server publish). Public, private, and presence channels supported. WebSocket endpoint at ws-{cluster}.pusher.com. Cluster hostnames include eu, us2, us3, ap1, ap2, ap3, etc.

- **Human URL:** [https://pusher.com/docs/channels](https://pusher.com/docs/channels)
- **Base URL:** `https://api-{cluster}.pusher.com/apps/{app_id}`

#### Tags

- Pub/Sub
- WebSockets
- HTTP
- Messaging

#### Properties

- [Documentation](https://pusher.com/docs/channels)
- [Pricing](https://pusher.com/channels/pricing)
- [AsyncAPI](asyncapi/pusher-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [Postman Collection](collections/pusher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pusher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Pusher Beams API

Server API for sending iOS, Android, and Web push notifications via FCM, APNs, and Web Push.

- **Human URL:** [https://pusher.com/docs/beams](https://pusher.com/docs/beams)
- **Base URL:** `https://{instance_id}.pushnotifications.pusher.com`

#### Tags

- Push Notifications
- Mobile
- Web Push

#### Properties

- [Documentation](https://pusher.com/docs/beams)
- [Pricing](https://pusher.com/beams/pricing)
- [Postman Collection](collections/pusher.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/pusher.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/pusher-app)
- [Portal](https://pusher.com/)
- [Documentation](https://pusher.com/docs)
- [Pricing](https://pusher.com/channels/pricing)
- [Git Hub](https://github.com/pusher)
- [Status Page](https://status.pusher.com/)
- [Plans](plans/pusher-plans-pricing.yml)
- [Rate Limits](rate-limits/pusher-rate-limits.yml)
- [Fin Ops](finops/pusher-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
