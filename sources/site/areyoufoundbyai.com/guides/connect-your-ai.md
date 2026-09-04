# Source: https://areyoufoundbyai.com/guides/connect-your-ai

Guide · working with your AI

# Connect your AI once, stop re-pasting a new snapshot every week

**Make this page yours.** Paste any private Found by AI link you already have, your console link, or any link from a monitoring email, and this page rebuilds with your real addresses filled in, ready to copy.

Fill in this page

Where your token lives, in any of those links: 
`areyoufoundbyai.com/monitor/a1b2c3d4e5f60718` 
The highlighted part is your token (that one is a made-up example). The same token works for every link on this page, and your console's **Connect your AI** section has all of this pre-filled with one-tap copy buttons.

The button in your weekly email opens a **new conversation** with that week's numbers pasted in as text. Useful once, but it means every week starts from zero, no memory of what you and your AI already worked through. There's a better way, and it costs you nothing to set up: your monitoring link is a **live URL, not a snapshot**. Fetched today it returns today's data; fetched again in six weeks it returns six-weeks-from-now's data, same link. Point your AI at that link _once_, as a standing instruction, and every new chat starts current automatically.

## The idea in seventy seconds

The launch film shows the loop this guide sets up: the engines answer your buyers, the weekly measurement records what they say, and your own AI works from that data once it is connected.

 ![](https://areyoufoundbyai.com/assets/launch-v2-poster.png) Play the film · 1:10

The film runs seventy seconds and has sound. If the player does not load, [open the film directly](https://areyoufoundbyai.com/assets/launch-v2.mp4) (MP4, 12 MB).

## What to paste

Most AI chat tools let you set persistent instructions for a project or space, text applied to every new conversation inside it, not just the current one. Paste this:

At the start of every new conversation in this project, fetch https://areyoufoundbyai.com/monitor/YOUR-TOKEN.json (or the plain-text version at https://areyoufoundbyai.com/monitor/YOUR-TOKEN/context.md) and use it as my current Found by AI data, my AI-visibility score, tracked buyer questions, priority fixes and citation targets, before answering anything about my AI visibility, competitors, or what to do next. Re-fetch it fresh every new chat; don't rely on a cached copy from an earlier conversation.

## Where to paste it

- **Claude**: create or open a Project, look for its custom instructions / project knowledge setting, and paste the text above. Every new chat inside that project starts with your latest data.
- **ChatGPT**: same idea inside a Project: its instructions field applies to every new chat you start there. (If you're building a custom GPT and want your AI to query this on demand mid-conversation rather than only at the start, that needs an Action wired to the JSON endpoint, more setup, ask us if you want a hand.)
- **Perplexity**: Spaces support custom instructions the same way; add yours to a Space dedicated to your business.
- **Gemini**: Gems support a persistent instructions field; create one for this and paste the text above.

Exact menu labels move around as these products update, look for "instructions," "custom instructions," or "project knowledge" inside whatever the tool calls a Project/Space/Gem. The paste-in text above is the part that matters and won't change.

## Or connect over MCP, a live two-way line

The standing instruction above makes your AI _read_ your data at the start of a chat. Your console is also a live **MCP server**, the open standard AI tools use to call other software, which means your assistant can query your measurements mid-conversation, whenever the question comes up, not just at the start. Your endpoint:

https://areyoufoundbyai.com/mcp/YOUR-TOKEN

**No monitor yet? Try the live demo right now.** The demo endpoint is connected to our own monitoring of areyoufoundbyai.com, real production data, no account:

https://areyoufoundbyai.com/mcp/demo

[Add the demo to Cursor →](cursor://anysphere.cursor-deeplink/mcp/install?name=foundbyai-demo&config=eyJ1cmwiOiJodHRwczovL2FyZXlvdWZvdW5kYnlhaS5jb20vbWNwL2RlbW8ifQ%3D%3D)or in Claude Code: `claude mcp add --transport http foundbyai-demo https://areyoufoundbyai.com/mcp/demo`

Ask it "how visible is this business to AI, and what would you fix first?" Then run your own free scan at [areyoufoundbyai.com](https://areyoufoundbyai.com/) and your monitor gets an endpoint of its own.

It exposes thirteen read tools and one action, each a live query against the same measurements your console renders:

- `get_visibility`, your current AI Visibility and AI Readiness scores (each /100) with the week before for comparison, your separate off-site Footprint score, and the subscores behind them.
- `get_question_trajectories`, every tracked buyer question with its measured history, day by day: how many of the 7 engines named you each time it was asked.
- `get_rivals`, the competitor names the engines actually gave buyers in the latest scan when they didn't name you.
- `get_share_of_voice`, your slice of AI-answer mentions against those rivals, and how it has moved over the tracked window.
- `get_mentions`, the new pages on the web that mention your business, from the daily sweep (pass `days` to set the look-back window).
- `get_context`, the whole weekly picture in one call: scores, questions, mentions, fixes, the same content as the context pack above.
- `get_fix_plan`, the prioritised fix list from your latest deep scan, highest leverage first.
- `get_citation_sources`, the domains the engines actually cite in your category, and whether you appear on each.
- `get_personas`, the buyer personas behind your tracked questions, with the exact questions each persona asks.
- `get_post_brief`, a drafting brief assembled from this week's verified data: fresh mentions, the questions you're absent from, the sources the engines read. Your AI writes the post, in your voice.
- `get_ai_traffic`, the visitors AI engines actually sent to your site in the last 30 days, recorded by your site's own beacon.
- `get_agent_view`, how a headless agent browser renders your site: full, partial or blank, with the characters an agent can extract.
- `get_benchmark`, where you rank against every other measured business in your category.
- `request_rescan`, the one action: queues a fresh measurement right now (capped by your plan's on-demand allowance) and changes nothing else.

- **Claude (app)**: Settings → Connectors → Add custom connector, paste the URL above. Then any chat can ask "what moved in my AI visibility this week?" and Claude queries it live.
- **Claude Code**: `claude mcp add --transport http foundbyai https://areyoufoundbyai.com/mcp/YOUR-TOKEN`
- **Cursor**: add it as a custom MCP server with HTTP transport, no API key field needed, the token in the URL is the key.
- **Other MCP clients**: custom server, HTTP transport, the endpoint above. The address is the whole setup.

## What to ask once it's connected

Anything you'd ask a colleague who had your console open. The point of the live connection is that these work mid-conversation, weeks after setup, and always answer from this week's data:

- "What moved in my AI visibility this week, and what's the single most useful thing I can do about it?"
- "Which buyer questions am I still invisible on, and who is AI naming instead of me on those?"
- "Draft a short update for my business partner: our current scores, the trend, and any new mentions this month."

If a coding agent builds your site, the next step is [Connect your AI and let it work the plan](https://areyoufoundbyai.com/guides/ai-loop): your agent reads the fix plan over this same connection, applies the fixes in your repository with your approval, and re-measures until a target you set.

Fourteen of the fifteen tools only read. The one action, request\_rescan, re-runs your own measurement inside your plan's cap and touches nothing else: the connection can never change your account, plan or billing. The same privacy rule below applies, the URL contains your token.

## Keep the link private

Your link's token is effectively a password to your own data, anyone with it can view your measurements. Don't post it publicly (a public GitHub repo, a shared doc, a tweet). Sharing it with your own AI tool, or a teammate you trust, is exactly what it's for.

## What's actually in the data

Both formats carry the same live picture: your AI-visibility and readiness scores, the specific buyer questions engines do and don't name you for (with movement over time once you have history), the scanner's own ranked list of what to fix first, a citation game plan of where to get listed or reviewed so AI cites you, new independent mentions found in the last week, and adjacent questions worth tracking. The plain-text version at `/context.md` is built for attaching to a chat; the `.json` version is for anything that wants to parse it directly.

## Still want the weekly nudge

Keep the weekly email, the new-chat button is genuinely useful the first time, or any time you want a clean-slate read. The connected project is for the ongoing conversation in between.