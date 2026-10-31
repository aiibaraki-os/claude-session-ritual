# Claude Session Rituals

**Two small habits that make Claude pick up where you left off, and stop repeating the same mistake.**

Claude can carry a lot between sessions now: memory, a `CLAUDE.md` it reads at the start of every session, even scheduled tasks. What still slips is the handoff itself: which decision is current, what was promised and by when, and which mistake already happened twice. These two free parts keep that in plain files that every session, every tool, and you can read. Set them up in about 30 seconds, with no installs and no code.

| File | What it does for you |
|---|---|
| [`rituals.md`](rituals.md) | Every session opens with "here's where we left off" and closes with "one line for next time" |
| [`failure-log.md`](failure-log.md) | Turns each AI mistake into a one-line record, and then into a rule, so it stops happening |
| [`examples/`](examples/) | Three ready-to-copy files (`CLAUDE.md`, `notes.md`, and a blank `failure-log.md`), so both habits run from your next session |

## Quick start (about 30 seconds)

1. Copy the three files in [`examples/`](examples/) into your project folder: [`CLAUDE.md`](examples/CLAUDE.md), [`notes.md`](examples/notes.md), and [`failure-log.md`](examples/failure-log.md).
2. Already have a `CLAUDE.md`? Paste the sections from [`examples/CLAUDE.md`](examples/CLAUDE.md) into yours instead of replacing it.

The sign that it works: the next time you open Claude Code, it starts by telling you where you left off.

## Prefer a skill? (claude.ai, about 2 minutes)

The same two habits are also packaged as an [Agent Skill](https://agentskills.io/specification): the folder [`session-rituals/`](session-rituals/) holds one `SKILL.md`.

1. Download this repository and zip the `session-rituals` folder itself, so the folder is the root of the ZIP (not its contents).
2. In claude.ai, open Customize > Skills, upload the ZIP, and turn the skill on. (Anthropic's guide: https://support.claude.com/en/articles/12512198-how-to-create-custom-skills)
3. In a project folder, keep `notes.md` and `failure-log.md` from [`examples/`](examples/). The skill reads and updates them.

Skills are an open format, so the same folder also works in other tools that support Agent Skills.

Want to know why each line is there? [`rituals.md`](rituals.md) and [`failure-log.md`](failure-log.md) explain them, with real examples.

## Waiting for Claude Duet?

On October 21, 2026, Anthropic announced Claude Duet: an agent that sends you a morning brief and messages you when something needs your attention. It is starting with Pro and Max users in the US, through a waitlist.

If Duet hasn't reached you yet, you can start the same daily rhythm today with Claude Code. The two rituals in this repository are the first step: Claude opens each session with where you left off, and closes with one line for next time.

When Duet does reach you, nothing you set up here is wasted. Duet carries over the memory and skills in your Claude account. A `CLAUDE.md` file stays in its project folder, so ask Claude in a chat to remember the rules that matter most (you can review them under Settings > Memory). Those come with you: what Claude may do without asking, which numbers it must never make up, and when a project should stop.

*This repository is not affiliated with Anthropic. Claude and Claude Duet are Anthropic products.*

## Where these come from

These are 2 of the 8 parts of a personal AI system we have run every day for 15 months. Every part was kept or rewritten based on what actually failed. The examples in the failure log come from that real log, with identifying details removed.

The full system also includes:

- an AI that messages you first every morning,
- a real-numbers file so your AI can't make numbers up,
- quit lines for projects,
- a second-opinion review before big decisions,
- a 7-day setup plan.

It is available as the **AI-OS Starter Kit**: https://aiibaraki.gumroad.com/l/ai-messages-you-first

You don't need the kit to use anything in this repository.

## License

MIT. Use it, change it, and share it.
