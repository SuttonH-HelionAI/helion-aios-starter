---
name: content-strategy
description: Plans content pillars, topic clusters, and a prioritized publishing queue from customer research, keyword data, and competitor analysis. Auto-triggers on phrases like "content strategy", "content ideas", "what should I write about", "blog strategy", "topic clusters", "editorial calendar", "content pillars", "content roadmap", "I don't know what to write". User-invocable as `/content-strategy`.
---

> **Engine:** Growth

# /content-strategy

Plan the content engine before writing the first post. Pillars, clusters, scored ideas, publishing plan. Every piece is either searchable, shareable, or both, in that priority order.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Check `context/about-business.md`. If it exists, pull the offer, what you sell, who you serve, competitors. Check `context/about-me.md` for who you are.
2. Read the voice from `references/voice.md` and the `## Voice` section of `CLAUDE.md` so the plan and outlines land in the right register.
3. Check `projects/[current-slug]/brief.md`. If a project is active, pull the campaign brief.
4. Check `projects/[current-slug]/research/`. If customer research exists, use it.

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only what is missing for this specific run.
- **Partial:** "I have [list]. Missing [list]. Quick three-question intake to fill the gaps."
- **Fresh:** "Workspace has no context yet. Run `/onboard` first to fill `context/about-business.md`, takes about 10 minutes, then come back. This skill needs grounding to produce real value."

Never proceed without at least Loaded or Partial context.

---

## Step 1: Gather signals

Pull from every source available, in this order:

1. **Customer research** at `projects/[slug]/research/`: quote bank, personas, JTBD map. Pull verbatim language.
2. **Keyword data** if the user has GSC, Ahrefs, or SEMrush exports. Sort by volume, difficulty, intent.
3. **Sales and support input**: questions, objections, repeated pains. Extract by frequency.
4. **Forum mining**: `site:reddit.com [topic]`, `site:quora.com [topic]`, Indie Hackers, Hacker News, industry Discord.
5. **Competitor content audit**: `site:competitor.com/blog`. Identify what they cover repeatedly and the gaps they have left.

If customer research is missing, say so and recommend `/customer-research` before proceeding.

---

## Step 2: Pick pillars

3-5 pillars. Each should:

- Align with a product or service you sell
- Match what your audience cares about (proven by research, not assumed)
- Have search volume or social interest
- Be broad enough to support 8-15 subtopics

**Four ways to pick pillars:**

1. Product-led: what problems does your product solve?
2. Audience-led: what does your ICP need to learn?
3. Search-led: what topics have volume in your space?
4. Competitor-led: what are competitors ranking for that you should own too?

Pick the angle that fits the data you actually have.

**Required: name a measurable target per pillar.** Every pillar gets one primary traffic-or-conversion number with a 90-day deadline. Examples:

- "Pillar 1 hub topic targeted to 500 monthly organic visits in 90 days."
- "Pillar 2 targeted to 50 email signups per month by day 90, driven from the hub plus three spokes."
- "Pillar 3 targeted to top 10 ranking for the hub keyword in 90 days, plus 200 monthly visits."

The target gets logged in `pillars.md` next to the rationale. If you cannot name a target, the pillar is not real yet, do more research before locking it.

---

## Step 3: Map clusters

For each pillar, build a hub-plus-spokes structure:

```
Pillar (Hub)
├── Spoke 1
├── Spoke 2
├── Spoke 3
└── Spoke 4
```

The hub is the comprehensive overview. Spokes are the subtopics. Spokes link back to the hub. The hub links to all spokes.

**URL note:** most content works fine under `/blog/[slug]` with good internal linking. Only use dedicated `/guides/[topic]` URL structures when you are building a true pillar resource with multiple layers of depth.

---

## Step 4: Pick content types per piece

**Searchable types (capture existing demand):**

- Use-case content: `[persona] + [use-case]` (e.g., "project management for designers")
- Hub-and-spoke pillars
- Template libraries with standalone value
- Glossary entries for "What is [term]"
- Comparison and "vs" content

**Shareable types (create demand):**

- Thought leadership that names a pattern everyone feels
- Data-driven content using product data, public data, or original research
- Expert roundups (15-30 experts on one question)
- Case studies (Challenge, Solution, Results, Learnings)
- Meta content (transparency posts about your business)

Every piece in the queue gets tagged Searchable, Shareable, or Both. Searchable is the default. Shareable is the supplement.

---

## Step 5: Map by buyer stage

Tag every topic by stage:

| Stage | Modifiers | Examples |
|---|---|---|
| Awareness | "what is", "how to", "guide to" | "What is agile project management" |
| Consideration | "best", "top", "vs", "alternatives" | "Best PM tools for remote teams" |
| Decision | "pricing", "reviews", "demo" | "[Product] pricing comparison" |
| Implementation | "templates", "tutorial", "how to use" | "Step-by-step setup tutorial" |

A healthy queue spans all four stages, weighted toward where your funnel currently leaks.

---

## Step 6: Score and prioritize

Each topic gets scored on four factors:

1. **Customer Impact (40%)**: How often did this come up in research? What percentage of customers face this? How emotional is the pain?
2. **Content-Market Fit (30%)**: Does this align with what your product solves? Can you offer unique insights? Will it lead to product interest?
3. **Search Potential (20%)**: Monthly search volume. Competition level. Long-tail opportunities. Trend direction.
4. **Resources (10%)**: Do you have the expertise? What assets are needed? How long to produce?

**Scoring template:**

| Idea | Impact (40%) | Fit (30%) | Search (20%) | Resources (10%) | Total |
|---|---|---|---|---|---|
| Topic A | 8 | 9 | 7 | 6 | 8.0 |
| Topic B | 6 | 7 | 9 | 8 | 7.1 |

Top 10 ideas go into the first publishing batch.

---

## Step 7: Build the publishing plan

12-week plan, one piece per week for a solo team or 2-3 per week for a content team. Balance:

- 70-80% searchable, 20-30% shareable
- Distribute across buyer stages, weighted toward the leaky stage
- Start each pillar with the hub piece, then publish spokes that link to it
- Sequence so each new piece can link to two or three previously published pieces (the linking compounds)

**First piece in the queue is a "ship this week" assignment.** The top-ranked topic from Step 6 gets:

- A draft outline written into `publishing-plan.md` (working title, target keyword, target word count, H2s in order, the customer quote driving each H2, the internal links to existing pages, the CTA).
- A named owner.
- A due date set 7 days from the strategy doc timestamp.
- The pillar target it rolls up to.

Do not move on until that first outline is on the page. Strategy without an assignment ships nothing.

**30/60/90 review checkpoint.** Bake the review schedule into `publishing-plan.md`:

| Checkpoint | Date | Score per pillar |
|---|---|---|
| Day 30 | [date + 30] | Pieces published vs planned, early traffic signal, on track yes/no |
| Day 60 | [date + 60] | Traffic vs target, top 3 pieces, bottom 3 pieces, kill or double-down call |
| Day 90 | [date + 90] | Pillar target hit yes/no, revise pillar weighting, set the next 90-day targets |

If a pillar misses its day-60 trajectory by more than 50%, re-open Step 2 and either reshape the pillar or kill it.

---

## Step 8: Deliverables

Write four files to `projects/[slug]/content-strategy/`. Create the folder if it does not exist yet, `projects/` is a grow-into folder in this kit.

1. `pillars.md`: 3-5 pillars with rationale, product connection, authority case, and one named 90-day traffic-or-conversion target per pillar.
2. `clusters.md`: hub plus spokes per pillar. Mermaid or ASCII tree.
3. `topic-queue.md`: scored table of every idea with stage, type, target keyword, customer quote backing it.
4. `publishing-plan.md`: 12-week schedule with piece, pillar, type, stage, keyword, owner, due date. Includes the full "ship this week" draft outline for the top-ranked piece and the 30/60/90 review checkpoint table.

Once the plan is set, the per-piece writing hands off to `/copy` and `/social` for the actual drafts.

---

## Hard rules

- No pillar without customer research backing. If research is missing, run `/customer-research` first.
- No topic in the queue without a customer quote, a sales-call note, or a keyword backing it.
- Searchable is the default. Shareable is supplemental, not the foundation.
- Every spoke must link to its hub. The hub must link to every spoke.
- No AI tells in the published content or the strategy doc.

## When to stop

Definition of done:

- 3-5 pillars locked with rationale and a named 90-day traffic-or-conversion target each.
- Cluster map exists for every pillar.
- Top 10 topics scored and ranked.
- 12-week publishing plan written.
- Top-ranked piece has a full draft outline and a due date 7 days out.
- 30/60/90 review checkpoint table is in `publishing-plan.md` with real dates.
- All four files exist in `projects/[slug]/content-strategy/`.

Ship.
