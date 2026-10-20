# Opening and Closing Rituals: the shape of a session

## Why this exists

You can write great instructions for your AI, but **without a trigger to read them, they're wallpaper.** This part pins two small rituals to the start and the end of every session, so the system runs itself.

It came from a real incident. Our AI promised "daily progress starting tomorrow." **Because nothing existed to start the next day, nothing moved for 13 days.** An AI that lives in sessions has no "tomorrow." It has only "now" and "the next time you open it," and the rituals sit on exactly those two points.

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
3. If a promise with a deadline was made, remind me to set one notification (calendar or reminder).
   The AI does not exist until it is next opened. Deadlines are kept by notifications, not by the AI's memory
```

**Item 3 is the easiest rule here to break.** "The AI will remember" fails you every time. The only things that remember are files and notifications.

## The weekly review (5 minutes, pinned somewhere in your weekend)

1. Update any numbers you track from real measurements. Open the dashboards and copy the figures over; this is most of the 5 minutes
2. Scan the failure log (see [`failure-log.md`](failure-log.md)) for one minute. The same pattern twice is your next CLAUDE.md rule
3. Ask yourself one question: "Did I give the AI the same correction more than once this week?" If so, that's a rule candidate too

## When it's not working

- **The rituals feel like going through the motions.** If the opening report is always "all clear," you're tracking the wrong things. Swap one item out
- **You forgot the closing ritual and just closed the window.** That's normal. Opening item 2 catches the miss: next time, Claude's first job is to check what last time left unwritten
