# The Philadelphia Inquirer (philadelphia-inquirer)

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
