---
name: lead-magnets
description: Plans and ships email-capture assets, downloadable lead magnets or interactive free tools, with gating, landing page, distribution, and measurement built in. Auto-triggers on phrases like "lead magnet", "gated content", "content upgrade", "free tool", "calculator", "generator", "ROI calculator", "audit tool", "grader", "opt-in", "freebie", "PDF download", "Notion template", "engineering as marketing". User-invocable as `/lead-magnets`.
---
> **Engine:** Growth

# /lead-magnets

One skill, two branches. Picks the format, defines the offer, ships the capture and distribution plan. Never generic. Always grounded in the operator's ICP and stage.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Check `context/about-business.md` and `context/about-me.md`. Pull positioning, ICP, JTBD, top objections, what you sell, who you serve.
2. Check `references/voice.md` and the `## Voice` section of `CLAUDE.md`. Pull the register to write in.
3. Check `context/priorities.md` for stage and what matters this quarter.
4. Check the user's last message for inline context: a topic, a deliverable name, an audience.

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only what is missing for this specific run.
- **Partial:** "I have [list]. Missing [list]. Three-question intake."
- **Fresh:** "Workspace has no context. Run `/onboard` first, ten minutes, then come back. This needs grounding to produce real value."

Never proceed without Loaded or Partial.

---

## Step 1: Route

Ask one question:

> "What are we building? Pick one: a downloadable lead magnet (PDF, template, checklist, Notion doc) or an interactive free tool (calculator, generator, audit, grader)."

Pick the branch. State the choice and why. Continue.

---

## Branch A: Downloadable lead magnet

### A1. Pick the format

Match format to buyer stage and effort budget:

| Stage | Goal | Best formats |
|---|---|---|
| Awareness | Educate on the problem | Checklist, cheat sheet, mini-course |
| Consideration | Help evaluate solutions | Comparison template, assessment, swipe file |
| Decision | Remove implementation friction | Ready-to-use template, migration guide, ROI worksheet |

Rule of thumb. Pick the format the audience already searches for, not the one you want to write. A pre-filled Notion template usually beats a 40-page ebook for B2B SaaS audiences.

### A2. Outline the content

Solve one specific problem, not a category. "Cold email templates that get replies" beats "the cold outreach guide." Keep consumable under thirty minutes, ideally under ten. Show the immediate, actionable takeaway in the first page.

### A3. Decide the gate

| Gate | Use when |
|---|---|
| Full gate | High-value, bottom-funnel, lead quality matters more than volume |
| Partial gate | Preview plus full version, balances reach and capture |
| Ungated plus optional opt-in | Top-funnel education, max reach |
| Content upgrade | Inside a blog post, contextual, converts 2 to 5x the sidebar |

Ask for the minimum fields. Email only converts highest. Every extra field cuts conversion 5 to 10 percent. Email plus role is the ceiling unless the offer is webinar-tier.

### A4. Landing page and delivery

Landing page: headline benefit, preview mockup, three to five bullets of what is inside, social proof line, form, FAQ. Delivery: thank-you page plus email copy. Thank-you page never goes to waste, propose the next step (demo, trial, related read).

---

## Branch B: Interactive free tool

### B1. Validate the idea

Run the eight-factor scorecard, 1 to 5 each:

| Factor | What you score |
|---|---|
| Search demand exists | Is there real volume for "[thing] calculator" or "[thing] generator"? |
| Audience matches buyers | Tool users have to map to your ICP, not random traffic |
| Uniqueness vs existing | What is already live? Can you be 10x more useful? |
| Natural path to product | Tool reveals a gap your product fills |
| Build feasibility | Can a v1 ship in a week or two? |
| Maintenance burden (inverse) | What breaks weekly if you ship this? |
| Link-building potential | Is this the kind of thing other writers cite? |
| Share-worthiness | Will the output get screenshotted? |

25 plus is greenlight, 15 to 24 is promising, under 15 is reconsider.

### B2. Tool types

| Type | Examples | Best for |
|---|---|---|
| Calculator | ROI, savings, pricing estimator | Decisions involving numbers |
| Generator | Templates, names, policies, copy | Create something quickly |
| Analyzer | Site grader, SEO auditor, copy scorer | Evaluate existing work |
| Tester | Meta tag preview, deliverability test | Check if something works |
| Library | Snippet bank, icon set, template gallery | Reference material |

### B3. MVP scope

Core function only, one input flow, one output. Mobile works. Email gate on the full report. Skip account creation, save-results, advanced features, pixel-perfect design. Ship in a week.

### B4. Gating

Two patterns work. Show the result, gate the detailed report (highest conversion that still respects the user). Or unlock advanced inputs after email capture. Avoid hiding the whole tool behind a form, kills SEO and shareability.

### B5. SEO and link bait

Tool landing page targets "[thing] calculator", "[thing] generator", "free [tool type]." Supporting blog targets "how to [use case]", "what is [concept]." Tools earn links because they are useful, unique, and shareable. Reach out to writers covering the category with the tool as a citation candidate.

---

## Step 2: Distribution plan (both branches)

Pick channels that match the offer:

- Blog: inline CTA inside the three highest-traffic relevant posts. Build a post-specific content upgrade where it makes sense.
- Popups: exit-intent and scroll-depth, message matches the page topic. The installed `/cro` skill specs these.
- Social: carousel of three to five key points, link to the asset in bio. The installed `/social` skill writes these.
- Paid: lead ads for top-funnel assets, search ads for high-intent (templates, calculators), retargeting for blog traffic. The installed `/ads` skill drafts these.
- Partner co-promo: include in adjacent newsletters, joint webinars, bundled resource collections.

---

## Step 3: Measurement

Benchmarks you should hit:

| Metric | Target |
|---|---|
| Landing page conversion (warm) | 20 to 40 percent |
| Landing page conversion (cold) | 5 to 15 percent |
| Cost per lead | Varies, set against LTV and channel CAC |
| Lead-to-customer (B2B) | 1 to 5 percent |
| Email open rate on delivery | 30 to 50 percent |

A/B test one variable at a time: headline (benefit vs curiosity), format (checklist vs guide on same topic), gate level, form fields, CTA copy.

---

## Hard rules

- One format per asset. Do not ship an ebook plus a video plus a spreadsheet for the same offer.
- Solve one problem, not a category. Specific beats broad every time.
- Email-only form unless the offer earns a second field.
- Build the destination after capture too, the welcome email and the first nurture send go live before launch. The installed `/email` skill drafts both.
- Never gate the whole tool behind a form, kill SEO.
- No AI tells in any output.

---

## When to stop

Definition of done:

- Branch picked, format chosen, outline or spec written.
- Gating decision, form fields, landing page structure, delivery method documented.
- Distribution plan with at least three channels.
- KPIs and one A/B test on deck.
- File saved at `projects/[business]/lead-magnets/[name].md`. Create the folder if it does not exist.

Ship.
