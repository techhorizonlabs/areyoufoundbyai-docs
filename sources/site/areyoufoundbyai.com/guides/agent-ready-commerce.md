# Source: https://areyoufoundbyai.com/guides/agent-ready-commerce

Guide · agentic commerce

# Agents are starting to buy. Can they act on your site?

The next buyers on your site aren't people, they're AI agents that navigate, compare, fill carts, apply codes and **complete purchases** on a customer's behalf. The question stops being "which AI surface am I optimising for?" and becomes **"what data can an agent access, trust, and use?"** Most sites break exactly there: the data exists, but it isn't structured, consistent or surfaced in a way software can act on. This checklist distils the current best practice, including [Stripe's technical field guide](https://stripe.com/guides/how-to-prepare-for-agentic-commerce-technical-field-guide) (March 2026), into five moves, in order.

## 1\. Be readable at all

Allow the verified agent crawlers in robots.txt, `GPTBot`, `ClaudeBot`, `Google-Extended` ([check yours free](https://areyoufoundbyai.com/tools/ai-crawler-checker)), and make sure your firewall isn't hard-blocking what robots.txt permits. Serve full HTML from the server: agents parsing prices and availability mostly don't execute JavaScript ([the raw-HTML truth](https://areyoufoundbyai.com/research/schema-ai-crawlers)). Do disallow expensive dynamic paths (internal search, cart endpoints), access for reading, not for burning your compute.

## 2\. Publish the map

An `llms.txt` at your domain root listing core collections, policies and docs ([the standard](https://llmstxt.org); stripe.com/llms.txt is a clean reference). If you publish documentation, offer Markdown twins of key pages, agents read them at a fraction of the token cost.

## 3\. Make your products machine-readable

Server-side **Product and Offer JSON-LD** with real prices and availability is the difference between an agent recommending you and an agent transacting with you, it's Level 4 on [our agent-readiness ladder](https://areyoufoundbyai.com/how-it-works). At scale, direct product feeds give agents exact, current data and eliminate hallucinated prices.

## 4\. Declare your interface, honestly

- `/.well-known/ai-plugin.json` with a _specific_ `description_for_model` ("search athletic footwear, check live size availability, get shipping estimates", not marketing copy).
- `manifest.json` with `short_name` and high-res icons, that's your identity on agent-rendered product cards.
- `openapi.yaml` if you expose an API, precise endpoints beat prose.
- A [DNS-AID record](https://areyoufoundbyai.com/guides/dns-aid) so agents can discover your entry point from DNS.

**The honesty rule, again:** only declare surfaces that exist. An ai-plugin.json describing capabilities you don't have, or an MCP record pointing at nothing, reads as broken the moment an agent probes it, worse than absence. Publish as you build, not before.

## 5\. Handle the traffic, and the payment

Detect agent user-agents at the CDN edge and serve lightweight Markdown/JSON views (Stripe cites ~90% token reduction). Cache read-heavy price/inventory endpoints with stale-while-revalidate. Rate-limit agents with `429 + Retry-After`, never silent blocks. And when you're ready to let agents pay, both major rails are live in 2026: **Stripe's** open Agentic Commerce Protocol with Shared Payment Tokens (seller-scoped, time-and-amount-bounded), and **Cloudflare's** agentic stack, the [Monetization Gateway](https://blog.cloudflare.com/monetization-gateway/) turns HTTP 402 + the open x402 protocol (now a Linux Foundation project with Coinbase) into per-request payment for any resource, Web Bot Auth verifies which agent is calling, and their [Visa and Mastercard partnership](https://blog.cloudflare.com/secure-agentic-commerce/) extends agent purchasing to card rails. If your site already sits behind Cloudflare, charging agents is becoming a settings decision, not a build. (We practise this ourselves, our scan API speaks x402.)

## Where are you today?

Every free scan measures the readable-to-actable ladder for your site, crawler access, structure, machine-readable offers, agent interface, plus whether AI engines actually name you. [Run the free scan →](https://areyoufoundbyai.com/?src=guide-agentic)