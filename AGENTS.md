# Documentation project instructions

This repo is the public documentation for **Are you found by AI?**, built and operated by Tech
Horizon Labs. It is a [Mintlify](https://mintlify.com) site: pages are MDX files with YAML
frontmatter, and configuration and navigation live in `docs.json`.

## Source of truth

The live site at https://areyoufoundbyai.com is the source of truth. Before changing a fact, check
it against the live page that states it (`/pricing`, `/how-it-works`, `/framework`, `/llms.txt`,
`/for-agents`, `/guides/connect-your-ai`, `/methodology/website-counts`) or against the live MCP
`tools/list` on `https://areyoufoundbyai.com/mcp/demo`. If you cannot trace a claim to one of
those, do not publish it.

## Terminology

- The product is "Are you found by AI?", with the question mark. Use the full name in titles and
  first mentions.
- The paid plan is "Pro". The one-off report is the "Snapshot". Agencies and groups with several
  sites ask for a rate; there is no public agency price.
- The headline measure is the "named share": countable saved answers that name the business,
  divided by all countable saved answers. Every saved repetition counts, and missing evidence is
  left out rather than counted as a no.
- "AI Visibility" and "AI Readiness" are scores out of 100. "Footprint" is the separate off-site
  score. Describe the AI Visibility score only with the public scoring basis on the live site
  and in the MCP tool descriptions; do not add calculation details beyond that.
- Website counts are hostnames, not businesses: write "4,400+ websites measured".

## Style

- Australian English (optimise, organisation, behaviour, colour), except in code, identifiers,
  URLs and quoted names.
- Plain, full sentences in active voice, addressed to the reader as "you".
- No em or en dashes anywhere. Use a comma, colon, full stop or brackets, and "to" or a plain
  hyphen for ranges.
- No hype words such as unlock, leverage, seamless or powerful.
- Never use a count lower than the real figure.
- Sentence case for headings. Bold for UI elements, for example **Settings**. Code formatting for
  file names, commands, paths and code references.

## Content boundaries

- Document what is live for customers. Do not document features that are built but switched off,
  internal crew or agent names, or internal scoring weights.
- `sources/site/` holds dated copies of live pages for reference. Do not edit or cite them as
  current.
- Never publish a private console link or monitor token. Use `YOUR-TOKEN` in examples.
