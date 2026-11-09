# Bank of Uganda Exchange Rates API — bou-exchange-rate

[![npm version](https://img.shields.io/npm/v/bou-exchange-rate.svg)](https://www.npmjs.com/package/bou-exchange-rate)
[![license](https://img.shields.io/npm/l/bou-exchange-rate.svg)](https://github.com/AllRates-Today/bou-exchange-rate/blob/main/LICENSE)
[![zero dependencies](https://img.shields.io/badge/dependencies-0-brightgreen.svg)](https://www.npmjs.com/package/bou-exchange-rate)
[![TypeScript](https://img.shields.io/badge/TypeScript-types%20included-3178C6.svg)](https://www.typescriptlang.org/)
[![USD/UGX today](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fbou%3Fsource%3DUSD%26target%3DUGX&query=%24.rate&label=USD%2FUGX%20published%20by%20Bank%20of%20Uganda&color=0A7E8C&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/bou/)
[![rate date](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fallratestoday.com%2Fapi%2Fopen%2Fcentral-bank%2Fbou%3Fsource%3DUSD%26target%3DUGX&query=%24.rate_date&label=rate%20date&color=555&cacheSeconds=3600)](https://allratestoday.com/central-bank-rates-api/bou/)

**Official Bank of Uganda (Uganda) daily exchange rates for Node.js and TypeScript. The published central bank rates behind tax filings, customs valuations, audits, and compliant invoicing — not market estimates, but the numbers Bank of Uganda itself prints, every business day.**

## 🚀 Why this client?

- 🏛️ **Official published rates** — Bank of Uganda's own table, with the publisher's own `rate_date` on every response
- 📅 **History from 2026** — this source publishes only its current table, so the archive builds forward from the day we started collecting
- 🔀 **Published vs derived, always flagged** — computed inverse/cross pairs carry `derived: true`, never mixed with official prints
- ⚡ **Zero dependencies** — pure ESM + CJS over global `fetch`; Node 18+, Bun, Deno, and edge runtimes
- 🔷 **Type-safe** — full TypeScript definitions shipped with the package
- 🧾 **Compliance-grade metadata** — `rate_type`, publication date, and source disclaimer on every response

> **Official rate, not mid-market:** every value here is a number Bank of Uganda itself published, fixed once printed and carrying the central bank's own `rate_date` — what filings and audits require. Need the live mid-market rate for pricing or display instead? Use the [mid-market API](https://allratestoday.com/docs/) or [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk). The two can diverge by several percent.

## 🔑 Get your API key

Get a free API key at [allratestoday.com/register](https://allratestoday.com/register) — no credit card required. Latest rates are on every plan, including free.

## 📈 Latest published table

[![Latest Bank of Uganda table](https://allratestoday.com/api/open/central-bank/bou/table.svg)](https://allratestoday.com/central-bank-rates-api/bou/)

The image is rendered live from the keyless endpoint, so it follows the central bank's publications on npm and on GitHub alike without a new release. The same table as text is folded below for search and copy-paste: on GitHub [a daily Action](.github/workflows/daily-table.yml) refreshes it whenever the central bank publishes a new table; on npm it is as of the package's publish date.

<!-- daily-table:start -->
<details>
<summary>Table as text: published 2026-11-09 by Bank of Uganda — 54 rates. Updated 2026-11-09.</summary>

| Base | Quote | Type | Rate |
| --- | --- | --- | ---: |
| EUR | UGX | buy | 4560.621324 |
| EUR | UGX | closing | 4592.756444 |
| EUR | UGX | closing_buy | 4586.74823 |
| EUR | UGX | closing_sell | 4598.764658 |
| EUR | UGX | midday | 4578.5945215 |
| EUR | UGX | midday_buy | 4572.797105 |
| EUR | UGX | midday_sell | 4584.391938 |
| EUR | UGX | reference | 4566.407598 |
| EUR | UGX | sell | 4572.193872 |
| GBP | UGX | buy | 5467.597884 |
| GBP | UGX | closing | 5505.687451 |
| GBP | UGX | closing_buy | 5498.771594 |
| GBP | UGX | closing_sell | 5512.603308 |
| GBP | UGX | midday | 5488.337364 |
| GBP | UGX | midday_buy | 5481.224031 |
| GBP | UGX | midday_sell | 5495.450697 |
| GBP | UGX | reference | 5474.903706 |
| GBP | UGX | sell | 5482.209528 |
| KES | UGX | buy | 31.402613 |
| KES | UGX | closing | 31.579263 |
| KES | UGX | closing_buy | 31.516462 |
| KES | UGX | closing_sell | 31.642065 |
| KES | UGX | midday | 31.499355 |
| KES | UGX | midday_buy | 31.42452 |
| KES | UGX | midday_sell | 31.574191 |
| KES | UGX | reference | 31.465279 |
| KES | UGX | sell | 31.527945 |
| TZS | UGX | buy | 1.5330131 |
| TZS | UGX | closing | 1.5509641928 |
| TZS | UGX | closing_buy | 1.5402782 |
| TZS | UGX | closing_sell | 1.5616502 |
| TZS | UGX | midday | 1.5476333 |
| TZS | UGX | midday_buy | 1.5369662 |
| TZS | UGX | midday_sell | 1.5583004 |
| TZS | UGX | reference | 1.546598 |
| TZS | UGX | sell | 1.5601829 |
| USD | UGX | buy | 4085.48 |
| USD | UGX | closing | 4102.14 |
| USD | UGX | closing_buy | 4097.14 |
| USD | UGX | closing_sell | 4107.14 |
| USD | UGX | midday | 4093.33 |
| USD | UGX | midday_buy | 4088.33 |
| USD | UGX | midday_sell | 4098.33 |
| USD | UGX | reference | 4090.48 |
| USD | UGX | sell | 4095.48 |
| ZAR | UGX | buy | 247.76101 |
| ZAR | UGX | closing | 249.54169424 |
| ZAR | UGX | closing_buy | 249.19199 |
| ZAR | UGX | closing_sell | 249.89139 |
| ZAR | UGX | midday | 248.31019 |
| ZAR | UGX | midday_buy | 247.95039 |
| ZAR | UGX | midday_sell | 248.66998 |
| ZAR | UGX | reference | 248.09813 |
| ZAR | UGX | sell | 248.43525 |

</details>

Source: [Official rates published by BOU, served by AllRatesToday](https://allratestoday.com/central-bank-rates-api/bou/). Rates are as printed by the central bank; AllRatesToday is not affiliated with it.
<!-- daily-table:end -->

## 📦 Installation

```bash
npm install bou-exchange-rate
```

```bash
yarn add bou-exchange-rate
```

```bash
pnpm add bou-exchange-rate
```

Requires Node 18+ (global `fetch`); also runs on Bun, Deno and edge runtimes. Also published under the org scope as [`@allratestoday/bou-exchange-rate`](https://www.npmjs.com/package/@allratestoday/bou-exchange-rate) — same code, same versions.

## 🏁 Quick start

```js
import { getRate } from 'bou-exchange-rate';

const pair = await getRate('USD', 'UGX', { apiKey: 'art_live_...' });
console.log(pair.rate, pair.rate_date); // the official Bank of Uganda rate, on the central bank's own date
```

## 📚 API reference

- [Latest pair rate](#latest-pair-rate) — one pair from the latest published table
- [Full published table](#full-published-table) — everything the central bank printed, in one call
- [Table for a date](#table-for-a-date) — the official table for an invoice or filing date
- [Daily time series](#daily-time-series) — one pair across a date range

---

### Latest pair rate

Free plan and up. Pairs the central bank does not print directly are resolved from its table and flagged (see *Published vs derived rates* below).

```js
const pair = await getRate('USD', 'UGX', { apiKey: 'art_live_...' });
```

**Response:**

```javascript
{
  bank: 'bou',
  name: 'Bank of Uganda',
  rate_date: '2026-10-14',   // Bank of Uganda's own publication date
  source: 'USD',
  target: 'UGX',
  rate: 4130.24,
  rate_type: 'reference',
  derived: false,
  method: 'published',
  disclaimer: 'Official rates as published by the named central bank. On weekends/holidays the most recent published rate_date is returned.'
}
```

### Full published table

Free plan and up. The complete table for the latest publication date.

```js
import { getLatestRates } from 'bou-exchange-rate';

const table = await getLatestRates({ apiKey: 'art_live_...' });
console.log(table.rate_date, table.rates.length);
```

**Response:**

```javascript
{
  bank: 'bou',
  name: 'Bank of Uganda',
  rate_date: '2026-10-14',
  rates: [
    { "base": "USD", "quote": "UGX", "type": "reference", "value": 4130.24 },
    { "base": "USD", "quote": "UGX", "type": "sell", "value": 4135.24 },
    { "base": "USD", "quote": "UGX", "type": "buy", "value": 4125.24 },
    // … the rest of the published table (33 currencies vs UGX)
  ],
  disclaimer: '…'
}
```

### Table for a date

Paid plans. The official table for any date since 2026 — weekends and holidays return the most recent published date, flagged via `published_on_requested_date`, which is exactly the in-force rate a filing needs.

```js
import { getRatesForDate } from 'bou-exchange-rate';

const day = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...' });
// Optionally narrow to one pair:
const one = await getRatesForDate('2026-06-30', { apiKey: 'art_live_...', source: 'USD', target: 'UGX' });
```

**Response:**

```javascript
{
  bank: 'bou',
  requested_date: '2026-06-30',
  rate_date: '2026-06-30',                // the date actually published
  published_on_requested_date: true,      // false when a weekend/holiday fell back
  rates: [ /* the full table for that date */ ],
  disclaimer: '…'
}
```

### Daily time series

Paid plans. One resolved rate per publication date — ready for charting, revaluation runs, or audit workpapers.

```js
import { getHistory } from 'bou-exchange-rate';

const series = await getHistory(
  { source: 'USD', target: 'UGX', from: '2026-01-01', to: '2026-10-14' },
  { apiKey: 'art_live_...' }
);
```

**Response:**

```javascript
{
  bank: 'bou',
  source: 'USD',
  target: 'UGX',
  from: '2026-01-01',
  to: '2026-10-14',
  count: 152,
  rates: [
    // one entry per publication date
    { date: '2026-10-14', rate: 4130.24, rate_type: 'reference', derived: false, method: 'published' },
    // …
  ],
  disclaimer: '…'
}
```

Pass `{ symbol: 'USD' }` instead of `source`/`target` to get the raw published rows for one currency (all rate types, no pair resolution).

---

## 🗺️ Currencies covered

Bank of Uganda currently publishes rates covering **33 currencies** against the UGX (as of the latest table):

🇦🇪 `AED` · 🇦🇺 `AUD` · 🇧🇮 `BIF` · 🇨🇦 `CAD` · 🇨🇭 `CHF` · 🇨🇳 `CNY` · 🇩🇯 `DJF` · 🇩🇰 `DKK` · 🇪🇹 `ETB` · 🇪🇺 `EUR` · 🇬🇧 `GBP` · 🇮🇳 `INR` · 🇯🇵 `JPY` · 🇰🇪 `KES` · 🇰🇲 `KMF` · 🇰🇷 `KRW` · 🇰🇼 `KWD` · 🇱🇸 `LSL` · 🇲🇺 `MUR` · 🇲🇼 `MWK` · 🇳🇴 `NOK` · 🇳🇿 `NZD` · 🇷🇼 `RWF` · 🇸🇦 `SAR` · 🇸🇪 `SEK` · 🇸🇸 `SSP` · 🇸🇿 `SZL` · 🇹🇿 `TZS` · 🇺🇸 `USD` · `XAU` · `XDR` · 🇿🇦 `ZAR` · 🇿🇼 `ZWG`

## 🏛️ Source

The Bank of Uganda publishes a daily opening rate card each morning — middle, buying and selling shilling rates for the major world currencies plus a COMESA table covering the region's currencies. The middle rate is the reference Ugandan banks and the revenue authority work from.

- Publisher's own page: [Exchange rates](https://bou.or.ug/) · [bou.or.ug](https://bou.or.ug)
- Publication: every business day; the exact schedule, freshness status and any current delay are on the [Bank of Uganda rates page](https://allratestoday.com/central-bank-rates-api/bou/)
- In the API: usually by **10:15 UTC** (measured over the last 9 publications). Schedule a sync at or after that time and retry hourly until `rate_date` moves; every response carries the same figure as `available_by_utc` — see [when to poll](https://allratestoday.com/docs/#when-to-poll)
- Values are stored unmodified, with the publisher's own `rate_date` on every row — see the [methodology](https://allratestoday.com/official-rates-methodology/)

## 🧭 Reading the numbers

- `value` is always **quote currency per 1 unit of base currency** (`base: "EUR", quote: "USD", value: 1.15` means 1 EUR = 1.15 USD).
- Bank of Uganda quotes **UGX per 1 unit of foreign currency** (e.g. `base: "USD", quote: "UGX"` means UGX per one US dollar).
- Need the other way round? Ask `getRate(target, source)` and the API inverts or crosses for you, flagged `derived: true` — never divide a published rate yourself in a compliance workflow.
- Precious-metal codes (`XAU`, `XAG`, `XPT`, `XPD`) are quoted **per troy ounce**.
- `rate_type` tells you which of the central bank's series a row belongs to (`reference` here); some publishers print buy/sell or several fixings for the same pair.

## 🧩 ERP & accounting systems

Loading the official Bank of Uganda rate into an accounting system is a supported workflow, not a hack. Step-by-step guides with the direction each system expects:

- [Dynamics 365 Business Central](https://allratestoday.com/docs/integrations/business-central/) — built-in Currency Exchange Rate Service, no code
- [Xero](https://allratestoday.com/docs/integrations/xero/) · [QuickBooks Online](https://allratestoday.com/docs/integrations/quickbooks/) · [SAP S/4HANA and ECC](https://allratestoday.com/docs/integrations/sap/) · [Odoo](https://allratestoday.com/docs/integrations/odoo/)

The same keyed endpoints return `?format=csv`, `?format=xml` and `?format=xlsx`, and accept the key as `?api_key=` on the URL for importers that cannot send headers:

```bash
curl "https://allratestoday.com/api/v1/central-bank/bou/latest?format=xml&api_key=art_live_..."
```

## 🤖 AI agents

- MCP server: `npx -y @allratestoday/central-bank-mcp` (stdio) or the hosted endpoint `https://allratestoday.com/api/mcp` — tools for official rates, history, cross-bank comparison and publication calendars
- Already using the general SDK or MCP server? Since 2026-10-01 [`@allratestoday/sdk`](https://www.npmjs.com/package/@allratestoday/sdk) 1.4+ has `officialRates('bou')` and [`@allratestoday/mcp-server`](https://www.npmjs.com/package/@allratestoday/mcp-server) 0.6+ has a `get_official_rates` tool — both return this source's latest table with no key, so you can add it without a second dependency
- Claude Code plugin (no key): `/plugin marketplace add AllRates-Today/claude-code-plugin` then `/plugin install allratestoday@allratestoday` — bundles both MCP servers plus an `/official-rate bou ...` command
- Evaluating? Agents can self-issue a trial key with no signup: `POST https://allratestoday.com/api/agent/keys` (send `Content-Type: application/json`) returns a 100-call key valid 7 days that covers the free-plan methods (latest table, pairs); dated tables and history need a [paid plan](https://allratestoday.com/pricing/). The MCP servers expose it as `request_trial_key`
- Machine-readable site guide: [llms.txt](https://allratestoday.com/llms.txt) · [for-ai-agents](https://allratestoday.com/for-ai-agents/)

## ⚖️ Published vs derived rates

If Bank of Uganda does not print a pair directly, the API resolves it from the central bank's own table and says so — official and computed values are never confused:

| `method` | `derived` | Meaning |
| --- | --- | --- |
| `published` | `false` | The central bank printed this pair directly |
| `inverse` | `true` | Computed as 1 ÷ the published opposite direction |
| `cross` | `true` | Computed via UGX from two published rates |

## 🛡️ Error handling

Errors are thrown as `Error` with `status` (HTTP code) and `body` (the API's JSON error) attached:

```js
try {
  const pair = await getRate('USD', 'XXX', { apiKey: 'art_live_...' });
} catch (err) {
  console.log(err.message); // human-readable reason
  console.log(err.status);  // e.g. 404
}
```

| Status | Meaning |
| ------ | ------- |
| — | Missing `apiKey` (thrown before any request) |
| `400` | Malformed date or parameters |
| `401` | Invalid API key |
| `403` | Endpoint needs a [paid plan](https://allratestoday.com/pricing/) (historical dates & series) |
| `404` | Pair or date range not covered by Bank of Uganda |
| `429` | Monthly quota exceeded |

## 🔷 TypeScript

Full definitions ship with the package — no `@types` install:

```ts
import type { LatestRates, PairRate, DatedRates, RateEntry, HistoryQuery, RequestOptions } from 'bou-exchange-rate';
```

## 📦 CommonJS

```javascript
const { getRate } = require('bou-exchange-rate');

getRate('USD', 'UGX', { apiKey: 'art_live_...' }).then((pair) => console.log(pair.rate));
```

## 💡 Quota tips

- Rates change once per business day — cache the published table locally and a small monthly quota goes a long way.
- Every request counts toward your AllRatesToday quota, shared across all AllRatesToday endpoints on your key.

## 📖 Methods reference

| Method | Plan | Description |
| ------ | ---- | ----------- |
| `getRate(source, target, { apiKey })` | Free | Latest rate for one pair, resolved from the published table |
| `getLatestRates({ apiKey })` | Free | The central bank's full latest published table |
| `getRatesForDate(date, { apiKey, source?, target? })` | Paid | The official table (or one pair) for a YYYY-MM-DD date |
| `getHistory({ symbol \| source+target, from?, to? }, { apiKey })` | Paid | Daily series since 2026 |

## 📥 Bulk data (no key)

Need the whole archive rather than an API call? The same published tables are mirrored daily as open data:

- Hugging Face: [AllRatesToday/central-bank-exchange-rates](https://huggingface.co/datasets/AllRatesToday/central-bank-exchange-rates) — one CSV per institution (`rates/bou.csv`)
- Kaggle: [allratestoday/central-bank-exchange-rates](https://www.kaggle.com/datasets/allratestoday/central-bank-exchange-rates)
- Raw JSON on GitHub: `https://raw.githubusercontent.com/AllRates-Today/central-bank-exchange-rates/main/data/bou/latest.json`

## 🔗 Links

- **Website:** [allratestoday.com](https://allratestoday.com)
- [Bank of Uganda rates page](https://allratestoday.com/central-bank-rates-api/bou/) — live table, publication cadence, FAQ
- [All central bank sources](https://allratestoday.com/central-bank-rates-api/)
- [Download central bank rates](https://allratestoday.com/download-central-bank-rates/) — every bank's latest table and history as Excel, CSV or JSON
- [Package docs on the site](https://allratestoday.com/docs/sdk/bou-exchange-rate/) · [ERP integration guides](https://allratestoday.com/docs/integrations/)
- [API documentation](https://allratestoday.com/docs/#central-bank) · [Interactive reference](https://allratestoday.com/api-reference/) · [Methodology](https://allratestoday.com/official-rates-methodology/)
- [Register (Free)](https://allratestoday.com/register) · [Dashboard](https://allratestoday.com/profile) · [Pricing](https://allratestoday.com/pricing/)
- [Status](https://allratestoday.com/status)
- [Postman collection](https://allratestoday.com/postman/)
- [ChatGPT app](https://chatgpt.com/plugins/plugin_asdk_app_6ae1e76098f48191a285ac3f5ab7a83b) — ask ChatGPT for live and official central bank rates
- [OpenAPI reference on Bump.sh](https://bump.sh/allratestoday/doc/allratestoday-api) — also on [SwaggerHub](https://app.swaggerhub.com/apis-docs/allratestoday/allratestoday-exchange-rate-central-bank-rates-api/2.2.0)
- [GitHub](https://github.com/AllRates-Today/bou-exchange-rate)

## 📜 License

MIT
