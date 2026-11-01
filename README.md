# Bluesky Scraper – Posts, Profiles & Search

Bluesky scraper for posts, hashtags, user feeds and profiles. Search Bluesky by keyword via the official public AT Protocol API. No login, no cookies. Export to CSV, JSON or Excel. Incremental monitoring.

**[Run it on Apify →](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=hero)** (pay per result, free Apify account to start)


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

1. Create a free account at [apify.com](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=quickstart) and copy your API token.
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

## FAQ

**Do I need a Bluesky account?**
No. The actor uses Bluesky's public API and never logs in.

**Can I search hashtags?**
Yes, put `#tag` in the queries.

**How many posts per search?**
Bluesky's public API returns roughly the first 100 posts per query to anonymous clients. For more, run several narrower queries or split the time range with `since`/`until` (and use incremental mode on a schedule).

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/bluesky-scraper` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=pricing) for current pay-per-result pricing.

## Sample data

Browse real sample rows, download a free CSV sample and see ready-made feeds at [rowsift.co.uk](https://rowsift.co.uk/feeds/bluesky-scraper/?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=sample-data).

## More data actors

- [UK Companies House Scraper – Companies & Directors](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [Hacker News Scraper – Stories, Comments & Jobs](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [npm Package Scraper – Downloads & Dependencies](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [SEC EDGAR Scraper – 10-K, 10-Q & 8-K Filings](https://apify.com/devteamdrew/sec-edgar-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [arXiv Scraper – Paper Search, Abstracts & Authors](https://apify.com/devteamdrew/arxiv-scraper?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [UK Public Tenders Scraper – Contracts Finder & Find a Tender](https://apify.com/devteamdrew/uk-public-tenders?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)
- [CQC Care Homes & Providers Scraper – UK Care Directory Leads](https://apify.com/devteamdrew/uk-cqc-care-providers?utm_source=github&utm_medium=readme&utm_campaign=bluesky-scraper&utm_content=more)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.
