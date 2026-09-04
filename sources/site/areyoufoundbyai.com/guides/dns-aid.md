# Source: https://areyoufoundbyai.com/guides/dns-aid

Guide · agent discovery

# DNS-AID: one DNS record that makes you discoverable to AI agents

The next wave after AI search is AI **agents**: software that researches, books and buys _for_ people. Before an agent can use your site, it has to find your machine entry point. **DNS-AID** (Agent Interface Discovery, IETF draft) answers that with the system that already runs the internet's discovery: DNS. One record at `_index._agents.yourdomain.com`, built on the standard HTTPS/SVCB record type (RFC 9460), tells agents where to start, before they crawl a single page.

It takes about five minutes, costs nothing, and agent-readiness scanners already check for it. Almost nobody has it yet, which is exactly why it's worth doing now.

## The record

| Type | **HTTPS** |
| --- | --- |
| Name | **\_index.\_agents** |
| TTL | Auto |
| Priority | 1 |
| Target | **yourdomain.com** (your apex domain) |
| Value | **alpn="h2"** |

## Add it in Cloudflare (5 minutes)

1. Log in at dash.cloudflare.com → select your domain → **DNS → Records → Add record**.
2. Type: **HTTPS**. Name: `_index._agents` (Cloudflare appends your domain automatically). TTL: Auto.
3. Priority: **1**. Target: your apex domain (e.g. `yourdomain.com`). Value: `alpn="h2"`.
4. Save. The record is usually live worldwide within minutes.
5. Bonus: under **DNS → Settings**, enable **DNSSEC**: resolvers can then cryptographically verify your record is genuine.

## On any other DNS host

Same four values. Look for record type **HTTPS** (some panels label it **SVCB** or "type 65"), Route 53, Google Cloud DNS and most modern hosts support it. If your panel doesn't offer the type at all, you can move just your DNS (not your hosting or your registrar) to a free Cloudflare plan and add it there.

## Verify it's live

Fastest: our free [DNS-AID checker](https://areyoufoundbyai.com/tools/dns-aid-checker), it also shows whether the record is DNSSEC-authenticated. Or from any terminal:

`curl -s -H "accept: application/dns-json" "https://cloudflare-dns.com/dns-query?name=_index._agents.yourdomain.com&type=HTTPS"`

A JSON answer containing a type-65 record means you're live. Note: older versions of `dig` can't render type-65 records, a blank `dig +short` does NOT mean the record is missing; trust the DNS-over-HTTPS check above.

## The honesty rules

**Only publish entry points that exist.** The `_index` record is the generic entrypoint, it points at your real website, so every business can publish it truthfully today. The draft also defines service-specific names (`_mcp._agents`, `_a2a._agents`) for sites that actually run an MCP server or agent-to-agent endpoint. Don't publish those until you genuinely operate the surface behind them: scanners resolve and probe these records, and a record pointing at nothing reads as broken, worse than no record at all.

## Where this is heading

DNS-AID is an IETF Internet-Draft ([draft-mozleywilliams-dnsop-dnsaid](https://datatracker.ietf.org/doc/draft-mozleywilliams-dnsop-dnsaid/)) building on the HTTPS/SVCB record standard ([RFC 9460](https://www.rfc-editor.org/rfc/rfc9460)). Drafts evolve, but the record type is standard DNS, the cost is one entry, and readiness scanners (including [our scan](https://areyoufoundbyai.com/)) already measure it. Early signals like this are how you show up prepared when the agent wave arrives.

## Check where you stand

[Check your domain's DNS-AID record →](https://areyoufoundbyai.com/tools/dns-aid-checker) 
Or run the [full free scan](https://areyoufoundbyai.com/?src=guide-dnsaid), DNS discovery is one of 30+ signals behind your AI-visibility score, measured from live engine answers.