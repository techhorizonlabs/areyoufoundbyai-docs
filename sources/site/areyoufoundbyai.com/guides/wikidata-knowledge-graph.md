# Source: https://areyoufoundbyai.com/guides/wikidata-knowledge-graph

Guide · entity signals

# Getting into Wikidata and Google's Knowledge Graph, without getting deleted

Being a recognised **entity** is one of the strongest signals AI engines weigh when deciding who to name. Wikidata and Google's Knowledge Graph are the two registries that matter most, and both are widely misunderstood. This guide is unusually honest because **we got our own items deleted** and are writing from the deletion log.

**What happened to us:** we created Wikidata items for our company and product, referenced with our There's An AI For That and Product Hunt listings. An admin deleted both within days: _"Does not meet the notability policy… the only contributor was \[our founder's account\]."_ Every step below exists because of that lesson.

## Why self-created Wikidata items get deleted

Wikidata's notability bar for companies needs **serious, publicly available, independent sources**. These do NOT count: your own website, directory listings you created (Product Hunt, TAAFT, Crunchbase you filled in yourself), social profiles, press releases. A brand-new account whose only edits are its own company is the classic deletion trigger, admins see hundreds of these a week.

## The durable path in

1. **Bank independent coverage first.** Real press, industry newsletters that chose to feature you, awards, books, research citations. One genuine article beats ten self-made listings.
2. **Make your account non-single-purpose.** Before touching your own brand, make a handful of genuinely useful edits to unrelated items over a few weeks. Single-purpose accounts get pattern-matched.
3. **Create ONE minimal item, the organisation.** Label, description, instance-of (business), country, official website, founder, and a registry identifier (in Australia: your ABN via the ABR). Reference every claim, with retrieved dates. No puffery.
4. **Wait 30+ days before the product item.** If the org item survives review, add the product with the same discipline, linked via developer/publisher.
5. **Never recreate a deleted item unchanged.** Same-day re-deletion plus a possible block. If deleted, the answer is more independent sources, not persistence.

## How Google's Knowledge Graph actually forms

There is **no submission form** for the Knowledge Graph. Google builds entities from corroboration: Wikidata/Wikipedia, your **schema.org Organization markup**, government registries, consistent NAP details, and independent mentions across the web. In practice:

- Ship Organization JSON-LD with `sameAs` links to profiles that verifiably exist (a dead link is an anti-signal, we've made that mistake too).
- Match your name, address and details EXACTLY everywhere they appear.
- Earn third-party citations, across the businesses we measure, most brand mentions in AI answers sit on third-party pages, and KG formation follows the same gravity.
- Registry identifiers (ABN/ABR in Australia, Companies House in the UK) corroborate legal existence for free.

Expect the Knowledge Graph to lag your citation-building by weeks to months. It's a trailing indicator of the same work, not a lever you pull directly.

## How to check where you stand

Our free scan checks your entity signals live, Wikidata presence, Knowledge Graph entry, registry verification, schema, and the citations that drive both, as part of the 30+ signals behind your AI-visibility score. [Run the free scan →](https://areyoufoundbyai.com/?src=guide-wikidata)