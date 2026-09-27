# AI Radar

A daily agent that sweeps the web for **practical AI news** — new apps, big
launches, breakout tools and real use cases — and writes a short digest so you
don't miss the next Wispr Flow or Grok moment.

| File | What |
|---|---|
| [AGENT.md](AGENT.md) | What the agent does each run: the bar, sources, scoring, format |
| [profile.md](profile.md) | **Your taste** — context, stack, feedback log. Edit this to tune it |
| [digests/](digests/) | One file per day, newest = latest |

Runs as a scheduled Claude Code routine: each firing opens a fresh session on
this repo with the prompt "Follow ai-radar/AGENT.md", which searches, writes
`digests/YYYY-MM-DD.md`, commits and pushes.

**To tune it:** add a line to the feedback log in `profile.md`, e.g.
"more consumer apps, less enterprise".
