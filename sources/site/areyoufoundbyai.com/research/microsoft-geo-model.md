# Source: https://areyoufoundbyai.com/research/microsoft-geo-model

[Research](https://areyoufoundbyai.com/research) · the Microsoft model

# Microsoft just published how AI decides what to recommend. Here's the same model, measured.

In January 2026 Microsoft Advertising released ["From discovery to influence: a guide to AEO and GEO"](https://about.ads.microsoft.com/en/blog/post/january-2026/from-discovery-to-influence-a-guide-to-geo), the first official platform playbook describing, with a diagram, how an AI assistant actually chooses what to recommend. It deserves more attention than it got: it is the closest thing to a spec for AI visibility that any platform has published. We read all 16 pages and mapped their model, factor by factor, against what our scanner already measures.

## The model, in one paragraph

A buyer asks an assistant a question. The assistant draws on three inputs, the **knowledge graph** (what the model already knows about you, plus real-time web search), **page-level data** (your structure, pricing, rendered content) and **use info** (the buyer's location and affinities), then runs a **reasoning phase**: it breaks the question down and fans out its own searches, weighs freshness, text relevance, commercial signals and context, and answers with recommendations and citations. Microsoft's framing of the practical question: not "which AI am I optimising for?" but _"what data or content can this capability access and use, and how do we make that data accurate, comprehensive, and trustworthy?"_

## Their factor → our measurement

| Microsoft's model says AI weighs… | Where you see it measured |
| --- | --- |
| **"Break down and fan out queries"**: the assistant runs its own searches mid-answer | Deep reports list the exact fan-out searches each engine ran before answering, the pages those searches surface are the pages to win |
| **Freshness** | The freshness signal (visible dates, dateModified) in your readiness score, with the fix when stale |
| **Commercial signals**: machine-readable price and availability | Product/Offer schema detection, Level 4 on the agent-readiness ladder; stores on an e-commerce stack without it get the exact fix |
| **Text + contextual relevance** | The quotable-content signals: answer-shaped copy, quotations, statistics, sourced claims |
| **Knowledge graph: pre-trained knowledge**: what models already believe about you | The LLM-mentions corpus in deep reports: real model answers that name (or confuse) your brand, month by month |
| **Real-time web search** during reasoning | Our engine queries run with live web search on, and the crawler/index checks (bingbot access, IndexNow) that decide whether that search can even find you |
| **Page-level: rendered content and structure** | The raw-HTML read: JavaScript-shell detection and server-side schema checks, what the crawler actually receives, not what a browser renders |
| **Use info: location** | The suburb-by-suburb visibility map for local businesses |
| **Product feeds** pushed to platforms | The honest gap: feeds live inside Merchant Center and platform consoles, and we don't measure them today. If you run a store, maintain them, Microsoft's line is "completeness beats cleverness." |

And the line that matters most for the agent era, verbatim from page 9: **"Without your live site working properly, the sale fails even if your feed and crawled data were perfect."** An agent that can't add to cart on your real site loses the sale at the last step, which is exactly what the upper rungs of the readiness ladder (and [the agent-ready commerce checklist](https://areyoufoundbyai.com/guides/agent-ready-commerce)) exist to catch.

## What this changes

Mostly, it confirms: the model AI platforms describe internally is the one we've been measuring externally, fan-out searches, freshness, off-site trust, machine-readable commerce, working pages. If you want to know where you stand against Microsoft's own list, that's what the scan is.

Measure yourself against the model

The free scan asks the engines your buyers' questions and grades every factor above it can reach. ~60 seconds.

[Run the free scan →](https://areyoufoundbyai.com/?src=research-msgeo)

Source: Microsoft Advertising, "From discovery to influence: A guide to AEO and GEO" (January 2026; PDF at aka.ms/ads/AeoGeo), read in full July 2026; quotes verbatim. The mapping to our measurements is ours; Microsoft has no affiliation with this analysis or product.

**Method.** Found by AI asks ChatGPT, Claude, Perplexity and Google's AI the questions real buyers ask for each category, then measures which businesses the engines actually name. Scores are 0–100 point-in-time measurements; the index re-scans and grows automatically. Businesses listed here were selected and measured by us from public directories, [scan your own site free](https://areyoufoundbyai.com/?src=benchmarks) to see where you'd rank. Queries and methodology are open: [github.com/techhorizonlabs](https://github.com/techhorizonlabs).