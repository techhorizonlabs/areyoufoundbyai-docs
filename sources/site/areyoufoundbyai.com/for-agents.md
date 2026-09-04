# Source: https://areyoufoundbyai.com/for-agents

Found by AI for agents

# Fifteen tools over what AI actually says about a business.

Add one MCP server and your agent can read the measurements: the verbatim answer each of seven engines gave to a buyer's question, the web searches it ran before answering, which competitor it named instead, and what to change. Try it against the public demo server before you pay anything.

```
claude mcp add --transport http found-by-ai https://areyoufoundbyai.com/mcp/demo
```

That is the live demo server, no key and no signup. A paid monitor swaps `demo` for its own token and the same fifteen tools answer about that business, plus `request_rescan` to re-measure on demand.

If you would rather not carry a credential in a URL, and you should not want to, the same token works as a header against a static endpoint. URLs end up in server logs, proxies and browser history; headers do not.

```
curl -X POST https://areyoufoundbyai.com/mcp \
  -H "authorization: Bearer <your-token>" \
  -H "content-type: application/json" \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/list"}'
```

`x-api-key` works too. Both forms reach the same tools, and the path form keeps working for anything already pointed at it.

What an agent sees

## This site, as your agent receives it.

We score other sites on agent-readiness, so here is our own front door: the markdown the homepage serves when an agent asks for it, the llms.txt, the skill card, the tool list. Typed from the live endpoints, not a mock.

```
AREYOUFOUNDBYAI.COM · AGENT SESSION
$ GET /   accept: text/markdown
  200 text/markdown · the site itself, as markdown
$ GET /llms.txt
  200 text/plain
  > Are you found by AI? (short form "Found by AI") is
  > the free AI-visibility scanner built and operated
  > by Tech Horizon Labs at areyoufoundbyai.com.
$ GET /.well-known/agent-skills
  200 · skill: ai-visibility-scan · free, no auth, 60s
$ POST /mcp/demo   tools/list
  200 · 15 tools: get_answers, get_rivals, get_visibility,
    get_fix_plan, get_benchmark, request_rescan, ...
$ POST /api/scan {"url":"yoursite.com"}
  200 json · one live measurement, about 60 seconds
ready.
```

Every request above answers right now on this domain; the llms.txt lines are re-fetched live when this section scrolls into view. The scan checks the same surfaces on yours.

What comes back

## A receipt, not a score.

Ask your agent to call `get_answers` and it gets the sentence the engine gave the buyer, with the model, the date, whether it came from live web search or model memory, how many samples named the business, the competitors in that answer, and the searches the engine ran first. Nothing is summarised away.

```
> which engines named this business, and who did they name instead?

  ## best mortgage broker Brisbane southside
  named you on 0 of 7 engines
  Searches the engines ran first: ChatGPT: "mortgage broker Brisbane south",
  Claude: "best mortgage broker Brisbane 2026"

  ### Google AI Overviews (google-serp-aio) - did not name you
  - named in 0/3 samples - live web search - 2026-08-09
  > "...consider speaking with local experts who know the market:
     Robertson Mortgage Broking..."
```

Every rival name in that output came out of an engine's own answer. We treat it as data about the market, and so should your agent.

The tools

## Fourteen read, one action.

| get\_answers | the verbatim answer each engine gave to each tracked question, with the fan-out searches it ran first |
| --- | --- |
| get\_cited\_queries | reverse lookup: name a competitor, get the questions where the engines named them |
| get\_visibility | current and previous AI Visibility and Readiness scores, with the subscores |
| get\_question\_trajectories | every tracked buyer question and how many engines named you on each measured day |
| get\_rivals | the competitor names the engines gave instead of you, latest measure and recurring |
| get\_share\_of\_voice | your share of AI answer mentions against the rivals the engines name |
| get\_citation\_sources | the domains the engines cite in your category, and whether you appear on them |
| get\_fix\_plan | the prioritised changes that move you, blockers first |
| get\_mentions | new pages on the web that mention you, from the daily sweep |
| get\_benchmark | your rank and percentile against every measured business in your category |
| get\_ai\_traffic | visitors the engines actually sent to your site, by engine and week |
| get\_agent\_view | what a headless agent browser can actually read on your site |
| get\_personas | the buyer personas behind your tracked questions |
| get\_post\_brief | this week's measured data assembled for drafting |
| request\_rescan | the one action: queue a fresh measurement, capped by plan |

A fleet token answers across a whole client network with five more: `get_network_summary`, `get_site_scores`, `get_site_mentions`, `get_site_fix_plan`, `get_site_post_brief`. Per-staff keys are scoped and revocable.

Agent-readiness

## Check, fix, verify. With tools, not promises.

The scan grades every site on an agent-readiness ladder, level 0 to 5, from merely crawlable to fully agent-operable. The loop that climbs it is three of the tools above, so your agent can run the whole thing without a human in the middle.

Step 01 · Check

### Read the site the way an agent does.

What a headless agent browser can actually read on the site, plus the 30-plus readiness signals behind the score: crawler access, llms.txt, schema, markdown, skill cards.

[get\_agent\_view →](https://areyoufoundbyai.com/for-agents#tools 'See every tool')

Step 02 · Fix

### Take the ordered plan, not a lecture.

The prioritised changes that move the score, blockers first, in plain language with the evidence attached. Paste-ready where a file is the fix.

[get\_fix\_plan →](https://areyoufoundbyai.com/for-agents#tools 'See every tool')

Step 03 · Verify

### Re-measure. The score is the receipt.

Queue a fresh measurement, capped by plan. The next read shows what actually moved, engine by engine, question by question.

[request\_rescan →](https://areyoufoundbyai.com/for-agents#tools 'See every tool')

Other ways in

## If MCP is not your shape.

| POST /api/scan | free, no auth, one measurement of a domain as JSON |
| --- | --- |
| POST /api/agent/scan | a deep measurement paid per call over x402, no account and no API key |
| GET /api/agent/sov | share of voice for a keyword, x402 |
| /monitor/<token>.json | the whole console as one JSON document, with a read-order hint for agents |
| /monitor/<token>/context.md | the same measurements as markdown, sized to paste into a context window |
| /.well-known/agent-skills | an agent skill card describing the visibility scan |
| /llms.txt, /llms-full.txt | the site itself, written for a machine |

x402 is the part no one else in this category does: your agent pays per call in USDC on Base, with no signup, no key and no subscription. That matters when the thing doing the buying is software.

The method

## You can argue with it.

Seven engines, questions written from the business's own site rather than a keyword tool, chat engines asked up to three times and majority voted, every answer stored word for word with its model and date. Scoring, evals and the audit suite are open source at [github.com/techhorizonlabs/thl-open](https://github.com/techhorizonlabs/thl-open).

3,800+ businesses measured so far. Across the 1,309 in the public index, 28% are named by no engine at all.

Price

## US$79 a month, per site.

The tools are included, not an add-on and not metered in credits. That covers a weekly re-measure of twenty five buyer questions across all seven engines, the daily mention sweep, and everything above. The Fleet plan runs a whole client network from one console at US$149 a month plus US$39 a site.

[What is in each plan](https://areyoufoundbyai.com/pricing) · [measure a domain free, no signup](https://areyoufoundbyai.com/)