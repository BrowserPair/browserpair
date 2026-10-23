# Public discovery audit — October 23, 2026

## Verified observations

- The sitemap index, all three child sitemaps, the docs sitemap, robots files, and the sampled HTML pages returned HTTP 200: 32 checked URLs in total, including 25 HTML responses.
- The public website pages checked have canonical URLs and permit indexing. The anonymous application shell has `noindex,nofollow,noarchive`, which is appropriate for the authenticated app.
- Public HTML contains meaningful text without JavaScript rendering. The homepage, how-it-works, capabilities, and pricing pages mention both ChatGPT and Claude.
- Homepage JSON-LD contains Organization, WebSite, and WebPage. It does not currently contain SoftwareApplication. This is an optional structured-data improvement, not evidence of a crawl failure.
- Website and docs robots policies permit OAI-SearchBot, Claude-SearchBot, Claude-User, and PerplexityBot while excluding specified training crawlers.
- Requests carrying OAI-SearchBot and Claude-SearchBot user agents received homepage HTTP 200. These were user-agent simulations from one environment, not requests from verified crawler IPs and not a guarantee of crawler access worldwide.
- An initial default Python user-agent request received 403 for the main robots and sitemap URLs; follow-up Mozilla and search-bot-user-agent requests succeeded. No broad firewall exception was added on this evidence.
- Cloudflare Bot Fight Mode and its broad AI-bot blocking setting were disabled at inspection. No custom firewall ruleset appeared in the returned ruleset list. This is a configuration snapshot, not a complete WAF security audit.
- Production OAuth discovery returned HTTP 200 and advertised PKCE S256, public clients, and client ID metadata documents.
- Official MCP Registry `/v0.1/servers?search=browserpair` returned `servers: []`. The metadata in this PR is a publication candidate, not a live listing.

## Prepared changes

- [Documentation PR #4](https://github.com/BrowserPair/docs/pull/4): Claude setup, comparison, session/data flow, dashboard reading workflow, and onboarding links.
- `product.json`: shared product facts and authoritative links, with the Claude guide labelled pending publication.
- `registry/server.json`: passes the official 2025-12-11 JSON schema. No application source or credentials are included.

## Remaining work

- Review and merge the documentation and metadata PRs, then verify deployment and the new docs sitemap entries.
- Authenticate the BrowserPair domain namespace and publish the registry candidate; read the resulting entry back before calling it listed.
- Update homepage Organization `sameAs` with the public organization and add accurate SoftwareApplication metadata, with validation against visible product content.
- Add links from the website to the published client and comparison guides; check the actual changed frontend before delivery under the private repository's review rules.
- Review Search Console and Bing ownership, coverage, and submitted sitemaps. These account metrics were not verified in this audit. Reuse the existing IndexNow setup for materially changed canonical URLs after publication.

Crawl access and structured data do not guarantee indexing, ranking, or AI citations. This audit records observable technical conditions rather than a visibility score.

## Publication follow-up — October 23, 2026

- Documentation PR #4 and metadata PR #1 were merged with the owner's explicit approval.
- Mintlify confirmed docs commit `140ac87b2f9ceb8543a41d486e791edb89f42722` live. All four new guide URLs returned HTTP 200 and appeared in the docs sitemap.
- Official MCP Registry publication succeeded for `com.browserpair/browserpair@1.0.0`. Both the exact-record API and search API returned the entry with `status: active` and `isLatest: true`.
- Registry authentication used a temporary BrowserPair DNS TXT proof. The generated signing key, login token, and that exact temporary record were removed after publication. No existing DNS records were changed.
- Product facts and hub README now link the live Claude guide and registry entry.
- GSC Wizard refused Search Console and Bing inspection because its trial/subscription is inactive. No search-account metrics or sitemap submissions were verified through it; no subscription was purchased.
- The registered host's read-only terminal inspection remains QUEUED with no stdout or exit status. Private website metadata/link changes and their required source validation/preview were not performed. The private application repository was not modified.
