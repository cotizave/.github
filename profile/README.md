<div align="center">

# Cotizave

### Exchange-Rate Data Infrastructure

Build with multi-country exchange rates, currency conversions and financial
reference data through one API.

[![npm](https://img.shields.io/npm/v/@cotizave/sdk?label=%40cotizave%2Fsdk&color=cb3837&logo=npm)](https://www.npmjs.com/package/@cotizave/sdk)
[![CI](https://github.com/cotizave/cotizave-typescript/actions/workflows/ci.yml/badge.svg)](https://github.com/cotizave/cotizave-typescript/actions/workflows/ci.yml)
[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/cotizave/cotizave-typescript/blob/master/LICENSE)

[API & docs hub](https://github.com/cotizave/exchange-rates-api) · [Documentation](https://docs.cotizave.com) · [API reference](https://docs.cotizave.com/api/v2/introduction) · [Dashboard](https://app.cotizave.com) · [Website](https://global.cotizave.com)

</div>

---

## What is Cotizave

Cotizave is a data platform that gives developers and businesses exchange-rate and
financial reference data through a single, typed API — official and market rates,
conversions, historical series, bank information and calendars for 22 countries
across Latin America, North America and Europe, behind one API key.

It is infrastructure, not a widget: you integrate it server-side and build pricing,
billing, analytics, remittances and reporting on top of it.

## Where to start

| | Description | |
| --- | --- | --- |
| [**Exchange Rates API**](https://github.com/cotizave/exchange-rates-api) | The hub: quick start, endpoints, the OpenAPI spec and a Postman collection. **Start here.** | [Browse →](https://github.com/cotizave/exchange-rates-api) |
| [**TypeScript / JavaScript SDK**](https://github.com/cotizave/cotizave-typescript) | Fully-typed client for the API v2. ESM + CommonJS, Node.js 22+. | `npm i @cotizave/sdk` |
| [**Python SDK**](https://github.com/cotizave/cotizave-python) | Fully-typed client for the API v2. Python 3.10+. | `pip install cotizave` |
| [**Agent Skill**](https://github.com/cotizave/agent-skills) | Guides AI coding agents (Claude, Cursor, Codex) to integrate Cotizave correctly. | `npx skills add cotizave/agent-skills` |

Additional language SDKs are planned; this list shows what is available today.

## Documentation & resources

- **[Documentation](https://docs.cotizave.com)** — guides, reference and quick start
- **[API v2 reference](https://docs.cotizave.com/api/v2/introduction)** — endpoints and responses
- **[API & docs hub](https://github.com/cotizave/exchange-rates-api)** — OpenAPI spec, Postman and examples
- **[Dashboard](https://app.cotizave.com)** — manage API keys and usage

## Security & responsible usage

Cotizave is designed for server-side use. Keep your API key in a server environment
variable and never ship it in a browser bundle or public client. The SDKs send the
key only as a request header, enforce HTTPS, and keep money arithmetic on the server.

Found a security issue? See the SDK's
[security policy](https://github.com/cotizave/cotizave-typescript/blob/master/SECURITY.md)
for private reporting.

## Community & contributions

- Report bugs or request features in each repository's **Issues**.
- The TypeScript SDK is open source (MIT); see its
  [contributing guide](https://github.com/cotizave/cotizave-typescript/blob/master/CONTRIBUTING.md).

---

<div align="center">

**[Get started →](https://github.com/cotizave/exchange-rates-api)**

</div>
