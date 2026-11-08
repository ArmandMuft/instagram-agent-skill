---
name: ig-plan
description: >-
  Build the week on Instagram - what to post, which format, when, and who to
  engage with. Use when the user says "plan my week", "what should I post",
  "content calendar", "I have nothing to post about", or wants a posting
  schedule and an engagement list.
---

# ig-plan

The control room. Everything else in this pack executes; this decides what gets
executed. Run it once a week, on the same day.

## Input

Read `voice.md`, `swipe.md` and `log.md` if they exist. Look in
`~/.claude/instagram/` first, then in the project's knowledge or docs, then in
files attached to this chat. The swipe file is the user's own evidence from
`/ig-viral` about which formulas are landing in their niche right now, and it
outranks anything in this file. The log stops the plan repeating a theme from
the last fortnight.

If they do not exist, ask for five things and write them down:

1. What the user sells, and to whom.
2. The three or four themes they want to be known for.
3. What actually happened this week: a client call, a number, a mistake, a
   thing they built, an argument they had. This is where posts come from.
4. Ten accounts worth being visible to.
5. How many posts a week they can actually make and keep making, and how many
   hours that is.

## What to post

**The cadence the user can hold beats the cadence that works on paper.** If
`voice.md` gives a posting cadence, plan exactly that many posts and no more.
A plan that needs more hours than they have gets dropped in week three, and a
dropped plan posts nothing. If they want to go up, say what it costs in hours
and let them choose.

With no cadence given, four to five posts a week, and at least three of them
Reels. Reels are the only format on Instagram that reliably reaches people who
do not follow the account. Carousels go deep with the people who already do.
Stories are daily and are planned separately.

On two or three posts a week, keep the mix below but rotate it across a
fortnight instead of cramming every type into one week.

**Collabs count double.** If the account works with clients or partners, a
post published as a collab lands on both grids and reaches both audiences. If
the log or the audit shows collab posts outperforming solo ones, plan at least
one a week before anything else.

Mix across the week, never two of the same type back to back:

| type | share | job |
| --- | --- | --- |
| **Proof** | 1 per week | something that happened, with a number. Reel. |
| **Teach** | 1 to 2 per week | one thing the viewer can do today. Reel or carousel. |
| **Opinion** | 1 per week | a position that could lose you followers. Reel. |
| **Story** | 1 per fortnight | a scene with a cost. Reel. |
| **Offer** | 1 per fortnight | what you sell, said plainly, no apology. Carousel or stories. |

For each slot give: the theme, the specific angle from what actually happened
this week, the format, and the hook formula number from `ig-reel/hooks.json`.
Not a topic, an angle. "AI" is not a plan. "The proposal we lost because the
draft had an em dash in it" is a Reel.

## When to post

Post when the user's audience is awake and not at work. For most consumer
audiences that is early evening local time; for a business audience, early
morning.

But say this plainly: **the hour matters far less than the first two seconds.**
Instagram will keep showing a Reel for days if it performs, and will bury a
well-timed one that does not. If the user is optimising posting times before
their hooks work, they are polishing the wrong thing, and you should say so.

Anchor times to the audience's timezone, not the user's, if those differ.

## The engagement round, which is not optional

20 minutes a day, before posting, not after. Build a list of 10:

- **5 reach** - accounts with an audience the user wants, where a good comment
  gets seen. Comment early, before the thread is 200 deep.
- **3 peers** - same size, same field. This is the group that reciprocates.
- **2 buyers** - people who could actually buy. Comment for weeks before any
  DM, and never pitch in a comment.

Hand the list to `/ig-comment`.

## Output

```
WEEK OF SEP 15

MON  engage only  (20 min, list below)
TUE  7:30pm  REEL      PROOF    #5  Time Collapse   - 5hr proposal to 20 min
WED  stories only + engage
THU  7:00pm  CAROUSEL  TEACH    Job B caption       - the 4-slide clause breakdown
FRI  7:30pm  REEL      OPINION  #2  Negative Command - stop doing discovery calls
SAT  -
SUN  6:00pm  REEL      STORY    #21 Mid-Sentence    - the refund email

STORIES  every day, 3 to 5 frames, question box on Thursday.

ENGAGE  (5 reach / 3 peers / 2 buyers)
  ...

Say "write Tuesday" and I will draft it.
```

Write the plan to `plan.md` so the other skills can read it:
`~/.claude/instagram/plan.md` in Claude Code. In a claude.ai chat the working
folder is wiped when the chat ends, so give the user the plan and tell them to
add it to the project's knowledge as `plan.md`. Nothing is scheduled or posted
anywhere. This is a plan and the user runs it.
