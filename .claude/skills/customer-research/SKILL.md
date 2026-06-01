---
name: customer-research
description: Mines customer language and synthesizes themed insights, personas, and a verbatim quote bank from real assets and online sources. Auto-triggers on phrases like "customer research", "VOC", "voice of customer", "talk to customers", "build personas", "review mining", "Reddit mining", "G2 reviews", "what do customers say". User-invocable as `/customer-research`.
---

> **Engine:** Growth

# /customer-research

You synthesize what customers actually said, not what the founder wishes they said. Two modes, one output. No invented data.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Check `context/about-business.md`. If it exists, pull the offer, what you sell, who you serve, competitors. Check `context/about-me.md` for who you are.
2. Read the voice from `references/voice.md` and the `## Voice` section of `CLAUDE.md` so deliverables land in the right register.
3. Check `projects/[current-slug]/brief.md` if a project is active.
4. Check the last message for inline context (URLs, asset paths, segment focus).

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only the two intake questions.
- **Partial:** "I have [list]. Missing [list]. Quick three-question intake to fill the gaps."
- **Fresh:** "Workspace has no context yet. Run `/onboard` first to fill `context/about-business.md`, takes about 10 minutes, then come back. This skill needs grounding to produce real value."

Never proceed without at least Loaded or Partial context.

---

## Step 1: Two-question intake

Ask exactly these two questions, one at a time:

1. "What is the goal? Improve messaging, build personas, find product gaps, understand churn, or something else?"
2. "What research assets do you have right now? Transcripts, surveys, support tickets, G2 reviews, NPS verbatims, or nothing yet?"

Default the project folder to `projects/[current-project]/research/`. If no current project, ask for a slug. Create the folder if it does not exist yet, `projects/` is a grow-into folder in this kit.

---

## Step 2: Route to one or both modes

Based on the intake:

- Assets exist, run **Mode A: Synthesis** on them.
- No assets, skip to **Mode B: Gather** to collect raw data first.
- Both, run Mode B until the minimum sample is hit, then Mode A.

Tell the operator which mode you are running and why before you start.

---

## Mode A: Synthesis

For every asset, extract six fields:

1. **Jobs to Be Done.** Functional, emotional, social.
2. **Pain Points.** Unprompted pains with emotional language rank highest.
3. **Trigger Events.** What changed that made them look.
4. **Desired Outcomes.** In their words, verbatim.
5. **Language and Vocabulary.** Exact phrases. This is the gold. "We were drowning in spreadsheets" beats "manual process inefficiency."
6. **Alternatives Considered.** Competitor, DIY, do nothing, hire someone.

After extraction, synthesize:

1. Cluster by theme across assets.
2. Score each theme on frequency times intensity.
3. Segment by customer profile if signals are present (company size, role, tenure).
4. Pick the five to ten money quotes that best carry each theme.
5. Flag contradictions, places where customers said one thing but behavior said another.

### Confidence tiers

Label every insight before you present it:

| Confidence | Criteria |
|---|---|
| High | Theme in 3+ independent sources, mentioned unprompted, consistent across segments |
| Medium | Theme in 2 sources, or only prompted, or limited to one segment |
| Low | Single source, possible outlier, needs validation |

### Sample bias

Call this out in the output, not silently:

- Online reviewers skew toward power users and strong opinions.
- Support tickets skew toward problems, not value.
- Reddit skews technical and skeptical vs mainstream buyers.
- App store reviews skew toward the very happy and the very angry.

### Minimum viable sample

Do not build a persona or claim a theme from fewer than five independent data points per segment. Say so out loud when the data is thin.

---

## Mode B: Gather

Pick sources based on ICP type. Read raw, capture verbatim, do not paraphrase.

| ICP Type | Primary Sources |
|---|---|
| B2B SaaS, technical buyers | Reddit role-specific subs, G2 and Capterra, Hacker News, LinkedIn, Indie Hackers |
| SMB and founders | r/entrepreneur, r/smallbusiness, Indie Hackers, Product Hunt, Facebook Groups |
| Developer and DevOps | r/devops, r/programming, Hacker News, Stack Overflow, Discord |
| B2C and consumer | App store 1-3 star reviews, Reddit hobby subs, YouTube comments, TikTok comments |
| Enterprise | LinkedIn posts, analyst reports, G2 Enterprise filter, job postings |

Quick decision guide:

- Have a product category? Start with G2 and Capterra, your category and your competitors.
- Need raw language? Reddit threads and YouTube comments.
- Need triggers? LinkedIn posts and "Ask HN" threads, look for the moment something broke.
- Need competitive intel? Competitor 4-star reviews on G2, every one names a small gap.

For every quote captured, log: source URL, exact quote, context, sentiment, theme tag, customer profile signals.

---

## Step 3: Synthesize into the deliverable

Default deliverable set, write all four unless the operator asked for less:

1. **Quote bank** at `projects/[slug]/research/quote-bank.md`. Themed. Frequency and intensity per theme. Five to ten money quotes per theme with source attribution.
2. **Personas** at `projects/[slug]/research/personas.md`. One to three. Only segments with five or more data points. No invented fields. Profile, primary JTBD, triggers, top pains, desired outcomes, objections, alternatives, vocabulary, channels.
3. **JTBD map** at `projects/[slug]/research/jtbd.md`. Functional, emotional, social jobs by segment.
4. **Gap doc** at `projects/[slug]/research/gaps.md`. What you still do not know, where to find it.

This quote bank is the canonical source `/icp` pulls verbatim quotes from. The same research feeds `/content-strategy` topic ideas and any `/copy` or `/ads` run you make later.

---

## Persona anti-patterns

- Do not name them cutely (no "Marketing Mary") unless the team genuinely uses the name.
- Do not average across segments. A persona that represents everyone represents no one.
- Do not invent. Leave a field blank if you have no data on it.
- Revisit personas quarterly. Markets and products move.

---

## Hard rules

- No paraphrasing in quotes. Verbatim or do not include it.
- No persona under five data points per segment. Say so.
- Every insight gets a confidence tier. No silent guesses.
- Weight assets from the last 12 months heavier. A 3-year-old transcript may describe a different product.
- Strip AI tells from every deliverable.

---

## When to stop

Definition of done:

- Both modes that were needed have run.
- All four deliverables exist in `projects/[slug]/research/`.
- Confidence tiers and sample bias are visible in the output.
- The gap doc names the next three sources to mine.

Ship.
