---
name: social
description: Writes, plans, and repurposes social content across LinkedIn, X, Instagram, TikTok, Facebook, and YouTube Shorts. Covers single posts, weekly batches, repurposing from long-form, and short-form video scripts. Auto-triggers on phrases like "LinkedIn post", "Twitter thread", "social calendar", "content batch", "repurpose this", "viral content", "what should I post", "TikTok script", "Reels", "Shorts", "short-form video". User-invocable as `/social`.
---
> **Engine:** Growth

# /social

Social content that pulls weight. Routes to single post, weekly batch, repurposing, or short-form video.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Check `context/about-business.md` and `context/about-me.md`. Pull positioning, ICP, JTBD, competitors, what you sell, who you serve.
2. Check `references/voice.md` and the `## Voice` section of `CLAUDE.md`. Pull the register to write in.
3. Check `context/priorities.md` for what matters this quarter.
4. Check `projects/[business]/social/pillars.md` if it exists. Otherwise build 3-5 pillars and save it.

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only what is missing for this specific run.
- **Partial:** "I have [list]. Missing [list]. Quick three-question intake to fill the gaps."
- **Fresh:** "Workspace has no context yet. Run `/onboard` first, takes 10 minutes, then come back. This skill needs grounding to produce real value."

Never proceed without at least Loaded or Partial context.

---

## Step 1: Routing question

Ask once:

> "What do you need: a single post, a weekly batch, repurposing from long-form content, or a short-form video script?"

---

## Step 2: Pillars

If `pillars.md` does not exist, build it on the first run.

Default mix (tune to ICP). Each pillar names the funnel step it serves so posts pay back, not just publish:

| Pillar | Share | Funnel step | Topics |
|---|---|---|---|
| Industry insight | 30% | Top-funnel awareness | Trends, data, predictions |
| Behind the scenes | 25% | Mid-funnel proof | Building, lessons, decisions |
| Educational | 25% | Mid-funnel proof | How-tos, frameworks, tips |
| Personal / opinion | 15% | Top-funnel awareness | Stories, values, hot takes |
| Promotional | 5% | Bottom-funnel CTA | Product, offers, launches |

Save to `projects/[business]/social/pillars.md`. Every post in the weekly batch gets tagged with its funnel step in the output file so you can see at a glance whether the week is unbalanced.

---

## Branch A: Single post

### Hook families (pick one, write 2-3 options)

- Curiosity: "I was wrong about X." "The real reason Y happens is not what you think."
- Story: "Last week, X happened." "3 years ago I [bad state]. Today I [good state]."
- Value: "How to X without Y." "5 things that Z."
- Contrarian: "Unpopular opinion: X." "Y is wrong, here is why."

### Platform shapes

| Platform | Visible before "more" | Best length | Hashtags |
|---|---|---|---|
| LinkedIn | ~210 chars | 1,200-1,500 chars | 3-5 at the end |
| X | Full 280 | Under 100 chars per tweet | 1-2 |
| Instagram | ~125 chars | Caption up to 2,200 | 3-5 |
| Facebook | 40-80 ideal | Conversational | 1-2 |
| Threads | 1-2 lines | Up to 500 | 1 |
| YouTube | First 100 chars | Up to 5,000 desc | 3-5 |

### Format rules

- Front-load the message before truncation.
- LinkedIn: links in comments. Carousels get strong reach.
- X: tweets under 100 chars perform best. Quote tweets with insight beat retweets.
- Instagram: Reels get 2x reach of static. Saves and shares weigh more than likes.
- TikTok: vertical only, trending sounds, reply to comments with videos.

---

## Branch B: Weekly batch

### Default grid

| Day | LinkedIn | X | Instagram |
|---|---|---|---|
| Mon | Industry insight | Thread | Carousel |
| Wed | Educational | Tips tweet | Reel |
| Fri | Hot take | Engagement reply | Story |

Tue and Thu: behind-the-scenes on LinkedIn, engagement on X, Story or carousel on IG.

### Batching workflow (2-3 hrs weekly)

Pull pillars and last week's top posts. Write 5 LinkedIn posts (one per pillar). Write 3 X threads plus daily one-liners. Draft 2 Instagram carousels and 1-2 Reel scripts. Schedule everything. Leave Friday open for real-time posts.

Output: `projects/[business]/social/[week-of-date].md` with every post written, hashtags included, image or video prompt where useful, and a funnel-step tag per post.

### Primary post of the week (required pick)

After the batch is written, pick one post as the week's primary. Not a calendar of equal-weight posts. One bet.

At the top of the weekly file, write:

```
## Primary post: [post title or hook]
Platform: [LinkedIn | X | Instagram | TikTok]
Goal: [signups | clicks | DMs | replies | bookings]
Target number: [e.g., 25 signups, 200 clicks, 10 DMs]
Why this one: [one sentence]
```

This is the post that gets engagement budget, paid boost if applicable, and the 30-min/day reply effort. The other posts hold the calendar. The primary moves the number.

### Minimum viable week (90 minutes)

If you only have 90 minutes, do not try to fill the full grid. Ship this instead:

- 1 LinkedIn post on the strongest pillar (mid-funnel proof), 30 min.
- 1 short-form video script, phone-recorded same day, 30 min.
- 1 X reply chain on 5 target accounts with real insight, 15 min.
- 1 primary post pick from the three above, with goal + target number, 15 min.

Output to `projects/[business]/social/[week-of-date]-mvp.md`. Ship today, batch the rest when the week opens up.

---

## Branch C: Repurposing from long-form

### Atoms per long-form piece

| Atom | Best home |
|---|---|
| Quotable line / bold claim | X, LinkedIn |
| Story arc (60-90 sec) | Reels, TikTok, Shorts |
| Tactical tip / how-to | LinkedIn, Shorts |
| Contrarian take | X, LinkedIn |
| Data callout / surprising number | LinkedIn carousel, X |

### Per piece, aim for

- 3-5 short clips (15-60 sec) for Reels, TikTok, Shorts.
- 1-2 LinkedIn text posts. 1 X thread. 1 carousel. 1 newsletter section.

### Workflow

1. Get the transcript (Whisper, Descript, podcast host).
2. Mark timestamps for the 5-10 best moments.
3. Extract clips. Write standalone captions, do not assume the viewer saw the full piece.
4. Add subtitles to every clip. Spread the release across 1-2 weeks.

---

## Branch D: Short-form video (TikTok, Reels, Shorts)

Different physics from feed posts. Three seconds to stop the scroll.

### Platform specs

| Platform | Length | Ratio | Watch out for |
|---|---|---|---|
| TikTok | 15-60 sec | 9:16 | Trending sounds, raw feel |
| Reels | 15-30 sec | 9:16 | Polished, rewards saves and shares |
| Shorts | 30-60 sec | 9:16 | YouTube SEO applies, searchable title |

### Three-second rule

Every video needs three hooks in the first second: visual, verbal, text overlay. If any is missing, the scroll continues.

### Structures

```
Problem -> Solution (15-30s)
0-3s   Hook: state the problem
3-10s  Agitate: why it matters
10-25s Solution
25-30s CTA

List (30-60s)
0-3s   Hook: "5 things that X"
3-50s  Items every 5-8 sec
50-60s CTA

Tutorial (30-60s)
0-3s   Hook: show end result first
3-8s   "Here is how"
8-50s  Steps, quick and clear
50-60s Result and CTA
```

### Hook library

- Curiosity: "The secret to X nobody talks about." "I can't believe this works."
- Value: "How to X in Y seconds." "5 things that Z."
- Story: "3 months ago I [bad state]." "I made a huge mistake with X."
- Contrarian: "Unpopular opinion: X." "Most people get this wrong."

### Caption and subtitle rules

Max 2 lines, 3-5 words per line, bold sans-serif with black outline, match timing to speech. Captions increase watch time 25-40%. Always add them.

### Output

```
## Video: [title]
Platform: [TikTok | Reels | Shorts]
Length: [seconds]
Format: [talking head | slideshow | demo | screen recording]

Hook (0-3s)
- Visual: [...]
- Audio: [...]
- Text overlay: [...]

Body
- [timestamp]: [beat]
- [timestamp]: [beat]

CTA (final 3-5s)
- Verbal: [...]
- Text: [...]
- Action: [follow / comment / link]

Notes
- Music: [trending sound or original]
- B-roll: [list]
```

---

## Engagement routine (30 min/day)

Reply to every comment on your posts. Comment on 5-10 target accounts with new insight (not "great post"). Repost with added commentary. Send 2-3 DMs to new connections.

---

## Hard rules

- One CTA per post.
- Every post must work standalone, no "as I said in the last one".
- Hooks come from the four families. If a hook does not match, rewrite.
- Captions on every short-form video. Always.
- No em-dashes. No AI tells.
- LinkedIn external links go in comments, never the post body.
- Hashtags count against character limits. Use the table above.

---

## Metrics that matter

- Awareness: impressions, reach, follower growth rate.
- Engagement: engagement rate, comments, shares, saves.
- Conversion: profile visits, link clicks, DMs, attributed leads.
- Video: watch time %, completion rate, saves, shares.

Weekly review: top 3 posts (why), bottom 3 (why), follower trend, best posting time from data.

---

## When to stop

Done when output is on disk under `projects/[business]/social/` (create the folder if it does not exist), every post has hook, body, CTA, hashtags within platform limits and any visual prompt, the pillars file exists with funnel-step tags, the weekly batch names one primary post with goal and target number, and short-form scripts include captions and B-roll notes. Ship.
