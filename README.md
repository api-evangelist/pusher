# Pusher (pusher)

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
