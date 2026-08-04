# Courier (courier-com)

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

Courier is notification infrastructure for product and engineering teams - a single API that orchestrates transactional and product messaging across email, SMS, push, chat (Slack, Teams), and an in-app inbox. One `POST /send` call routes a notification to the right channel(s) per recipient using templates designed in a visual studio, subscription topics, user preferences, brands, audiences, and automation workflows. The REST API (base `https://api.courier.com`) also manages users/profiles, lists, tenants for multi-tenant apps, translations, bulk sends, and audit events, and is wrapped by official server SDKs (Node, Python, Go, Ruby, PHP, Java) and a CLI. Authentication is a Bearer API key. The documented asynchronous event mechanism is HMAC-signed outbound webhooks.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/courier-com/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/courier-com/refs/heads/main/apis.yml)

## Tags

- Notifications
- Messaging
- Email
- SMS
- Push
- Multi-Channel
- Notification Infrastructure
- In-App Inbox

## Timestamps

- **Created:** 2026-07-02
- **Modified:** 2026-07-02

## APIs

### Courier Send API

The core `POST /send` endpoint. Dispatches a single notification to one or more recipients and routes it across channels (email, SMS, push, chat, inbox) using a template or inline content, per-recipient routing, data, and overrides.

- **Human URL:** [https://www.courier.com/docs/reference/send/send-a-message](https://www.courier.com/docs/reference/send/send-a-message)
- **Base URL:** `https://api.courier.com`

#### Tags

- Send
- Notifications
- Multi-Channel

#### Properties

- [API Reference](https://www.courier.com/docs/reference/send/send-a-message)
- [Documentation](https://www.courier.com/docs/sending/index)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Messages API

List and inspect sent messages - retrieve a message, its rendered content, its delivery/engagement history (ENQUEUED, SENT, DELIVERED, OPENED, CLICKED), cancel an enqueued message, and archive messages.

- **Human URL:** [https://www.courier.com/docs/reference/messages](https://www.courier.com/docs/reference/messages)
- **Base URL:** `https://api.courier.com`

#### Tags

- Messages
- Delivery Status
- Tracking

#### Properties

- [API Reference](https://www.courier.com/docs/reference/messages)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Lists API

Manage subscription lists and their subscribers - create/replace, list, get, delete, and restore lists, and add, subscribe, list, and remove the users subscribed to a list for group and topic-based sends.

- **Human URL:** [https://www.courier.com/docs/reference/lists](https://www.courier.com/docs/reference/lists)
- **Base URL:** `https://api.courier.com`

#### Tags

- Lists
- Subscriptions
- Audiences

#### Properties

- [API Reference](https://www.courier.com/docs/reference/lists)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier User Profiles API

Store and manage recipient profiles keyed by your user id - create, get, replace, merge/patch, and delete a profile, and list the subscription lists a user belongs to. Profiles hold channel addresses (email, phone, tokens) and custom data used at send time.

- **Human URL:** [https://www.courier.com/docs/reference/profiles](https://www.courier.com/docs/reference/profiles)
- **Base URL:** `https://api.courier.com`

#### Tags

- Profiles
- Users
- Recipients

#### Properties

- [API Reference](https://www.courier.com/docs/reference/profiles)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier User Preferences API

Read and update a recipient's notification preferences - list all topic preferences for a user, get a single topic, and update a user's channel opt-in/opt-out status per subscription topic.

- **Human URL:** [https://www.courier.com/docs/reference/user-preferences](https://www.courier.com/docs/reference/user-preferences)
- **Base URL:** `https://api.courier.com`

#### Tags

- Preferences
- Topics
- Opt-Out

#### Properties

- [API Reference](https://www.courier.com/docs/reference/user-preferences)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Device Tokens API

Register and manage the push notification device tokens (APNS, FCM, Expo) attached to a user - put, patch, get one, list all, and delete tokens so push notifications route to the right devices.

- **Human URL:** [https://www.courier.com/docs/reference/token-management](https://www.courier.com/docs/reference/token-management)
- **Base URL:** `https://api.courier.com`

#### Tags

- Push
- Device Tokens
- Mobile

#### Properties

- [API Reference](https://www.courier.com/docs/reference/token-management)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Notification Templates API

Programmatic access to notification templates designed in the Courier studio - list notifications, get and update their content blocks, and submit a draft to publish. Templates are referenced by id in the Send API.

- **Human URL:** [https://www.courier.com/docs/reference/notifications](https://www.courier.com/docs/reference/notifications)
- **Base URL:** `https://api.courier.com`

#### Tags

- Templates
- Notifications
- Content

#### Properties

- [API Reference](https://www.courier.com/docs/reference/notifications)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Brands API

Manage reusable brands - the logos, colors, and email template styling applied to notifications. Create, get, list, replace, and delete brands that are referenced by id at send time or on a template.

- **Human URL:** [https://www.courier.com/docs/reference/brands](https://www.courier.com/docs/reference/brands)
- **Base URL:** `https://api.courier.com`

#### Tags

- Brands
- Theming
- Branding

#### Properties

- [API Reference](https://www.courier.com/docs/reference/brands)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Automations API

Invoke Courier Automations - multi-step notification workflows with delays, throttling, conditional branches, and batched sends. Invoke an ad-hoc automation run or invoke a saved automation template by id.

- **Human URL:** [https://www.courier.com/docs/reference/automations](https://www.courier.com/docs/reference/automations)
- **Base URL:** `https://api.courier.com`

#### Tags

- Automations
- Workflows
- Orchestration

#### Properties

- [API Reference](https://www.courier.com/docs/reference/automations)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Audiences API

Define dynamic audiences from filters on user profile attributes - create/update, get, list, and delete an audience, and list the members that currently match. Audiences can be targeted by the Send API as recipients.

- **Human URL:** [https://www.courier.com/docs/reference/audiences](https://www.courier.com/docs/reference/audiences)
- **Base URL:** `https://api.courier.com`

#### Tags

- Audiences
- Segmentation
- Filters

#### Properties

- [API Reference](https://www.courier.com/docs/reference/audiences)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Tenants API

Model organizations/accounts in multi-tenant products - create/replace, get, list, and delete tenants, manage tenant default preferences, and associate users with one or many tenants for scoped branding and preferences.

- **Human URL:** [https://www.courier.com/docs/reference/tenants](https://www.courier.com/docs/reference/tenants)
- **Base URL:** `https://api.courier.com`

#### Tags

- Tenants
- Multi-Tenant
- Organizations

#### Properties

- [API Reference](https://www.courier.com/docs/reference/tenants)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Bulk API

Send the same notification to many recipients efficiently via a job - create a bulk job, add users to it, run it, get the job status, and list the users in the job. Designed for large one-to-many sends.

- **Human URL:** [https://www.courier.com/docs/reference/bulk](https://www.courier.com/docs/reference/bulk)
- **Base URL:** `https://api.courier.com`

#### Tags

- Bulk
- Batch
- High Volume

#### Properties

- [API Reference](https://www.courier.com/docs/reference/bulk)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Audit Events API

Retrieve workspace audit events for security and compliance - list all audit events and get a single event by id, covering administrative and configuration changes in the Courier workspace.

- **Human URL:** [https://www.courier.com/docs/reference/audit-events](https://www.courier.com/docs/reference/audit-events)
- **Base URL:** `https://api.courier.com`

#### Tags

- Audit Events
- Compliance
- Logs

#### Properties

- [API Reference](https://www.courier.com/docs/reference/audit-events)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Courier Translations API

Manage localization strings for notifications - get and update the translation (.po) content for a given domain and locale so notifications render in the recipient's language.

- **Human URL:** [https://www.courier.com/docs/reference/translations](https://www.courier.com/docs/reference/translations)
- **Base URL:** `https://api.courier.com`

#### Tags

- Translations
- Localization
- i18n

#### Properties

- [API Reference](https://www.courier.com/docs/reference/translations)
- [OpenAPI](openapi/courier-com-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/courier-com.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/courier-com.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/trycourier)
- [LinkedIn](https://www.linkedin.com/company/trycourier)
- [Website](https://www.courier.com)
- [Documentation](https://www.courier.com/docs)
- [Plans](plans/courier-com-plans-pricing.yml)
- [Rate Limits](rate-limits/courier-com-rate-limits.yml)
- [Fin Ops](finops/courier-com-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
