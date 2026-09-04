# Source: https://areyoufoundbyai.com/research/ai-visibility-market-2026

[Research](https://areyoufoundbyai.com/research) · market brief · August 2026

# AI visibility tools, mapped: who measures what, at what price

Serious money has moved into measuring whether AI recommends you. Profound closed a US$96M Series C in February 2026 at a reported valuation near a billion dollars[\[1\]](https://www.superbcrew.com/profound-raises-96-million-in-series-c-funding-round/), Peec AI raised roughly US$29M in its first sixteen months[\[2\]](https://www.rswebsols.com/news/from-0-to-200-million-in-16-months-peec-ais-ambitious-plan-to-dominate-ai-search-marketing/), and Ahrefs and Semrush both shipped AI-visibility trackers into their suites[\[3\]](https://finance.yahoo.com/news/ahrefs-launches-custom-ai-prompt-051600618.html). That capital has built real products. What it has not changed is the quiet pattern in the pricing pages: at almost every price point, you are buying a **slice** of the answer-engine board, and the rest sits behind a higher tier.

## What each published entry tier actually measures

Published pricing as read on 7 August 2026 (Lettertrace added 13 August, its Product Hunt launch day), links below so you can verify every cell at the source. Vendors change pricing; if a cell is out of date, tell us and we'll correct it.

| Tool | Entry price | Engines measured at that price | What sits behind a higher tier |
| --- | --- | --- | --- |
| Profound[\[4\]](https://thatmarketingbuddy.com/pricing/profound) | US$99/mo | ChatGPT only | Additional engines from US$399; enterprise reported at US$2,000+ |
| Peec AI[\[5\]](https://peec.ai/pricing) | ~US$95/mo | 3 of 7 engines | Claude is enterprise-only on every published tier |
| Otterly.ai[\[6\]](https://thatmarketingbuddy.com/pricing/otterly-ai) | US$29/mo | 4 engines | Gemini, Claude and AI Mode sold as add-ons |
| Surfer[\[7\]](https://www.g2.com/products/surfer-surfer/pricing) | US$49/mo | No AI tracker at this tier | The 25-prompt tracker starts at US$99/mo |
| Ahrefs Brand Radar[\[3\]](https://finance.yahoo.com/news/ahrefs-launches-custom-ai-prompt-051600618.html) | US$199/mo per platform | 1 platform per US$199 | All 6 platforms for US$699/mo, on top of a base Ahrefs plan |
| Lettertrace[\[10\]](https://github.com/letterstory/lettertrace) | US$0 + your own API keys | 4 engines on your keys: Claude, ChatGPT, Gemini + AI Overviews, Perplexity | Nothing is paywalled, the costs are in kind: you supply provider API keys, curate the prompts, pay the token bill (the maker's own estimate is ~US$3 a measurement), and host it or trust theirs. Tracking only, no fix layer. |
| **Are you found by AI?** | **US$79/mo** | **All 7 engines**: ChatGPT, Claude, Gemini, Perplexity, Grok, DeepSeek, Google AI Overviews | Nothing. One plan, the whole board, every week. |

## The free, open-source end of the market

August 2026 added a new corner to the map: **Lettertrace**[\[10\]](https://github.com/letterstory/lettertrace) launched as a fully open-source (MIT), bring-your-own-key tracker, self-hostable, with a CLI and no paid tier at all. For a developer who already holds provider API keys, that is genuinely good, and it makes something plain that pricing pages had been obscuring: **the tracking layer itself is now worth US$0**. What you are paying anyone for in this category is what sits around the tracking. Their own README says the quiet part well: "writing prompts that measure anything is the single biggest lever." A BYOK tool hands you that lever and the token bill; a service is supposed to hand you the answered question, the verified identity behind it, and the fix. Judge every tool on this page, ours included, by how much of that it actually does.

## What buyers should check, whichever tool they pick

Four questions separate measurement from theatre, and they apply to us as much as anyone. Does the tool show you the **verbatim answers** behind every score, or only charts about them? How many engines are **actually measured at your tier**, as opposed to appearing in the marketing? Is every question asked **more than once**, so a single lucky answer can't pass as a trend? And can you **re-ask the engine live** from the report, so a number can be checked the moment you doubt it? Our whole method is open source[\[8\]](https://github.com/techhorizonlabs/thl-open), because a measurement you can't inspect is a claim, and this category has enough claims.

## If you run an agency

Agencies reselling AI-visibility monitoring and remediation are charging clients US$500 to US$1,500 a month[\[9\]](https://llmpulse.ai/blog/white-label-ai-seo-software/), and agencies are already among the heaviest users of our free scan. We're designing a partner tier: white-labeled reports, a multi-client console, wholesale pricing. [Register interest](mailto:hello@techhorizonlabs.com?subject=Agency%20white-label%20interest) and shape it.

We can't outspend a billion-dollar valuation. We can out-show it: every engine, every answer kept word for word, at the price the market treats as an entry ticket. [Run the free scan](https://areyoufoundbyai.com/) and read what AI is telling your buyers today.

**Method.** Found by AI asks ChatGPT, Claude, Perplexity and Google's AI the questions real buyers ask for each category, then measures which businesses the engines actually name. Scores are 0–100 point-in-time measurements; the index re-scans and grows automatically. Businesses listed here were selected and measured by us from public directories, [scan your own site free](https://areyoufoundbyai.com/?src=benchmarks) to see where you'd rank. Queries and methodology are open: [github.com/techhorizonlabs](https://github.com/techhorizonlabs).