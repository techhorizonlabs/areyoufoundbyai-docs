# Are you found by AI? documentation

Source for the public documentation of [Are you found by AI?](https://areyoufoundbyai.com), the
AI visibility measurement built and operated by [Tech Horizon Labs](https://techhorizonlabs.com).
The site is built with [Mintlify](https://mintlify.com) and published at
<https://foundbyai.mintlify.app/>.

The product asks AI engines the questions a business's buyers type, saves the answers, and shows
whether the business is named, who is named instead and what to fix. These pages cover how the
measurement works, the plans, the free tools, the MCP server, the `/api/scan` endpoint and the
open-source skills in [techhorizonlabs/thl-open](https://github.com/techhorizonlabs/thl-open).

## Where the facts come from

The live site is the source of truth. When a page here and the live site disagree, the live site
wins and this repo should be corrected. The pages to check first:

- Plans and prices: <https://areyoufoundbyai.com/pricing>
- How the measurement works: <https://areyoufoundbyai.com/how-it-works> and <https://areyoufoundbyai.com/framework>
- Machine-readable summary: <https://areyoufoundbyai.com/llms.txt>
- Agent tools and the MCP server: <https://areyoufoundbyai.com/for-agents> and <https://areyoufoundbyai.com/guides/connect-your-ai>
- Website counts: <https://areyoufoundbyai.com/methodology/website-counts>
- MCP tool list: send `tools/list` to the public demo server, `https://areyoufoundbyai.com/mcp/demo`

## Repository layout

- `docs.json`: site configuration and navigation.
- `introduction.mdx`, `quickstart.mdx`, `how-it-works.mdx`: getting started.
- `concepts/`, `guides/`, `tools/`, `research/`: product documentation.
- `api/`, `mcp/`, `skills/`: the scan endpoint, the MCP server and the open-source skills.
- `sources/site/`: dated copies of pages from the live site, kept as reference material. They are
  not maintained and may be out of date; do not cite them as current.

## Preview locally

Install the [Mintlify CLI](https://www.npmjs.com/package/mint) and run it from the folder that holds
`docs.json`:

```bash
npm i -g mint
mint dev
```

The preview runs at `http://localhost:3000`. Pushes to the default branch publish through the
Mintlify GitHub app.

## Writing rules

See [`AGENTS.md`](./AGENTS.md). In short: Australian English, plain sentences, no em or en dashes,
no hype words, and no figure lower than the real one.

## Contact

Tech Horizon Labs, Noosa, Australia. hello@techhorizonlabs.com
