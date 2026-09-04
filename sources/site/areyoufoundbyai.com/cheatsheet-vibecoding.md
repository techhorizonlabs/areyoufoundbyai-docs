# Source: https://areyoufoundbyai.com/cheatsheet-vibecoding

[Are you found by **AI?**](https://areyoufoundbyai.com/) [Scan your site free →](https://areyoufoundbyai.com/?src=cheatsheet-vibecoding)

[Claude](https://areyoufoundbyai.com/cheatsheet) [ChatGPT](https://areyoufoundbyai.com/cheatsheet-chatgpt)Vibe-code

[⬇ PDF](https://areyoufoundbyai.com/cheatsheet-vibecoding.pdf) [⬇ Image](https://areyoufoundbyai.com/cheatsheet-vibecoding.png) [print](javascript:window.print())

Internal cheat sheet · steal this

# Vibe-code your own website. 
The whole stack on one page.

Design it with Claude, build it with Claude Code, ship it on Cloudflare, and bake AI-findability in from day one. Real install commands, no filler, no WordPress. Updated 22 Jul 2026.

01 · The stack (four decisions, all reversible)

Build: Claude Codethe CLI is the power toolSketch the look and structure in the Claude app first, then hand the plan to Claude Code in your terminal to build for real. Desktop and web versions exist; the CLI is the one that ships.

npm install -g @anthropic-ai/claude-code cd my-site && claude

Docs: [code.claude.com/docs](https://code.claude.com/docs)

Host: Cloudflaresimple, fast, free tierOne command scaffolds and deploys. Pick Vercel instead only if you are technical and living in Next.js.

npm create cloudflare@latest # or, technical: npm i -g vercel && vercel

Docs: [developers.cloudflare.com](https://developers.cloudflare.com/workers/) · [vercel.com/docs](https://vercel.com/docs)

Domain: Cloudflare or Namecheapat-cost beats retailCloudflare Registrar sells at wholesale (no markup, DNS in the same dashboard). Namecheap if you want a marketplace. Connect it to your host in the DNS tab: one CNAME. 
Buy: [domains.cloudflare.com](https://domains.cloudflare.com) · [namecheap.com](https://www.namecheap.com)

Logins: Cloudflare Access or Clerkgate it or grow itPrivate area for a team? Cloudflare Zero Trust (Access) gates any URL with email codes, zero code, free for 50 users. Real customer accounts? Clerk drops in sign-up, sign-in and billing-ready users.

\# Clerk (Next.js example) npm install @clerk/nextjs

Docs: [one.dash.cloudflare.com](https://one.dash.cloudflare.com) · [clerk.com/docs](https://clerk.com/docs)

02 · Level up the design (the pro-max combo)

UI/UX Pro Max skilldesign intelligenceA community skill that teaches Claude Code real design judgment: hierarchy, spacing, typography systems.

\# inside Claude Code, just type: install the UI/UX Pro Max skill

More: [mcp.directory/skills/ui-ux-pro-max](https://mcp.directory/skills/ui-ux-pro-max)

Magic MCP by 21st.devproduction components on demandType /ui and describe any component; it returns polished, animated, responsive code.

npx @21st-dev/cli@latest install claude --api-key KEY # then in chat: /ui a pricing section with 3 tiers

More: [21st.dev](https://21st.dev)

The ruthless review passbefore every shipWhen it looks done, it is not done. Ask Claude Code for a design-director pass and make it fix its own list.

Review every page like a design director. List the 10 worst issues, then fix them all. Screenshot before and after.

03 · The starter prompt (copy, paste, go)

\# NEW SITE, paste into Claude Code in an empty folder Build me a website for \[BUSINESS\] in \[TOWN/MARKET\]: \[what it sells, who buys it\]. Stack: static-first on Cloudflare (npm create cloudflare@latest), no WordPress, no framework unless genuinely needed, no dependency that does not earn its place. Before designing, read areyoufoundbyai.com/framework and areyoufoundbyai.com/llms-full.txt and apply GEO from day one: semantic HTML with one h1 per page, answer-shaped pages (the answer in the first two sentences), Organization + LocalBusiness + FAQ schema in JSON-LD, an llms.txt, robots.txt that ALLOWS GPTBot, OAI-SearchBot, ClaudeBot, PerplexityBot and Google-Extended, a sitemap.xml, and identical name-address-phone everywhere. Navigation rule: every page reachable within two clicks; nav and footer list every page. Then audit yourself before you tell me you are done: check every internal link returns 200, validate the schema at validator.schema.org, run Lighthouse and get 90+ on performance, SEO and accessibility, and screenshot the site at phone and desktop widths. Give me the audit results and the fix list, then fix them. \# CLONING A FRESH START instead? Swap the first line for: Clone the structure and content of \[OLD-SITE-URL\] into this stack, rewriting every page to be answer-shaped, then apply everything below unchanged.

**Why the GEO block matters:** buyers have stopped googling; they ask AI. A site built this way is readable to the engines that now do the recommending. The old-school move is ranking; the new one is being the answer.

04 · Prove it worked

Ship it, then measure the only thing that matters: **when a buyer asks AI who to use, are you named?** Free 60-second check: [areyoufoundbyai.com](https://areyoufoundbyai.com/), then fix what it shows you, re-scan, and watch the trend weekly. That loop is the whole game.

Keep this sheet · share it

This page: areyoufoundbyai.com/cheatsheet-vibecoding  ·  Claude models: areyoufoundbyai.com/cheatsheet  ·  ChatGPT models: areyoufoundbyai.com/cheatsheet-chatgpt 
Is AI recommending **your** business when buyers ask? Free 60-second check: [areyoufoundbyai.com](https://areyoufoundbyai.com/)

free to share · updated when the stack changesby Tech Horizon Labs