# The Failure Log: template and a filled-in sample

## Why this exists

When an AI messes up, most people make it apologize and move on. The apology is forgotten three minutes later. **A failure becomes an asset only when you turn it into a one-line record, and then into a rule or a mechanism.**

The ledger has six columns and takes about two minutes to fill in:

`Date / Actor (the AI, me, or the system) / What went wrong / How it was caught / What changed / One-line lesson`

**Two principles that matter:**

1. **An "Actor: Me" row is not self-blame.** Write it as a design failure: something was left depending on human attention. The "What changed" column is the star.
2. **Log what worked, too** (Actor: System, a win). If you change how you work without knowing what was working, you'll break the thing that was working.

## The blank ledger (copy this into failure-log.md)

```markdown
# My failure log

| Date | Actor | What went wrong | How it was caught | What changed | One-line lesson |
|---|---|---|---|---|---|
| [date] | [AI / me / system] | [what happened] | [how you noticed] | [new rule? new mechanism?] | [one line] |
```

## Filled-in sample (five entries, abstracted from our real log)

| Date | Actor | What went wrong | How it was caught | What changed | One-line lesson |
|---|---|---|---|---|---|
| Ex. 1 | AI | Invented the owner's income and savings, then kept proposing plans built on those numbers | The owner felt the numbers were off | New CLAUDE.md rule: "no stating numbers before reading the numbers file" | Plausible is not the same as true |
| Ex. 2 | AI | Proceeded as if a file existed that didn't | A search confirmed it wasn't there | New rule: "confirm a thing exists before referencing it" | A path from memory is a claim, not a fact |
| Ex. 3 | Me | Let a decision document sit for 12 days; the AI concluded it didn't exist | It surfaced during a review | Unfinished items idle for 7+ days now show up automatically at every session start | Filed is not finished. The loop closes when the change is confirmed in place |
| Ex. 4 | AI | Promised "daily progress starting tomorrow," but nothing existed to start the next day: 13 days of zero progress | The owner asked "any progress?" | Banned "I'll do it tomorrow." The two options are: do it now, or set a trigger (a notification or a scheduled run) | A promise without a mechanism is a wish |
| Ex. 5 | System (a win) | Nothing went wrong: a second AI caught three fake sources cited by the first | The fact-checking step caught them before anything went public | Kept the review step as standard practice | The review step earns its keep on the days nothing goes wrong |

## How to run it

- Add entries **on the spot**. If a failure crosses a session boundary, you'll remember about 30% of it
- In the weekly review (see [`rituals.md`](rituals.md)), scan the ledger for one minute. The same actor and the same pattern twice: that's your next CLAUDE.md rule
- Keep the ledger private by default. If you publish from it, publish only a summary, with names, amounts, and identifying details stripped out
