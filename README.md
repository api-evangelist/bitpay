# BitPay

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
