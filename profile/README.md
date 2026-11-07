<div align="center">

# Cotizave

### Exchange-rate data for developers and businesses

Multi-country currency references, conversions, historical series, bank rates and
calendars — across the Americas and Europe, behind a single API key.

[![Docs](https://img.shields.io/badge/docs-docs.cotizave.com-2563eb)](https://docs.cotizave.com)
[![Website](https://img.shields.io/badge/web-cotizave.com-0ea5e9)](https://cotizave.com)
[![API v2](https://img.shields.io/badge/API-v2-16a34a)](https://docs.cotizave.com/api/v2/introduction)

[**Documentation**](https://docs.cotizave.com) · [**API reference**](https://docs.cotizave.com/api/v2/introduction) · [**Get an API key**](https://cotizave.com)

</div>

---

## 🧰 Official tools

| | Tool | What it is | Install |
| :-: | --- | --- | --- |
| 🟦 | [**TypeScript SDK**](https://github.com/cotizave/cotizave-typescript) <br/> [![npm](https://img.shields.io/npm/v/@cotizave/sdk?color=cb3837&logo=npm)](https://www.npmjs.com/package/@cotizave/sdk) [![CI](https://github.com/cotizave/cotizave-typescript/actions/workflows/ci.yml/badge.svg)](https://github.com/cotizave/cotizave-typescript/actions/workflows/ci.yml) | Fully-typed client for the Cotizave API v2 — rates, conversions, history, markets and calendars. Zero config beyond your API key. | `npm i @cotizave/sdk` |
| 🤖 | [**Agent Skill**](https://github.com/cotizave/agent-skills) | Official skill that teaches a coding agent (Claude, Cursor, Codex…) to integrate Cotizave correctly — the right rate IDs, server-side keys, plan-aware fields. | `npx skills add cotizave/agent-skills` |
| 📮 | [**Postman collection**](https://docs.cotizave.com) | Every v2 endpoint, ready to try from Postman. | [Open in docs](https://docs.cotizave.com) |

## ⚡ Quick start

```ts
import { Cotizave } from '@cotizave/sdk';

const client = new Cotizave({ apiKey: process.env.COTIZAVE_API_KEY! });

// Live rates for a country
const { rates } = await client.rates.list('AR');

// A conversion — the math runs on Cotizave, not in your code
const conversion = await client.convert({ from: 'USD', to: 'BRL', amount: 100 });

// Historical series
const series = await client.history.daily({
  country: 'CO',
  rateId: 'co-trm',
  from: '2026-09-01',
  to: '2026-09-30',
});
```

Grab a free API key at [cotizave.com](https://cotizave.com) and keep it server-side.

## ✨ Why Cotizave

- 🌎 **Multi-country** — official and market rates across the Americas and Europe, one API.
- 🧩 **Typed & generated** — SDKs built from the OpenAPI v2 contract, so they never drift.
- 🔐 **Secure by design** — server-side keys, no money math on the client, rate-limit aware.
- 🤝 **Agent-ready** — a first-class skill so AI coding agents integrate it the right way.

## 📚 Learn more

**[Documentation](https://docs.cotizave.com)** — **[API v2 reference](https://docs.cotizave.com/api/v2/introduction)** — **[Website](https://cotizave.com)**

<!--
  This page lives in cotizave/.github → profile/README.md.
  Add rows to "Official tools" as more ship (MCP server, Python/Go SDKs, data feeds).
-->
