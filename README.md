# The Philadelphia Inquirer

The Philadelphia Inquirer is the largest daily newspaper in Pennsylvania, founded in 1829 and owned since 2016 by the nonprofit Lenfest Institute for Journalism. Inquirer.com publishes Philadelphia, regional, national, and world news, sports, business, opinion, arts, food, and obituaries, and the paper has won 20 Pulitzer Prizes (as of 2020).

The Inquirer does **not** operate a public commercial developer program. There is no developer portal, no API console, no API keys, and no published pricing for programmatic access. The programmatic surfaces that exist are:

- **RSS feeds** (Arc XP outbound feeds) — a site-wide feed plus per-category feeds for news, sports, business, opinion, entertainment, food, life, health, and real-estate. Rebuilt approximately hourly.
- **XML sitemaps** (Arc XP outbound feeds) — a sitemap index of roughly two years of daily child sitemaps, a Google News sitemap, an author sitemap, and a restaurant sitemap.
- **Dewey MCP** — an open-source FastMCP server (`phillymedia/dewey-mcp`) that exposes a single `search_archive` tool over the Inquirer archive indexed in Azure AI Search. Self-hosted; emerged from a Lenfest Institute fellowship supported by Microsoft and OpenAI.

The Inquirer's `phillymedia` GitHub organization also publishes the Dewey AI librarian (`dewey-ai`), Vestapol (`vestapol`, a Python package that registers external SQL tables over web data), the public Data Engineering Handbook, and a number of dbt/Airflow integrations. The `inquirer-api.github.io` repo is a Swagger UI shell that has never been wired to a spec.

## Repository contents

| File / folder | What it is |
|---|---|
| [`apis.yml`](./apis.yml) | apis.yml index of the three programmatic surfaces and the related GitHub repos, mobile apps, social, and parent organization. |
| [`openapi/`](./openapi) | OpenAPI 3.1 specs for the RSS feeds, the sitemaps, and the Dewey MCP HTTP envelope. |
| [`json-schema/`](./json-schema) | JSON Schemas for RSS items, sitemap URL entries, and Dewey search results. |
| [`json-structure/`](./json-structure) | JSON Structure representation of the RSS item. |
| [`json-ld/`](./json-ld) | JSON-LD context aligning Inquirer surfaces with schema.org NewsArticle / NewsMediaOrganization, sitemap, sitemap-news, and rss vocabularies. |
| [`examples/`](./examples) | Example request/response payloads for the RSS, sitemap, and Dewey MCP operations. |
| [`capabilities/`](./capabilities) | Naftiko-style capabilities: RSS aggregation, sitemap crawl, Dewey archive search. |
| [`rules/`](./rules) | Spectral ruleset enforcing Title Case summaries, camelCase operationIds, required `outputType=xml`, and tag presence. |
| [`vocabulary/`](./vocabulary) | Domain vocabulary covering the Inquirer's ownership, sections, Arc XP, RSS/sitemap surfaces, Dewey, and `phillymedia` projects. |
| [`plans/`](./plans) | Plans and pricing: developer plane is free and unmetered; consumer subscriptions are the actual revenue surface. |
| [`rate-limits/`](./rate-limits) | Rate-limit profile: nothing documented for RSS or sitemaps; robots.txt disallows enumerated; Dewey MCP rate limits are deployer-controlled. |
| [`finops/`](./finops) | FinOps profile: no developer billing surface; FOCUS alignment marked not applicable. |

## Documented APIs

1. **RSS Feeds** — `https://www.inquirer.com/arc/outboundfeeds/rss/` and `/category/{category}/`.
2. **Sitemaps** — sitemap index, daily URL sitemaps, Google News sitemap, author sitemap, restaurant sitemap.
3. **Dewey MCP** — open-source FastMCP server with `search_archive` tool over the Inquirer archive.

## Ownership and scale

- Founded **1829**; nonprofit owned by **The Lenfest Institute for Journalism** since 2016.
- Approximately **32,400** print and **118,000** digital subscribers (Wikipedia).
- Approximately **225** newsroom employees as of February 2021 (Wikipedia).
- **20 Pulitzer Prizes** as of 2020.
- Founding member of **Spotlight PA** (Pennsylvania investigative-journalism collaboration).

## Notable absences

- No developer portal, no OpenAPI catalog, no API keys, no commercial API tier.
- No published rate limits for RSS or sitemap consumers.
- `inquirer-api.github.io` exists but is an unconfigured Swagger UI shell.
- No public REST API for Inquirer content beyond Arc XP RSS/sitemap surfaces.
