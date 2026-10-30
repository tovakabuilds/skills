# Tovaka Builds skills

Free agent skills from [Tovaka Builds](https://www.tovakabuilds.com). Your AI agent plans and drafts your social posts. A person approves them. The Tovaka Scheduler publishes them and tells you how to fix anything that fails.

## The skills

| Skill | What it does |
| --- | --- |
| [tovaka-scheduler](skills/tovaka-scheduler/SKILL.md) | Connects your agent (Claude, Codex and others) to the Tovaka Scheduler: makes your brand brief with you, plans a week of Instagram, Facebook, Threads and Bluesky posts with secure uploads for your own images and videos, answers a client's change request, and explains failed posts. Every post waits for approval unless you turn review off. |

More are coming: content skills for finding an angle, writing hooks and scripts, and building reels.

## Install

```bash
npx skills add tovakabuilds/skills
```

Or copy `skills/tovaka-scheduler/SKILL.md` into your agent's skills folder (for Claude Code: `.claude/skills/tovaka-scheduler/SKILL.md` in your project).

## Connect your agent to the scheduler

No key to paste. Add the scheduler as a connector and sign in:

- **Claude** (desktop app or claude.ai): Settings > Connectors > Add custom connector, address `https://scheduler.tovakabuilds.com/api/mcp`, then Connect.
- **Codex** (ChatGPT desktop app): Settings > MCPs, add a Streamable HTTP server with that address, then Authenticate.

In the page that opens, sign in and click Allow. Full steps are in the skill.

## How approval works

Your agent only ever makes drafts. Nothing goes out until a person approves it, you or your client on a review link, unless you choose to skip review for a business. Agents cannot approve their own posts.

## Access

The Tovaka Scheduler is in an invite-only beta. Want an invite? Say hello at [tovakabuilds.com](https://www.tovakabuilds.com/#contact). The skills are free to use and adapt under the MIT license.

## License

[MIT](LICENSE)
