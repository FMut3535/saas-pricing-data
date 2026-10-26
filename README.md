---

# Verified SaaS Pricing

Starting prices, plan tables and dated price changes of 700+ SaaS tools, each checked against the vendor's own pricing page, plus a benchmark of how accurately AI assistants recall those prices. Maintained by [Happy Valley](https://happyvalley.dev), an independent SaaS directory. Updated monthly.

## Files

| File | Rows | What it holds |
| --- | --- | --- |
| `saas_tools_prices.csv` | 739 | One row per tool: slug, name, website, pricing URL, pricing model (free, freemium, paid, open source), lowest paid price in USD per month, the date that price was checked, primary category, profile URL. |
| `saas_pricing_plans.csv` | 2,721 | Every plan of every checked tool, as shown on the vendor's pricing page: plan name, price string, billing period, note, check date. |
| `saas_price_changes.csv` | 96 | Dated, sourced price and plan changes (2023 to 2026): tool, date, whether the date is effective or announced, kind (increase, decrease, plan-change, free-plan, sunset), headline, details, from/to USD where known, source URLs, check date. |
| `ai_saas_price_accuracy.csv` | 40 | October 2026 test: ChatGPT, Gemini, Perplexity and Claude were asked the cheapest paid monthly price of 40 well-known tools; each answer is graded against the vendor page (correct within 5%, close within 20%, wrongPlan when it equals another plan's price, wrong, none). |

## Method

- `starting_price_usd` is the cheapest paid plan in US dollars per month; plans sold only annually are shown as their monthly equivalent. Free plans and trials are excluded. Some prices are per user and some are flat; see the plans file.
- `price_checked_on` is the day the price was compared with the vendor's own pricing page. Rows without it were not verified and have no starting price.
- Price changes include only what the linked sources state; every entry has at least one source that was opened and read.
- The accuracy test used one prompt per assistant, one attempt, no follow-up, on 2026-10-26. Full write-up: https://happyvalley.dev/reports/ai-saas-price-accuracy

## Live versions

- Price changes log: https://happyvalley.dev/price-changes
- Biggest increases: https://happyvalley.dev/reports/biggest-saas-price-increases
- Cheapest by category: https://happyvalley.dev/reports/cheapest-saas-by-category
- Machine-readable: https://happyvalley.dev/llms.txt

## License and citation

CC BY 4.0. Cite as "Happy Valley, Verified SaaS Pricing, https://happyvalley.dev". Corrections: hello@happyvalley.dev
