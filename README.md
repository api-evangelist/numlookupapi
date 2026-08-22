# NumLookupAPI (numlookupapi)

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

NumLookupAPI is a phone number validation and lookup REST API from everapi. A single GET request validates a phone number and returns whether it is valid along with its local and international formats, country prefix, ISO country code and name, geographic location, carrier, and line type (mobile, landline, etc.). It is used for phone verification, data validation, and caller identity enrichment.

## Access Model

NumLookupAPI is a commercial API with a free tier:

- **Free** — $0/month, 100 requests/month, capped at 10 requests/minute. No credit card required to start.
- **Basic** — $9.99/month, 5,000 requests/month, no per-minute rate cap.
- **Pro** — $49.99/month, 50,000 requests/month, no per-minute rate cap.
- **Scale** — $109.99/month, 250,000 requests/month, no per-minute rate cap.
- **Custom** — custom monthly volume and price; contact everapi.

All plans authenticate with a single API key. Paid plans remove the per-minute rate limit and are metered on a monthly request quota; only successful calls count against the quota. Yearly billing is discounted ~20% versus monthly. (Plan quotas and prices as published on the pricing page; billing terms are modeled and marked `reconciled: false` in `plans/` and `finops/`.)

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/numlookupapi/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/numlookupapi/refs/heads/main/apis.yml)

## Tags

- Number Verification
- Phone Validation
- Phone Number Lookup
- Carrier Lookup
- Line Type
- Verification
- Data Validation
- Caller Identity

## Timestamps

- **Created:** 2026-07-12
- **Modified:** 2026-07-12

## APIs

### NumLookupAPI Phone Number Validation API

Validate and look up a phone number with a single GET request. Returns a `valid` flag plus local and international formats, country prefix, ISO country code and name, location, carrier, and line type. Accepts numbers with a country prefix (e.g. `+14158586273`) or a bare number paired with an ISO `country_code`.

- **Human URL:** [https://numlookupapi.com/docs/validate](https://numlookupapi.com/docs/validate)
- **Base URL:** `https://api.numlookupapi.com/v1`

#### Tags

- Phone Validation
- Number Verification
- Carrier Lookup
- Line Type

#### Properties

- [Documentation](https://numlookupapi.com/docs)
- [API Reference](https://numlookupapi.com/docs/validate)
- [OpenAPI](openapi/numlookupapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/numlookupapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/numlookupapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### NumLookupAPI Account Status API

Return the current account identifier and remaining request quota for the month and any grace allowance. Requests to this endpoint do not count against your quota or rate limit.

- **Human URL:** [https://numlookupapi.com/docs/status](https://numlookupapi.com/docs/status)
- **Base URL:** `https://api.numlookupapi.com/v1`

#### Tags

- Account
- Quota
- Usage

#### Properties

- [API Reference](https://numlookupapi.com/docs/status)
- [OpenAPI](openapi/numlookupapi-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/numlookupapi.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/numlookupapi.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Authentication

Pass your API key in the `apikey` HTTP header (recommended) or as an `apikey` query-string parameter. See [authentication/numlookupapi-authentication.yml](authentication/numlookupapi-authentication.yml).

```
curl "https://api.numlookupapi.com/v1/validate/+14158586273" \
  -H "apikey: YOUR-API-KEY"
```

## Common Properties

- [Authentication](authentication/numlookupapi-authentication.yml)
- [Domain Security](security/numlookupapi-domain-security.yml)
- [GitHub Organization](https://github.com/everapihq)
- [LinkedIn](https://www.linkedin.com/company/everapi)
- [Website](https://numlookupapi.com)
- [Documentation](https://numlookupapi.com/docs)
- [Plans](plans/numlookupapi-plans-pricing.yml)
- [Rate Limits](rate-limits/numlookupapi-rate-limits.yml)
- [Fin Ops](finops/numlookupapi-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
