---
name: session-rituals
description: Opens each session with where you left off and closes it with one line for next time; logs AI mistakes as one-line rules. Use when starting or ending a session, or when something went wrong.
license: MIT
metadata:
  source: https://github.com/aiibaraki-os/claude-session-ritual
  version: "0.1"
---

# Session rituals

Memory and auto-loaded instructions carry a lot between sessions. What still slips is the handoff: which decision is current, what was promised and by when. This skill keeps that in two small files in the project folder that any session, any tool, and the user can read, and reads them back every time:

- `notes.md`: the handoff note (one line for next time, open promises, dated decisions)
- `failure-log.md`: one row per mistake, turned into a rule when the same pattern shows up twice

If either file does not exist, create it from the templates in `examples/` of the source repository, or start with the headings used below.

## At the start of a session

1. Read `notes.md`. Tell the user the "one line for next time" and pick up from there.
2. Count the open promises (rows in `notes.md` whose Done column is not "yes"). If there are any, say the count first.
3. If the user keeps a numbers file, lead with anything in it that is older than 7 days or still empty.

Keep the opening report to a few lines. If it is always "all clear," suggest swapping one tracked item.

## At the end of a session

1. Check that today's decisions and any new rules are written into `CLAUDE.md` or `notes.md`. If not, write them now.
2. Write one sentence into `notes.md` under "One line for next time" that the next session can resume from.
3. If a promise with a deadline was made, put it on something that fires on its own: a scheduled task if the user's setup has one, otherwise remind the user to set one notification (calendar or reminder app). A promise with nothing scheduled behind it does not run by itself.

If the user closes the window without this, the next opening catches it: the first job is to check what last time left unwritten.

## When something goes wrong

1. Add one row to `failure-log.md` on the spot: Date / Actor (AI, user, or system) / What went wrong / How it was caught / What changed / One-line lesson.
2. "Actor: user" is a design note, not blame. Write down what was left depending on someone's attention.
3. If the same actor and the same pattern appear twice, propose a one-line rule for the "Rules from the failure log" section of `CLAUDE.md`. Add it only after the user says OK.

## Limits

- Never invent numbers. If a figure is not in a file the user gave you, say so.
- Do not edit `CLAUDE.md` rules without the user's OK.
