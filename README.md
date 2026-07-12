# NumLookupAPI (numlookupapi)

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
