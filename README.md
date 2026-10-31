# Tovaka Builds skills

Free agent skills from [Tovaka Builds](https://www.tovakabuilds.com). Your AI agent plans and drafts your social posts. A person approves them. The Tovaka Scheduler publishes them and tells you how to fix anything that fails.

## The skills

| Skill | What it does |
| --- | --- |
| [tovaka-scheduler](skills/tovaka-scheduler/SKILL.md) | Connects your agent (Claude, Codex and others) to the Tovaka Scheduler: makes your brand brief with you, plans a week of Instagram, Facebook, Threads and Bluesky posts with secure uploads for your own images and videos, answers a client's change request, and explains failed posts. Every post waits for approval unless you turn review off. |

### Content skills

Make short-form posts from your own brand brief. `content-factory` runs the rest in order and stops twice for your yes: once to approve the formats, and once to approve the finished media, captions and times before anything goes to the scheduler as a draft. Every other skill also works on its own.

| Skill | What it does |
| --- | --- |
| [content-factory](skills/content-factory/SKILL.md) | Runs the whole batch, from brand brief to drafts waiting for approval in the Tovaka Scheduler. Never publishes. |
| [study-format](skills/study-format/SKILL.md) | Turns 1 to 3 posts you like into a reusable format for your business (the structure, in your own words). |
| [pick-angle](skills/pick-angle/SKILL.md) | Picks the goal, emotion, angle and call to action for each post. |
| [hook-writer](skills/hook-writer/SKILL.md) | Writes 3 hooks per topic and scores each against a 4-point checklist. |
| [scripter](skills/scripter/SKILL.md) | Writes the script from the top hook. |
| [builder](skills/builder/SKILL.md) | Beat sheet, render with your own tools, and a first-frame check. |
| [caption-variants](skills/caption-variants/SKILL.md) | Instagram, Facebook, Threads and Bluesky captions, each inside its platform's limits. |
| [save-winners](skills/save-winners/SKILL.md) | After posts have run, saves what worked so the next batch starts from it. |

The scoring checks your hooks and first frame against a checklist. It does not predict views or virality.

## Install

```bash
npx skills add tovakabuilds/skills
```

Or copy a skill's whole folder (for example `skills/tovaka-scheduler/`) into your agent's skills folder (for Claude Code: `.claude/skills/tovaka-scheduler/` in your project). Copy the whole folder, not just SKILL.md: content-factory and study-format each carry a FORMATS-FILE.md.

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

[MIT](LICENSE). Sources, ideas we adapted and Ootto's license: [NOTICE.md](NOTICE.md).
