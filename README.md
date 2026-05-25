# RocketReach

RocketReach is a Seattle-based B2B contact data and sales intelligence provider that maintains a database
of 700M+ professional profiles and 60M+ companies. Its REST API exposes email, phone, and social-handle
discovery plus company firmographics for sales prospecting, recruiting, marketing enrichment, and CRM
hydration. Results are returned as structured profile and company objects and can be delivered
asynchronously via webhooks.

- Portal: <https://rocketreach.co>
- API Portal: <https://rocketreach.co/api>
- Reference: <https://docs.rocketreach.co/reference/rocketreach-api>
- Support: <api@rocketreach.co>

## APIs

| API | Description | OpenAPI |
| --- | --- | --- |
| RocketReach People Lookup API | Person enrichment by name+employer, LinkedIn URL, profile id, email, or NPI; supports single, bulk (up to 100), combined person+company, status polling, and webhook delivery via the legacy and Universal endpoints. | [openapi/rocketreach-people-lookup-api-openapi.yml](openapi/rocketreach-people-lookup-api-openapi.yml) |
| RocketReach People Search API | Search 700M+ professional profiles with filters such as name, current employer, title, location, skills, industry, and education. | [openapi/rocketreach-people-search-api-openapi.yml](openapi/rocketreach-people-search-api-openapi.yml) |
| RocketReach Company Lookup API | Single-company firmographic enrichment by domain, name, LinkedIn URL, or RocketReach company id. | [openapi/rocketreach-company-lookup-api-openapi.yml](openapi/rocketreach-company-lookup-api-openapi.yml) |
| RocketReach Company Search API | Search the company database by industry, headcount, revenue, location, and technology stack. | [openapi/rocketreach-company-search-api-openapi.yml](openapi/rocketreach-company-search-api-openapi.yml) |
| RocketReach Account API | Retrieve and manage API account details, API keys, and lookup / export / Universal credit balances. | [openapi/rocketreach-account-api-openapi.yml](openapi/rocketreach-account-api-openapi.yml) |

## Authentication

All endpoints require an `Api-Key` header. Generate and rotate keys from the
[API Usage & Settings page](https://rocketreach.co/account?section=nav_gen_api).

## Rate limits

A global ceiling of **10 requests per second** applies across all APIs. Tier-specific per-minute, per-hour,
per-day, and per-month limits vary by plan (Essentials, Pro, Ultimate, Custom) and by endpoint family
(Person Search, Person Lookup, Company Search, Bulk Jobs). On throttle, responses include a
`Retry-After` header. See <https://docs.rocketreach.co/reference/rate-limits>.

## Webhooks

People and bulk-people lookups can deliver results asynchronously to a configured webhook. Each delivery
carries an `RR-Request-ID` header that correlates with the originating request. See
<https://docs.rocketreach.co/reference/webhooks>.

## Universal Credits

The newer Universal endpoints (`/api/v2/universal/*`) share a single credit pool across people lookups,
people search, company lookups, and company search. See
<https://docs.rocketreach.co/reference/universal-credits-overview>.

## Profile maintainer

Kin Lane / API Evangelist — <kin@apievangelist.com>
