# Apify data tools MCP: Threads, Yelp, transcripts, Google Trends, Airbnb, Jumia

Give Claude, Cursor, VS Code or any MCP client live web data tools. One remote MCP server, no install:
it runs the [headply Apify Actors](https://apify.com/headply) as tools through Apify's hosted MCP server.

| Tool | What it returns | |
|---|---|---|
| `headply/threads-scraper` | Threads posts, full reply trees, profiles and keyword search | [Store page](https://apify.com/headply/threads-scraper) |
| `headply/threads-keyword-search-scraper` | Search Threads by keyword; posts with engagement | [Store page](https://apify.com/headply/threads-keyword-search-scraper) |
| `headply/yelp-scraper` | Every Yelp business in a city with phone, website, hours and reviews | [Store page](https://apify.com/headply/yelp-scraper) |
| `headply/yelp-reviews-scraper` | All Yelp reviews for a business, owner replies, only-new mode | [Store page](https://apify.com/headply/yelp-reviews-scraper) |
| `headply/tiktok-youtube-transcript-scraper` | Transcripts for TikTok/YouTube videos, channels, playlists | [Store page](https://apify.com/headply/tiktok-youtube-transcript-scraper) |
| `headply/google-trends-scraper` | Google Trends: many keywords on one scale, daily history, regions | [Store page](https://apify.com/headply/google-trends-scraper) |
| `headply/google-trends-trending-now` | Every Google Trends Trending Now search for any country | [Store page](https://apify.com/headply/google-trends-trending-now) |
| `headply/airbnb-occupancy-revenue-estimator` | Airbnb occupancy, ADR, RevPAR and revenue by market | [Store page](https://apify.com/headply/airbnb-occupancy-revenue-estimator) |
| `headply/airbnb-vrbo-scraper` | Airbnb + Vrbo listings with calendars, occupancy and revenue | [Store page](https://apify.com/headply/airbnb-vrbo-scraper) |
| `headply/jumia-price-intelligence` | Jumia prices and sellers in 8 African countries | [Store page](https://apify.com/headply/jumia-price-intelligence) |

Ask things like *"Compare ChatGPT, Claude and Gemini on Google Trends over 5 years"*,
*"List every plumber in Austin on Yelp with phone numbers"*, *"Transcribe this YouTube channel's last
10 videos"*, *"What is the Airbnb occupancy rate in Gatlinburg?"* or *"What are people on Threads saying
about our brand today?"*

## Connect

Remote server URL:

```
https://mcp.apify.com/?tools=headply/threads-scraper,headply/threads-keyword-search-scraper,headply/yelp-scraper,headply/yelp-reviews-scraper,headply/tiktok-youtube-transcript-scraper,headply/google-trends-scraper,headply/google-trends-trending-now,headply/airbnb-occupancy-revenue-estimator,headply/airbnb-vrbo-scraper,headply/jumia-price-intelligence
```

**Claude Desktop / Claude.ai** (Settings -> Connectors -> Add custom connector): paste the URL above; sign in
to Apify when asked (free account includes monthly credit).

**Cursor** (`~/.cursor/mcp.json`) or **VS Code** (`MCP: Open User Configuration`):

```json
{
  "mcpServers": {
    "headply-data-tools": {
      "url": "https://mcp.apify.com/?tools=headply/threads-scraper,headply/threads-keyword-search-scraper,headply/yelp-scraper,headply/yelp-reviews-scraper,headply/tiktok-youtube-transcript-scraper,headply/google-trends-scraper,headply/google-trends-trending-now,headply/airbnb-occupancy-revenue-estimator,headply/airbnb-vrbo-scraper,headply/jumia-price-intelligence",
      "headers": { "Authorization": "Bearer <YOUR_APIFY_TOKEN>" }
    }
  }
}
```

Get a token at https://console.apify.com/settings/integrations. Want only one tool? Use
`https://mcp.apify.com/?tools=headply/yelp-scraper` (any single tool id from the table).

## Pricing

Pay per result, charged by Apify: Threads $1.80 / 1,000 posts, Yelp $3 / 1,000 businesses and $0.30 / 1,000
reviews, transcripts $5 / 1,000 videos, Google Trends $3 / 1,000 keyword series, Airbnb $4 / 1,000 listings
(+$6 with occupancy), Jumia $2.50 / 1,000 products. Cheaper on paid Apify plans.

## Command-line versions

[google-trends-bulk-compare](https://github.com/headply/google-trends-bulk-compare) ·
[youtube-tiktok-transcripts](https://github.com/headply/youtube-tiktok-transcripts) ·
[airbnb-occupancy-calculator](https://github.com/headply/airbnb-occupancy-calculator) ·
[yelp-lead-list](https://github.com/headply/yelp-lead-list) ·
[threads-brand-monitor](https://github.com/headply/threads-brand-monitor) ·
[jumia-price-tracker](https://github.com/headply/jumia-price-tracker)

MIT licensed.
