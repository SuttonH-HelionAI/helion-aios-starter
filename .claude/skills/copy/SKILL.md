---
name: copy
description: Writes new marketing copy, edits an existing draft, or refreshes outdated content. One skill, three branches. Auto-triggers on phrases like "write copy", "rewrite this page", "headline help", "value proposition", "edit my copy", "polish this", "refresh this content", "content audit", "update this page", "this reads awkwardly". User-invocable as `/copy`.
---

> **Engine:** Growth

# /copy

One skill for every copy task. Routes to Write, Edit, or Refresh.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Read `references/voice.md` plus the `## Voice` section of `CLAUDE.md`. This is the register every line gets matched against.
2. Read `context/about-business.md` and `context/about-me.md`. Pull positioning, who you serve, what you sell, the lineup.
3. Check `context/priorities.md` for what matters this quarter, so the copy points at the live priority.
4. Check `projects/[current-slug]/brief.md`. If a project is active, pull the campaign brief.
5. Check the user's last message for inline context (URL, product name, audience).

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only what is missing for this specific run.
- **Partial:** "I have [list]. Missing [list]. Quick three-question intake to fill the gaps."
- **Fresh:** "Context is thin. Run `/onboard` first to fill `context/about-business.md` and `references/voice.md`, then come back. This skill needs grounding to produce real value."

Never proceed without at least Loaded or Partial context.

---

## Step 1: Routing question

Ask once:

> "Are we writing new copy, editing existing copy, or refreshing outdated content?"

- **Write** when there is no draft yet.
- **Edit** when there is a draft and the goal is sharper.
- **Refresh** when the page is already live and decaying.

---

## Branch A: Write

### Page purpose and traffic source

- Page type (homepage, landing, pricing, feature, about, product launch).
- The one action you want the visitor to take.
- Where traffic is coming from (ad, organic, email). Match the headline to the source.

### Headline formulas (pick one per page, write 3 options)

| Pattern | Shape | Example |
|---|---|---|
| Outcome | {outcome} without {pain} | Generate more leads without buying ads |
| Problem | Never {bad event} again | Never miss a sales opportunity again |
| Audience | The {category} for {audience} | The CRM built for solo founders |
| Differentiation | The {category} that {differentiator} | The CRM that updates itself |
| Proof | {N} {people} use {product} to {outcome} | 50,000 marketers use Drip to send better emails |
| Question | {Question that names the pain} | Hate chasing invoices? |

### Page structure (compact landing default)

1. Hero (headline + subhead + CTA + visual)
2. Social proof bar (logos, rating, or one stat)
3. Three benefits, headline + one-sentence body + proof if available
4. How it works in 3 steps (verb + outcome)
5. Testimonial with specific result
6. Final CTA with risk reversal

For B2B enterprise pages, add a logo bar, use cases by role, security/compliance, ROI block, and demo CTA. For product launches, add a video, before/after, and launch pricing.

### CTA formula

`[Action verb] + [what they get] + [qualifier if needed]`

Kill: Submit, Sign Up, Learn More, Click Here.
Ship: Start My Free Trial, Get the Checklist, See Pricing for My Team.

### Output

- One file at `projects/[slug]/copy/[page].md`. Create the folder if it does not exist.
- Each section labeled. 2-3 headline options with one line of rationale each. Meta title and meta description if the page lives at a URL.

---

## Branch B: Edit

Run the seven sweeps in order. After each sweep, loop back through earlier sweeps to make sure you did not break anything upstream.

| # | Sweep | What you are hunting |
|---|---|---|
| 1 | Clarity | Confused pronouns, jargon, sentences doing too much, missing context |
| 2 | Voice | Tone shifts, mixed formality, "we" vs "the company", random humor |
| 3 | So What | Features with no benefit, claims with no consequence, missing bridges |
| 4 | Prove It | Best/leading/trusted without evidence, vague "thousands of customers" |
| 5 | Specificity | Save time, improve workflow, many customers, fast results |
| 6 | Emotion | Flat informational copy where pain or aspiration should land |
| 7 | Zero Risk | Friction near the CTA, unanswered objection, hidden cost |

### Plain English swaps (use replace, do not paraphrase)

| Cut | Use |
|---|---|
| utilize | use |
| facilitate | help |
| in order to | to |
| commence | start |
| prior to | before |
| approximately | about |
| accommodate | meet, hold |
| ascertain | find out |
| disseminate | spread |
| furthermore | also |

Delete entirely: very, really, basically, actually, just, in due course, at the end of the day, of course, obviously, last but not least.

### Output

- Issue list ranked by impact: clarity, then proof, then specificity, then emotion.
- Rewritten copy inline.
- One-line rationale per change.

### Quality gate

For high-stakes pages (launch, pricing, top-funnel landing), score the copy 1-10 across four personas: conversion copywriter, UX writer, target customer, brand strategist. Address anything under 7. Ship when the average is 8+ and no panelist scores below 7.

---

## Branch C: Refresh

### Trigger conditions (one is enough to refresh)

- Traffic on this URL has dropped quarter over quarter.
- Any stat or data point is more than 12 months old.
- Product, pricing, or positioning changed since this was written.
- A competitor updated their version of the same page.

### Refresh vs rewrite matrix

| Signal | Action |
|---|---|
| Core message valid, details outdated | Refresh (facts, stats, examples) |
| Brand voice has clearly evolved | Refresh plus voice rewrite |
| Topic angle or audience has shifted | Full rewrite, send to Branch A |
| Page structure no longer matches search intent | Full rewrite |
| Light touch on stats and links | Light refresh, ship same day |

### Refresh checklist

1. Freshness: update dates, stats, examples. Remove references to deprecated tools.
2. Accuracy: verify every claim. Check that every linked resource is alive.
3. Voice: match current `references/voice.md`. Older pages drift.
4. SEO: add "Last updated: [date]" near the top. Check that search intent still matches the H1.
5. Proof: swap stale testimonials, add fresh case study lines if available.
6. Structure: add a comparison table or FAQ block if scannability is weak.

### Refresh cadence (default)

- Pricing pages: every quarter.
- High-traffic blog posts: every 6 months.
- Comparison and alternatives pages: every 3-6 months.
- Evergreen guides: annually.

### Output

- Diff between old and new at `projects/[slug]/copy/refresh-[date].md`. Create the folder if it does not exist.
- One-line note next to each change: stale stat, broken link, voice drift, proof swap.

---

## Hard rules

- One idea per section. The reader should be able to summarize each section in one sentence.
- Customer language wins. Use words from quote banks and reviews, not internal feature names.
- Specificity always beats adjectives. "Cut reporting from 4 hours to 15 minutes" beats "save time."
- No em-dashes. No AI tells.
- No exclamation points outside direct quotes.
- Honest over sensational. Never invent a stat or a testimonial.
- One primary CTA per section. Secondary asks live in links.

---

## When to stop

Definition of done:

- Branch ran end to end and the deliverable is on disk under `projects/[slug]/copy/`.
- For Write, every section has copy plus 2-3 headline options with rationale.
- For Edit, every flagged issue was either fixed or explicitly left in place with a reason.
- For Refresh, the refresh-vs-rewrite verdict is stated and the staleness checklist is complete.
- Page reads cleanly when spoken aloud.

Ship.
