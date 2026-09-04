# Source: https://areyoufoundbyai.com/research/cal-com-playbook

[Research](https://areyoufoundbyai.com/research) · claim check · August 2026

# The viral Cal.com playbook, checked claim by claim

A viral thread on X says Cal.com engineered itself into being the most-recommended scheduling tool in AI answers with four moves: 47 comparison blog posts, presence in 23 niche directories competitors ignored, 45,000+ GitHub stars, and 200+ upvoted Reddit mentions. It reads like a playbook anyone could run. We verify claims for a living, so before borrowing any of it we checked every claim against a primary source and measured both brands with our own scanner. The premise came apart on the first measurement: **Calendly scored 77/100 AI visibility to Cal.com's 40**, and ChatGPT never named Cal.com once.

## Every claim, against its primary source

All checks ran on 20 August 2026. Where a source blocked us, the table says so instead of guessing.

| The thread's claim | Verdict | What the source says |
| --- | --- | --- |
| Cal.com is the most-recommended scheduling tool in AI answers | FALSE | Our measurement: Cal.com 40, Calendly 77. ChatGPT named Cal.com in 0 of 4 asks and recommended Calendly instead |
| 47 comparison blog posts | PARTLY TRUE | 32 comparison-intent pages in the English sitemap[\[1\]](https://cal.com/sitemap_en.xml): 18 head-to-head, 14 alternatives listicles. Right order of magnitude, wrong number |
| Including “cal vs savvycal” | FALSE | The string “savvycal” appears zero times in the sitemap. The named example does not exist |
| Structured data behind the answers | FALSE | Zero JSON-LD, zero microdata, zero RDFa on the homepage, the flagship comparison page and the two comparison posts we parsed. Empty sameAs |
| 23 niche directories competitors ignored | UNVERIFIED | 4 confirmed live[\[2\]](https://www.producthunt.com/products/cal-com), 7 hosts returned bot-protection, the count of 23 is uncheckable. And Calendly is on the major directories too, so “competitors ignored” is false |
| 45,000+ GitHub stars | CONFIRMED | 47,813 stars[\[3\]](https://api.github.com/repos/calcom/cal.com). Understated, and attached to a repo that is no longer the product (next section) |
| 200+ Reddit mentions, with upvotes | PARTLY TRUE | 172 unique mentions found from capped searches, so 200+ is plausible. “With upvotes” is not: median score 2.0, and 40% of mentions sit at one upvote or less |
| The mentions are organic | CONFIRMED | Zero founder or staff accounts across 566 posts. The thread is right about this, and it took Cal.com five years |

## The event the thread leaves out

On 14 April 2026, Cal.com went closed source[\[4\]](https://cal.com/blog/cal-com-goes-closed-source-why). The production codebase is now proprietary, and the 47,813-star repository redirects to Cal.diy, a community MIT edition. The thread's third pillar was dismantled by Cal.com themselves four months before the thread was written. The community's verdict sits at the top of Cal.com's own Reddit results: the highest-scoring post about the company is titled “Cal.com uses fears of AI against security as an excuse to go closed source”, at 213 upvotes[\[5\]](https://www.reddit.com/r/selfhosted/comments/1smangt/calcom_uses_fears_of_ai_against_security_as_an/).

## What we measured, with our own product

Two scans through our public scanner on 20 August 2026, both free tier, both methodology v9f2, both sampling the same two engines (ChatGPT and Gemini), so they are directly comparable to each other. One honest limitation: our category inference generated different buyer questions for the two brands, so this is a same-tier comparison, not a single-prompt head-to-head. The gap survives the caveat, because Calendly beat Cal.com inside Cal.com's own answer set.

| | Cal.com | Calendly |
| --- | --- | --- |
| AI visibility | **40**/100 | **77**/100 |
| ChatGPT | Named in 0 of 4 asks. The answer recommended Calendly, Acuity and Square Appointments | Named in 2 of 4 asks, rank 2, and cited |
| Gemini | Named, position 4, behind Calendly, Setmore and SimplyBook.me | Named, position 1 |
| Google AI Overview | Shown for the query. Cal.com not in it | Shown, and named |
| Wikipedia / Wikidata entity | Neither | Both (Q111946817) |
| sameAs profiles in markup | 0, empty | 5 |
| Analytics tag on the marketing site | None found. An AI-sent buyer would arrive unrecorded | Present |

**Not one of Cal.com's 32 comparison pages was cited by either engine.** The engines built their answers from third-party sources instead: stackamplify.com, techradar.com, financesonline.com, onecal.io. The tactic the thread credits as the primary mechanism is the one that measurably produced nothing. A vendor's own “why we beat our competitor” page is a low-trust source, and the engines treat it as one.

## What Cal.com did that worked

Credit where it is due, because some of this was excellent. The open-source repository was the single largest driver: five years of stars, forks and “open source alternative” listicles, every one an independent page vouching for the brand. That is a business-model decision with a five-year lead time, a closed-source SaaS cannot copy it, and Cal.com has now switched the mechanism off themselves. The positioning was sharper still: they stepped around the crowded fight for “best scheduling tool” and took outright ownership of an uncontested question, “what is the open source alternative to Calendly?”. And the thread missed their largest content play entirely: roughly **333 programmatic use-case pages** under /workflows/, /routing/ and /scheduling/, about ten times the comparison-page footprint[\[1\]](https://cal.com/sitemap_en.xml). Their best comparison post is well-shaped too, with a TL;DR as the first heading, two comparison tables, a stated evaluation method and a named author[\[6\]](https://cal.com/blog/best-calendly-alternatives). It still earned zero citations in our measurement.

The gaps are just as instructive. No structured data anywhere we looked. No Wikipedia page, no Wikidata item, and a brand name that collides with a common given name, so the models have no stable anchor for the entity. The flagship comparison page's H1 read “Calendly.com does what others can't” when we checked it, on Cal.com's own page targeting their highest-intent query[\[7\]](https://cal.com/calcom-vs-calendly). And their marketing site carries no analytics tag we could find, so an AI-referred buyer would arrive invisible.

## What a small business can copy from this by Friday

**1\. Own a specific question, never a category.** The replicable half of Cal.com's win was answering an uncontested question. Yours will be phrased the way one buyer talks: “accounting software for Queensland tradies who invoice on the road”, rather than “best accounting software”. These phrasings register zero volume in keyword tools and still get asked, which is exactly the condition where AI answers matter more than search rankings.

**2\. Build the use-case page matrix.** Cal.com's 333 programmatic pages did more work than their 699 blog posts. A small business needs 15 to 30, one per real service-by-segment pair, each answering the question in its first paragraph. That opening answer is the one structural move Cal.com skipped on their own best page.

**3\. Ship the structured data they never did.** Organization and LocalBusiness JSON-LD, a populated sameAs, FAQPage on the FAQ blocks. An afternoon of work, and on this axis you would be strictly ahead of a company with 47,813 GitHub stars by the weekend.

**4\. Earn third-party mentions instead of publishing self-comparisons.** The most transferable finding in this research. The engines cited review sites and listicles, never the vendor. For an Australian business the equivalents are industry association directories, local trade press, supplier pages and real review platforms. One independent page that recommends you outweighs ten pages where you recommend yourself.

**5\. Skip what needs five years or venture funding.** The star flywheel, repeat Product Hunt wins, 1,100 indexed pages. Cal.com's own results suggest most of that page count was wasted, and the one truly causal asset has been retired by its owner.

## Method, and what we could not verify

Every claim above was checked against the primary source linked beside it, all on 20 August 2026. The two scans cost 36 cents total and the raw engine answers are kept verbatim in each report. Explicitly not verified, and stated rather than glossed: the directory count of 23 (G2, Capterra, AlternativeTo, SourceForge, TrustRadius and StackShare all returned bot-protection responses, and a blocked fetch is not evidence of absence); the total Reddit mention count (our 172 is a floor from capped searches that cannot see comment replies); and any schema injected client-side after page load, since we read server HTML, which is also what most AI crawlers read. Our scanner flagged Cal's name collision automatically, so mention counts for the brand are unreliable by construction: a naive search for “cal” returns California real estate and college football.

The same measurement, on your business.

We asked the engines about Cal.com and kept every answer as a receipt. The free scan does the identical thing for you: who AI names, who it names instead, and which sources it reads. 60 seconds, no signup.

[Run your free scan →](https://areyoufoundbyai.com/?src=research-calcom)

**Method.** Found by AI asks ChatGPT, Claude, Perplexity and Google's AI the questions real buyers ask for each category, then measures which businesses the engines actually name. Scores are 0–100 point-in-time measurements; the index re-scans and grows automatically. Businesses listed here were selected and measured by us from public directories, [scan your own site free](https://areyoufoundbyai.com/?src=benchmarks) to see where you'd rank. Queries and methodology are open: [github.com/techhorizonlabs](https://github.com/techhorizonlabs).