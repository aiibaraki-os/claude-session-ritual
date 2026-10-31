# Opening and Closing Rituals: the shape of a session

## Why this exists

You can write great instructions for your AI, but **without a trigger to read them, they're wallpaper.** This part pins two small rituals to the start and the end of every session, so the system runs itself.

It came from a real incident. Our AI promised "daily progress starting tomorrow." **Because nothing existed to start the next day, nothing moved for 13 days.** The work itself was within the AI's reach; what was missing was anything that would start it. A promise with nothing scheduled behind it has no "tomorrow." The rituals sit on the two points that always happen, the start and the end of a session, and item 3 below puts every deadline on something that fires by itself.

## The opening ritual (Claude does it, about 30 seconds)

Paste into CLAUDE.md:

```markdown
## At the start of every session, always
1. Read the previous "one line for next time" (in notes.md) and pick up from there
2. If any promises are unfinished, state the count first
3. If I keep a numbers file, lead with anything in it older than 7 days or still empty
```

Now every session starts "where we left off" instead of "from a blank page."

## The closing ritual (you and Claude, about 1 minute)

Before you close a session, ask: **"Did you write down what we decided today? What's the one line for next time?"**

Paste into CLAUDE.md:

```markdown
## At the end of every session, always
1. Confirm today's decisions and any new rules were written into CLAUDE.md or notes.md (if not, write them now)
2. Write the "one line for next time" into notes.md: one sentence the next session can resume from
   (e.g., "Continue the blog plan. Check last week's reader count, then decide whether to keep going")
3. If a promise with a deadline was made, put it on something that fires on its own: a scheduled task if my setup has one,
   otherwise one notification (calendar or reminder). A promise with nothing scheduled behind it does not run by itself
```

**Item 3 is the easiest rule here to break.** Remembering a promise is not the same as acting on it at the right time. If nothing is scheduled to fire, nothing starts, however good the memory is.

## The weekly review (5 minutes, pinned somewhere in your weekend)

1. Update any numbers you track from real measurements. Open the dashboards and copy the figures over; this is most of the 5 minutes
2. Scan the failure log (see [`failure-log.md`](failure-log.md)) for one minute. The same pattern twice is your next CLAUDE.md rule
3. Ask yourself one question: "Did I give the AI the same correction more than once this week?" If so, that's a rule candidate too

## When it's not working

- **The rituals feel like going through the motions.** If the opening report is always "all clear," you're tracking the wrong things. Swap one item out
- **You forgot the closing ritual and just closed the window.** That's normal. Opening item 2 catches the miss: next time, Claude's first job is to check what last time left unwritten
