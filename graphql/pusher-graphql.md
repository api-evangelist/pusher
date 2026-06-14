# Pusher GraphQL Schema

## Overview

This conceptual GraphQL schema models the Pusher platform — covering both **Pusher Channels** (real-time pub/sub messaging over WebSocket and HTTP) and **Pusher Beams** (cross-platform push notifications for iOS, Android, and Web).

The schema is derived from the Pusher REST API and WebSocket protocol documentation.

- REST API reference: https://pusher.com/docs/channels/library_auth_reference/rest-api/
- Channels docs: https://pusher.com/docs/channels
- Beams docs: https://pusher.com/docs/beams
- GitHub: https://github.com/pusher

---

## Schema File

[pusher-schema.graphql](pusher-schema.graphql)

---

## Type Summary

### App & Cluster (4 types)

| Type | Description |
|------|-------------|
| `App` | A Pusher application identified by app_id, key, and secret |
| `AppKey` | The public key distributed to client-side connections |
| `AppSecret` | The HMAC signing secret used server-side |
| `ClusterInfo` | Regional cluster metadata (eu, us2, ap1, etc.) |

### Channels (7 types)

| Type | Description |
|------|-------------|
| `AppChannel` | A named channel within a Pusher app |
| `ChannelInfo` | REST API channel state (occupied, subscriber count) |
| `ChannelList` | Paginated list of channels matching a filter |
| `ChannelSubscription` | A socket-to-channel subscription record |
| `PresenceChannelInfo` | Presence channel state including member list |
| `PresenceMember` | A user participating in a presence channel |
| `OccupancyInfo` | Subscription and user counts for a channel |

### Events (4 types)

| Type | Description |
|------|-------------|
| `Event` | A triggered event on a channel |
| `TriggerEvent` | An event ready to be dispatched via the REST API |
| `BatchEvent` | One item in a batch trigger request |
| `EventData` | The JSON payload of an event |

### Authentication & Sockets (5 types)

| Type | Description |
|------|-------------|
| `AuthToken` | Token returned by the auth endpoint |
| `SocketID` | Unique identifier for a WebSocket connection |
| `PrivateAuth` | Auth response for private channel subscriptions |
| `PresenceAuth` | Auth response with presence member data |
| `AuthorizationResponse` | Generic auth response envelope |

### Connections (3 types)

| Type | Description |
|------|-------------|
| `Connection` | A live WebSocket connection to Pusher |
| `ConnectionEvent` | State-change or lifecycle event on a connection |
| `ConnectionData` | Extra metadata attached to a connection event |

### Channel Type Models (4 types)

| Type | Description |
|------|-------------|
| `PublicChannel` | Open channel, no authentication required |
| `PrivateChannel` | Server-authenticated channel |
| `PresenceChannel` | Authenticated channel with member roster |
| `EncryptedChannel` | End-to-end encrypted private channel |

### Webhooks (4 types)

| Type | Description |
|------|-------------|
| `WebhookEvent` | A webhook delivery envelope from Pusher |
| `WebhookPayloadEvent` | A single event entry in a webhook payload |
| `EventWebhook` | Webhook for a published client or server event |
| `ChannelWebhook` | Webhook for channel occupied / vacated |
| `MemberWebhook` | Webhook for presence member added / removed |

### Pusher Beams (8 types)

| Type | Description |
|------|-------------|
| `BeamsNotification` | A Beams push notification send request |
| `NotificationPayload` | Multi-platform notification payload |
| `WebNotification` | Web Push notification fields |
| `AndroidNotification` | Android (FCM) notification fields |
| `IOSNotification` | iOS (APNs) notification fields |
| `BeamsToken` | JWT token for authenticated Beams targeting |
| `User` | A Beams authenticated user |
| `UserInterest` | A named topic a device is subscribed to |

### Devices (2 types)

| Type | Description |
|------|-------------|
| `Device` | A device registered with Pusher Beams |
| `DeviceInfo` | SDK, OS, and device metadata |

### API Meta (4 types)

| Type | Description |
|------|-------------|
| `APIResponse` | Standard response envelope |
| `ErrorDetail` | Structured error returned by the API |
| `APIStats` | Aggregate statistics for an app |
| `APIUsage` | Billing/quota usage metrics |

---

## Enums

| Enum | Values |
|------|--------|
| `ChannelType` | PUBLIC, PRIVATE, PRESENCE, ENCRYPTED |
| `ConnectionState` | CONNECTING, CONNECTED, UNAVAILABLE, FAILED, DISCONNECTED |
| `DevicePlatform` | IOS, ANDROID, WEB |
| `WebhookEventType` | CHANNEL_OCCUPIED, CHANNEL_VACATED, MEMBER_ADDED, MEMBER_REMOVED, CLIENT_EVENT, CACHE_MISS |
| `NotificationPriority` | LOW, NORMAL, HIGH |

---

## Operations

### Queries

- `app` — fetch a Pusher app by ID
- `channels` — list channels in an app with optional prefix/type filter
- `channel` — get info on a specific channel
- `presenceChannelInfo` — get the member roster for a presence channel
- `cluster` — fetch cluster metadata
- `appStats` / `appUsage` — billing and usage metrics
- `device` / `deviceInterests` / `beamsUser` — Beams device and user queries

### Mutations

- `triggerEvent` — publish an event to one or more channels
- `triggerBatchEvents` — publish multiple events in one request
- `authorizeChannel` — authenticate a socket for a private or presence channel
- `sendBeamsNotification` — send a push notification via Beams
- `generateBeamsToken` — issue a Beams JWT for authenticated targeting
- `registerDevice` / `deleteDevice` — manage Beams device registrations
- `addDeviceInterest` / `removeDeviceInterest` / `setDeviceInterests` — manage device topic subscriptions
- `deleteBeamsUser` — purge all Beams state for a user

### Subscriptions

- `channelEvents` — real-time stream of events on a channel
- `presenceMemberEvents` — join/leave stream for a presence channel
- `connectionStateChanged` — connection lifecycle updates
- `webhookEvents` — app-level webhook event stream

---

## Total Named Types

55 named types (object types, enums, scalars, and inputs).
