# The Philadelphia Inquirer (philadelphia-inquirer)

The Philadelphia Inquirer is the largest newspaper in Pennsylvania, owned by the nonprofit Lenfest Institute for Journalism. Inquirer.com publishes Philadelphia, regional, national, and world news, sports, business, opinion, arts, food, and obituaries. The Inquirer does not operate a public commercial developer program. Programmatic surfaces are limited to Arc XP-generated RSS feeds, news sitemaps, and a small set of open-source repositories from its `phillymedia` GitHub organization, including the `dewey-mcp` Model Context Protocol server that wraps an Azure AI Search index of the Inquirer archive.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/philadelphia-inquirer/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/philadelphia-inquirer/refs/heads/main/apis.yml)

## Scope

- **Type:** Index

## Tags

- News
- News Media
- Newspaper
- Journalism
- Philadelphia
- Pennsylvania
- Local News
- RSS
- Sitemap
- Arc Publishing
- MCP

## Timestamps

- **Created:** 2026-05-23
- **Modified:** 2026-05-23

## APIs

### The Philadelphia Inquirer RSS Feeds

Public RSS 2.0 feeds served from Arc XP's outbound feeds for Inquirer.com. A site-wide feed and per-category feeds expose article titles, links, descriptions, publication dates, and encoded article HTML for syndication and aggregation. Feeds are rebuilt hourly.

- **Human URL:** [https://www.inquirer.com](https://www.inquirer.com)
- **Base URL:** `https://www.inquirer.com/arc/outboundfeeds/rss`

#### Tags

- RSS
- News
- Syndication
- Arc Publishing

#### Properties

- [OpenAPI](openapi/rss-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/rss.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/rss.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.inquirer.com)

### The Philadelphia Inquirer Sitemaps

XML sitemaps and a Google News sitemap published by Arc XP. The sitemap index lists daily child sitemaps spanning roughly two years of inquirer.com URLs, with per-URL last-modified, change frequency, priority, and image metadata. A dedicated Google News sitemap exposes the most recent articles using the sitemap-news namespace.

- **Human URL:** [https://www.inquirer.com/robots.txt](https://www.inquirer.com/robots.txt)
- **Base URL:** `https://www.inquirer.com/arc/outboundfeeds`

#### Tags

- Sitemap
- News
- SEO
- Arc Publishing

#### Properties

- [OpenAPI](openapi/sitemaps-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/sitemaps.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/sitemaps.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Documentation](https://www.inquirer.com/robots.txt)

### Dewey MCP

Dewey MCP is a containerized FastMCP server that exposes read-only search over the Inquirer's news archive backed by Azure AI Search. It surfaces a single `search_archive` MCP tool with text query, optional date and author filters, and a configurable result limit (max 20). The server is open source under the `phillymedia/dewey-mcp` repository and is the protocol surface for the broader Dewey AI librarian project, which emerged from a Lenfest Institute fellowship supported by Microsoft and OpenAI.

- **Human URL:** [https://github.com/phillymedia/dewey-mcp](https://github.com/phillymedia/dewey-mcp)

#### Tags

- MCP
- AI
- Search
- Archive
- Azure AI Search

#### Properties

- [GitHub Repository](https://github.com/phillymedia/dewey-mcp)
- [Documentation](https://github.com/phillymedia/dewey-mcp#readme)
- [OpenAPI](openapi/dewey-mcp-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/dewey-mcp.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/dewey-mcp.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://www.inquirer.com)
- [About](https://about.inquirer.com)
- [GitHub Organization](https://github.com/phillymedia)
- [Mobile App](https://apps.apple.com/us/app/the-philadelphia-inquirer/id1495601779)
- [Mobile App](https://play.google.com/store/apps/details?id=com.philly.philly_native_android)
- [Newsletter](https://www.inquirer.com/newsletters/)
- [Subscribe](https://www.inquirer.com/subscribe/)
- [Careers](https://www.inquirer.com/careers/)
- [Parent Organization](https://www.lenfestinstitute.org)
- [Features](undefined)
- [Use Cases](undefined)
- [Integrations](undefined)
- [Customers](undefined)
- [Awards](undefined)
- [GitHub Repository](https://github.com/phillymedia/dewey-mcp)
- [GitHub Repository](https://github.com/phillymedia/dewey-ai)
- [GitHub Repository](https://github.com/phillymedia/vestapol)
- [GitHub Repository](https://github.com/phillymedia/data-engineering-handbook)
- [GitHub Repository](https://github.com/phillymedia/inquirer-api.github.io)
- [X (Twitter)](https://x.com/PhillyInquirer)
- [Facebook](https://www.facebook.com/philly.com)
- [Instagram](https://www.instagram.com/phillyinquirer/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
