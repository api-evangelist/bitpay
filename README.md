# BitPay

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

BitPay is a cryptocurrency payment processing platform providing REST APIs for accepting Bitcoin and altcoin payments. Merchants use BitPay to create invoices, manage refunds, process payouts, and access settlement and ledger data. BitPay handles cryptocurrency conversion and settles funds daily to bank accounts or cryptocurrency wallets.

## APIs

- **Invoices API** - Create and manage time-sensitive payment requests with 15-minute price locks
- **Bills API** - Send payment requests to specific buyers with fixed-price line items
- **Payouts API** - Submit cryptocurrency payments to recipients for disbursements and payroll
- **Refunds API** - Process full or partial refunds associated with invoices
- **Settlements API** - Access transfer reports for payments settled to merchant accounts
- **Rates API** - Retrieve exchange rate data for supported cryptocurrencies and fiat currencies
- **Ledgers API** - Access account balance records and ledger entries by currency

## Authentication

BitPay uses token-based API access with two facades:

- **POS Facade** - No cryptographic signing required; tokens created in the merchant dashboard
- **Merchant Facade** - Requires ECDSA-signed requests via `X-Identity` and `X-Signature` headers

All requests must include `X-Accept-Version: 2.0.0`.

## SDKs

Official client libraries are available for:

- Node.js / TypeScript
- Java
- C# (.NET)
- Python
- PHP

## Pricing

Volume-based tiered per-transaction pricing with no monthly subscription fee:

| Monthly Volume | Fee |
|---|---|
| Under $500,000 | 2% + $0.25 |
| $500,000 - $999,999 | 1.5% + $0.25 |
| $1,000,000+ | 1% + $0.25 |

## Resources

- Developer Portal: https://developer.bitpay.com/docs
- API Reference: https://developer.bitpay.com/reference/concepts
- Status Page: https://status.bitpay.com/
- Support: https://support.bitpay.com/hc/en-us
- Terms of Use: https://www.bitpay.com/legal/terms-of-use
- GitHub: https://github.com/bitpay
- Pricing: https://bitpay.com/pricing
