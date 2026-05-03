# Whisky Hunter

Whisky Hunter is a market research and data platform for whisky collectors, investors, traders, and enthusiasts that aggregates historical auction data from 28 online whisky auction sites into a single database. All trading volumes and winning bids are stated in GBP (£). The Whisky Hunter API provides free, public access to this data with no authentication required.

**Website:** https://whiskyhunter.net

## APIs

### Whisky Hunter API

The Whisky Hunter API provides free, public access to historical whisky auction data including aggregated platform statistics, distillery listings, and per-distillery historical auction data.

- **Documentation:** https://whiskyhunter.net/api/
- **Base URL:** https://whiskyhunter.net/api
- **Authentication:** None required
- **Live Data:** https://whiskyhunter.net/api/auctions_data/?format=json

#### Key Endpoints

| Endpoint | Description |
|---|---|
| `GET /auctions_data/` | Aggregated auction statistics across all 28 platforms |
| `GET /distilleries_info/` | List of all tracked distilleries with slugs |
| `GET /distillery_data/{slug}/` | Historical auction data for a specific distillery |

## OpenAPI Specifications

| Spec | Description |
|---|---|
| [Whisky Hunter API](openapi/whisky-hunter-openapi.yml) | OpenAPI spec for auctions data and distillery endpoints |

## Examples

| Example | Description |
|---|---|
| [Get Auctions Data](examples/whisky-hunter-get-auctions-data-example.json) | Aggregated auction statistics across platforms |
| [List Distilleries](examples/whisky-hunter-list-distilleries-example.json) | All tracked distilleries with slugs |
| [Get Distillery Data](examples/whisky-hunter-get-distillery-data-example.json) | Historical data for The Macallan distillery |

## Spectral Rules

- [whisky-hunter-rules.yml](rules/whisky-hunter-rules.yml) — Spectral ruleset enforcing Whisky Hunter API conventions

## Naftiko Capabilities

### Workflow Capabilities

| Capability | Description |
|---|---|
| [whisky-market-intelligence.yaml](capabilities/whisky-market-intelligence.yaml) | Whisky market research — auctions, distilleries, price tracking (3 tools) |

### Shared API Definitions

| File | API |
|---|---|
| [shared/whisky-hunter-api.yaml](capabilities/shared/whisky-hunter-api.yaml) | Whisky Hunter public API |

## JSON Schemas

| Schema | Description |
|---|---|
| [Auction Data Point](json-schema/whisky-hunter-auction-data-schema.json) | Aggregated auction statistics per platform per date |
| [Distillery](json-schema/whisky-hunter-distillery-schema.json) | Distillery record with name and slug |

## JSON Structures

| Structure | Description |
|---|---|
| [Auction Data Point](json-structure/whisky-hunter-auction-data-structure.json) | Auction data point structure |
| [Distillery](json-structure/whisky-hunter-distillery-structure.json) | Distillery structure |

## JSON-LD Context

- [whisky-hunter-context.jsonld](json-ld/whisky-hunter-context.jsonld) — Linked data context mapping whisky auction vocabulary to schema.org

## Vocabulary

- [whisky-hunter-vocabulary.yml](vocabulary/whisky-hunter-vocabulary.yml) — Domain vocabulary for whisky auctions, market data, distilleries, and spirits categories

## Common Resources

| Type | URL |
|---|---|
| Website | https://whiskyhunter.net |
| API | https://whiskyhunter.net/api/ |

**Maintainer:** Kin Lane (kin@apievangelist.com)
