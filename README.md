# Bluesky Scraper & API – Posts, Profiles & Search

Scrape Bluesky posts by keyword or hashtag, user feeds and profiles via the official public AT Protocol API. No login, no cookies. LLM-ready output, incremental monitoring, pay per result.

**[Run it on Apify →](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper)** (pay per result, free Apify account to start)


**Bluesky Scraper** by Moxie: fast, reliable and polite, built on official/public data sources.

## What can it do?

- Brand and keyword monitoring on Bluesky (schedule with incremental mode)
- Social listening and sentiment datasets for research
- Finding creators and leads by searching profiles
- Feeding fresh Bluesky posts into LLM agents and RAG pipelines

## Data source

Bluesky's official public AppView API (`api.bsky.app`, AT Protocol). Public data only; no login.

## Features

- **Pay only for results** (pay-per-event pricing, no monthly rental)
- **Incremental mode**: scheduled runs return only items you haven't received before
- **LLM-ready output**: optional compact Markdown per item for RAG / AI agents
- **Polite rate limiting** with automatic retries and backoff
- Clean, flat JSON you can export as CSV, Excel, JSON or via API


## Quick start

1. Create a free account at [apify.com](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper) and copy your API token.
2. `export APIFY_TOKEN=...`
3. Run one of the examples:

```bash
bash examples/run.sh          # curl
node examples/run.js          # JavaScript (apify-client)
python examples/run.py        # Python (apify-client)
```

Example input ([examples/input.json](examples/input.json)):

```json
{
  "mode": "searchPosts",
  "queries": [
    "web scraping"
  ],
  "maxItems": 20,
  "outputFormat": "both"
}
```

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/bluesky-scraper` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper) for current pay-per-result pricing.

## More data actors

- [Companies House Scraper – UK Company Data, Directors & Filings](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper)
- [Hacker News Scraper – Stories, Comments & Who Is Hiring Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper)
- [npm Scraper – Package Downloads, Dependencies & Maintainers](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.
