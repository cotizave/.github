# Cotizave

**Exchange-rate data for developers and businesses** — multi-country currency
references, conversions, historical series, bank rates and calendars, behind a
single API key.

[Documentation](https://docs.cotizave.com) · [Website](https://cotizave.com) · [API v2 reference](https://docs.cotizave.com/api/v2/introduction)

## Official tools

| Tool | What it is | Install |
| --- | --- | --- |
| [**TypeScript SDK**](https://github.com/cotizave/cotizave-typescript) | Fully-typed client for the Cotizave API v2 — rates, conversions, history and more. | `npm i @cotizave/sdk` |
| [**Agent Skill**](https://github.com/cotizave/agent-skills) | Official skill that teaches a coding agent (Claude, Cursor, Codex…) to integrate Cotizave correctly. | `npx skills add cotizave/agent-skills` |

## Quick start

```ts
import { Cotizave } from '@cotizave/sdk';

const client = new Cotizave({ apiKey: process.env.COTIZAVE_API_KEY! });

const { rates } = await client.rates.list('AR');
const conversion = await client.convert({ from: 'USD', to: 'BRL', amount: 100 });
```

Get a free API key at [cotizave.com](https://cotizave.com). Keep it server-side.

<!--
  Edit this page by changing profile/README.md in the cotizave/.github repository.
  Add more SDKs (Python, Go, …), an MCP server, or data repos to the table above
  as they ship.
-->
