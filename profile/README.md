<div align="center">

# Cotizave

### Exchange-Rate Data Infrastructure

Build with multi-country exchange rates, currency conversions and financial
reference data through one API.

[![npm](https://img.shields.io/npm/v/@cotizave/sdk?label=%40cotizave%2Fsdk&color=cb3837&logo=npm)](https://www.npmjs.com/package/@cotizave/sdk)
[![CI](https://github.com/cotizave/cotizave-typescript/actions/workflows/ci.yml/badge.svg)](https://github.com/cotizave/cotizave-typescript/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/cotizave/cotizave-typescript/blob/master/LICENSE)

[Documentation](https://docs.cotizave.com) · [API reference](https://docs.cotizave.com/api/v2/introduction) · [Dashboard](https://app.cotizave.com) · [Website](https://cotizave.com)

</div>

---

## What is Cotizave

Cotizave is a data platform that gives developers and businesses exchange-rate and
financial reference data through a single, typed API. Official and market rates,
conversions, historical series, bank information and calendars — for applications
across the Americas and Europe — behind one API key.

It is infrastructure, not a widget: you integrate it server-side and build pricing,
billing, analytics, remittances and reporting on top of it.

## Platform capabilities

| Capability | What it provides |
| --- | --- |
| **Exchange rates** | Official and market references per country, by canonical rate id. |
| **Currency conversion** | Single and bulk conversions, resolved on Cotizave — never computed client-side. |
| **History & statistics** | Point-in-time, daily series, raw captures, and period aggregates. |
| **Markets & banks** | Rate catalogs, spreads, best-route lookups and bank-published rates. |
| **Calendars** | Holidays and business-day math per country. |
| **Reference data** | Country, currency and issuer catalogs. |

> Coverage and available features vary by country and by plan.

## Developer tools

| Tool | Description | Install |
| --- | --- | --- |
| [**TypeScript SDK**](https://github.com/cotizave/cotizave-typescript) | Fully-typed client for the Cotizave API v2, generated from the OpenAPI contract. ESM + CommonJS, Node.js 22+. | `npm i @cotizave/sdk` |
| [**Agent Skill**](https://github.com/cotizave/agent-skills) | Official skill that guides AI coding agents (Claude, Cursor, Codex) to integrate Cotizave correctly. | `npx skills add cotizave/agent-skills` |

Additional language SDKs and integrations are planned; this list shows what is
available today.

## Quick start

```ts
import { Cotizave } from '@cotizave/sdk';

const client = new Cotizave({ apiKey: process.env.COTIZAVE_API_KEY! });

// Live rates for a country
const { rates } = await client.rates.list('AR');

// A single rate by its canonical id
const trm = await client.rates.get('CO', 'co-trm');

// A conversion — the arithmetic runs on Cotizave
const { to } = await client.convert({ from: 'USD', to: 'BRL', amount: 100 });

// A daily historical series
const series = await client.history.daily({
  country: 'CO',
  rateId: 'co-trm',
  from: '2026-09-01',
  to: '2026-09-30',
});
```

Create a free API key in the [dashboard](https://app.cotizave.com) and keep it
server-side.

## Documentation & resources

- **[Documentation](https://docs.cotizave.com)** — guides, reference and quick start
- **[API v2 reference](https://docs.cotizave.com/api/v2/introduction)** — endpoints and responses
- **[Postman collection](https://docs.cotizave.com)** — try every endpoint
- **[Dashboard](https://app.cotizave.com)** — manage API keys and usage

## Security & responsible usage

Cotizave is designed for server-side use. Keep your API key in a server
environment variable and never ship it in a browser bundle or public client. The
SDKs send the key only as a request header, enforce HTTPS, and keep money
arithmetic on the server.

Found a security issue? See the SDK's
[security policy](https://github.com/cotizave/cotizave-typescript/blob/master/SECURITY.md)
for private reporting.

## Community & contributions

- Report bugs or request features in each repository's **Issues**.
- The TypeScript SDK is open source (MIT); see its
  [contributing guide](https://github.com/cotizave/cotizave-typescript/blob/master/CONTRIBUTING.md).

---

<div align="center">

**[Get started →](https://docs.cotizave.com)**

</div>
