# Source: https://areyoufoundbyai.com/research/schema-ai-crawlers

[Research](https://areyoufoundbyai.com/research) · schema delivery

# If JavaScript puts your schema on the page, AI never sees it

Structured data only works if the crawler reading your site actually receives it. Google's crawler renders JavaScript. **The AI fleet mostly doesn't**: GPTBot, OAI-SearchBot, ClaudeBot and PerplexityBot fetch your raw HTML and move on. That one difference decides whether your schema exists, depending on _where it's added_.

## The three ways schema reaches a page

| Delivery | How it works | Google | AI crawlers |
| --- | --- | --- | --- |
| **Server HTML** (CMS, theme, SSR) | JSON-LD is in the HTML your server sends | ✓ read | **✓ read** |
| **Edge-injected** (CDN worker rewrites the response) | JSON-LD is added in transit, it IS the response HTML | ✓ read | **✓ read** |
| **Client-side JS** (tag manager, SPA, "schema tag" SaaS snippets) | a script adds JSON-LD after the page loads in a browser | usually read (rendering queue) | **✗ invisible** |

The third row is the trap. A whole category of tools sells "add schema without touching your site", a one-line script tag that injects JSON-LD client-side. The rich-results tester passes (it renders JS). Google may see it. **The crawlers behind ChatGPT, Claude and Perplexity request your raw HTML, don't execute the tag, and see a page with no schema at all.** The nuance worth knowing: Gemini benefits from Google's rendered index, so it's the exception, but you're then structured-data-visible to one AI family out of four.

## Check yourself in 60 seconds

**View source, not inspect element.** "Inspect" shows the rendered page (after JS); "view source" shows what crawlers without a browser get. Search the source for `application/ld+json`. In it → AI can read your schema. Only in "inspect" → it's JS-injected and invisible to the AI fleet.

Terminal version: `curl -s https://yoursite.com | grep -c "application/ld+json"`, zero means zero, for every crawler that doesn't run JS.

Our free scan reads your site the way AI crawlers do, raw HTML first, which is why it sometimes reports "no schema" on sites whose SEO plugin swears it's there. That disagreement isn't a bug; it's the measurement. (The same raw-first read is how we catch JavaScript-shell sites whose entire content is invisible to AI.)

## The fix, in order of preference

1) **Put it in the server HTML**: every mainstream CMS can (theme, plugin rendering server-side, or hard-coded in the template). 2) **Inject at the edge**: if the CMS is locked down, a CDN worker (e.g. Cloudflare Workers' HTMLRewriter) can add JSON-LD to the response itself: crawler-visible by construction, no CMS access needed. We build this pattern for Sprint clients on locked platforms. 3) If a client-side tag is genuinely your only option, know what it is: schema for Google's renderer, nothing for the AI fleet, and prioritise moving it server-side.

Is your schema actually reaching AI?

The free scan reads your raw HTML like the AI crawlers do and tells you what they can and can't see.

[Run the free scan →](https://areyoufoundbyai.com/?src=research-schema)

**Method.** Found by AI asks ChatGPT, Claude, Perplexity and Google's AI the questions real buyers ask for each category, then measures which businesses the engines actually name. Scores are 0–100 point-in-time measurements; the index re-scans and grows automatically. Businesses listed here were selected and measured by us from public directories, [scan your own site free](https://areyoufoundbyai.com/?src=benchmarks) to see where you'd rank. Queries and methodology are open: [github.com/techhorizonlabs](https://github.com/techhorizonlabs).