# RocketReach (rocketreach)

RocketReach is a Seattle-based B2B contact data and sales intelligence provider that maintains a database of 700M+ professional profiles and 60M+ companies and exposes it through a REST API for email, phone, and social-handle discovery plus company firmographics. The platform is used for sales prospecting, recruiting, marketing enrichment, and CRM hydration, with results returned as structured profile and company objects and optional webhook delivery for asynchronous lookups.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/rocketreach/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/rocketreach/refs/heads/main/apis.yml)

## Scope

- **Position:** Provider
- **Access:** 3rd-Party

## Tags

- B2B
- Contact Data
- Email Lookup
- Phone Lookup
- Sales Intelligence
- Lead Generation
- People Search
- Company Search
- Data Enrichment
- Prospecting
- Recruiting
- Webhooks

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### RocketReach People Lookup API

Look up an individual's email addresses, phone numbers, social handles, and full enriched profile from a name + employer, LinkedIn URL, RocketReach profile id, NPI number, or email. Supports single lookups, bulk lookups (up to 100 queries per request), status polling, combined person+company lookups, and the newer Universal endpoints. Results can be delivered synchronously or via webhook with an RR-Request-ID correlation header.

- **Human URL:** [https://docs.rocketreach.co/reference/people-lookup-api](https://docs.rocketreach.co/reference/people-lookup-api)

#### Tags

- Contact Data
- Email Lookup
- People
- Enrichment
- Webhooks

#### Properties

- [Documentation](https://docs.rocketreach.co/reference/people-lookup-api)
- [Documentation](https://docs.rocketreach.co/reference/bulk-person-lookup-person-lookup-api)
- [Documentation](https://docs.rocketreach.co/reference/rocketreach-check-person-lookup-status-people-lookup-api)
- [Documentation](https://docs.rocketreach.co/reference/create_universal_person_lookup)
- [Documentation](https://docs.rocketreach.co/reference/create_universal_person_bulk_lookup)
- [Documentation](https://docs.rocketreach.co/reference/create_person_and_company_lookup)
- [OpenAPI](openapi/rocketreach-people-lookup-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rocketreach-people-lookup-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rocketreach-people-lookup-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### RocketReach People Search API

Search RocketReach's 700M+ professional profiles using filters such as name, current employer, title, location, skills, industry, and education. Returns paginated lists of profile summaries that can then be passed to the People Lookup API for full contact enrichment.

- **Human URL:** [https://docs.rocketreach.co/reference/people-search-api](https://docs.rocketreach.co/reference/people-search-api)

#### Tags

- People Search
- Sales Intelligence
- Prospecting

#### Properties

- [Documentation](https://docs.rocketreach.co/reference/people-search-api)
- [Documentation](https://docs.rocketreach.co/reference/create_universal_person_search)
- [OpenAPI](openapi/rocketreach-people-search-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rocketreach-people-search-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rocketreach-people-search-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### RocketReach Company Lookup API

Retrieve an enriched company profile from a domain, company name, LinkedIn URL, or RocketReach company id. Returns firmographics including headcount, industry, founded year, location, revenue band, technology stack, and key social and contact metadata.

- **Human URL:** [https://docs.rocketreach.co/reference/company-lookup-api](https://docs.rocketreach.co/reference/company-lookup-api)

#### Tags

- Company Data
- Firmographics
- Enrichment

#### Properties

- [Documentation](https://docs.rocketreach.co/reference/company-lookup-api)
- [Documentation](https://docs.rocketreach.co/reference/create_universal_company_lookup)
- [OpenAPI](openapi/rocketreach-company-lookup-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rocketreach-company-lookup-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rocketreach-company-lookup-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### RocketReach Company Search API

Search RocketReach's company database using firmographic filters such as industry, headcount, revenue, location, and technology stack. Returns paginated company summaries suitable for downstream enrichment via the Company Lookup API.

- **Human URL:** [https://docs.rocketreach.co/reference/company-search-api](https://docs.rocketreach.co/reference/company-search-api)

#### Tags

- Company Search
- Firmographics
- Sales Intelligence

#### Properties

- [Documentation](https://docs.rocketreach.co/reference/company-search-api)
- [Documentation](https://docs.rocketreach.co/reference/create_universal_company_search)
- [OpenAPI](openapi/rocketreach-company-search-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rocketreach-company-search-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rocketreach-company-search-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### RocketReach Account API

Retrieve and manage RocketReach API account details, generate new API keys, and inspect plan, lookup credit balance, export credit balance, and Universal Credits usage. Provides both legacy account endpoints and the newer Universal account endpoint.

- **Human URL:** [https://docs.rocketreach.co/reference/rocketreach-api-account](https://docs.rocketreach.co/reference/rocketreach-api-account)

#### Tags

- Account
- Administration
- Usage

#### Properties

- [Documentation](https://docs.rocketreach.co/reference/rocketreach-api-account)
- [Documentation](https://docs.rocketreach.co/reference/rocketreach-api-account-newaccount)
- [Documentation](https://docs.rocketreach.co/reference/get_universal_account)
- [OpenAPI](openapi/rocketreach-account-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rocketreach-account-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rocketreach-account-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://rocketreach.co)
- [Website](https://rocketreach.co)
- [A P I Portal](https://rocketreach.co/api)
- [Documentation](https://docs.rocketreach.co/)
- [Documentation](https://docs.rocketreach.co/reference/rocketreach-api)
- [Getting Started](https://docs.rocketreach.co/reference/rocketreach-api)
- [Documentation](https://docs.rocketreach.co/reference/universal-credits-overview)
- [Webhooks](https://docs.rocketreach.co/reference/webhooks)
- [Rate Limits](https://docs.rocketreach.co/reference/rate-limits)
- [Errors](https://docs.rocketreach.co/reference/responses-and-errors)
- [F A Q](https://docs.rocketreach.co/reference/faq)
- [Pricing](https://rocketreach.co/api)
- [Sign Up](https://rocketreach.co/signup)
- [Login](https://rocketreach.co/login)
- [Support](mailto:api@rocketreach.co)
- [Blog](https://rocketreach.co/blog)
- [Company](https://rocketreach.co/about)
- [Careers](https://rocketreach.co/careers)
- [Press](https://rocketreach.co/press)
- [Trust Center](https://rocketreach.co/security)
- [Privacy Policy](https://rocketreach.co/legal/privacy-policy)
- [Terms of Service](https://rocketreach.co/legal/terms-of-use)
- [LinkedIn](https://www.linkedin.com/company/rocketreach)
- [Twitter](https://twitter.com/RocketReach)
- [Facebook](https://www.facebook.com/rocketreach)
- [YouTube](https://www.youtube.com/@rocketreach)
- [Integrations](https://rocketreach.co/integrations/salesforce)
- [Integrations](https://rocketreach.co/integrations/hubspot)
- [Integrations](https://rocketreach.co/integrations/zapier)
- [Integrations](https://chromewebstore.google.com/detail/rocketreach-find-email-ph/oeglkmmgnoojkmdfkpeofkflckjdjbpe)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
