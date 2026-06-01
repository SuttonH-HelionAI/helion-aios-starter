---
name: ads
description: Runs paid ads end to end. Campaign setup, ad creative generation and iteration, A/B testing. Auto-triggers on phrases like "paid ads", "PPC", "Google Ads", "Facebook ads", "Meta ads", "LinkedIn ads", "TikTok ads", "ROAS", "CPA", "ad campaign", "ad creative", "write me ads", "RSA headlines", "ad variations", "A/B test", "split test", "experiment", "should I test this", "statistical significance". User-invocable as `/ads`.
---

> **Engine:** Growth

# /ads

Three branches, one playbook. Setup, creative, testing.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Read `references/voice.md` plus the `## Voice` section of `CLAUDE.md`. Match every line of ad copy to that register.
2. Read `context/about-business.md` and `context/about-me.md`. Pull positioning, who you serve, the offer, objections.
3. Check `context/priorities.md` so the campaign points at the live quarter priority.
4. Check `connections.md` for the ad and analytics tools the AIOS can reach. If conversion tracking is not defined and validated, ads will spend blind. Flag it.
5. Check `projects/[slug]/ads/` for existing campaign artifacts.
6. Check the user's last message for the platform, the offer, and the goal.

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only what is missing for this specific run.
- **Partial:** "I have [list]. Missing [list]. Quick three-question intake to fill the gaps."
- **Fresh:** "Context is thin. Run `/onboard` first to fill `context/about-business.md` and `references/voice.md`, then come back. This skill needs grounding to produce real value."

Never proceed without at least Loaded or Partial context.

---

## Step 1: Route

Ask exactly one question:

> "What stage are you on? Pick one: setting up a campaign on a platform, generating ad creative (headlines/body/visuals), or testing variants (A/B)."

Run the matching branch. The three branches share Hard Rules at the bottom.

---

## Branch A: Setup

### A1. Pick the platform

| Platform | Best for | Use when |
|---|---|---|
| Google Ads | High-intent search | People already search for the solution |
| Meta | Demand gen, visual products | Strong creative, broad targeting works |
| LinkedIn | B2B, decision-makers | Job-title targeting matters, deal sizes 5k+ |
| TikTok | 18-34 audiences, video | You can ship native vertical video |
| X | Tech audiences, news cycles | Audience is on X and timing matters |

### A2. Lock account structure

Standard hierarchy. No deviation without a reason:

```
Account
  Campaign: [Objective] - [Audience/Product]
    Ad Set: [Targeting variation]
      Ads: 3-5 creative variants
```

**Naming convention, lock it:**

```
[Platform]_[Objective]_[Audience]_[Offer]_[Date]

META_Conv_Lookalike-Customers_FreeTrial_2026Q2
GOOG_Search_Brand_Demo_Ongoing
LI_LeadGen_CMOs-SaaS_Whitepaper_May26
```

### A3. Audience plan

**Lookalikes** seed off best customers by LTV, not all customers. 1% LAL for cold, expand outward if scaling stalls.

**Retargeting** segments by funnel stage:

| Stage | Audience | Message | Window |
|---|---|---|---|
| Hot | Cart, trial, demo | Urgency, objection-handling | 1-7 days |
| Warm | Pricing, feature page | Case studies, comparison | 7-30 days |
| Cold | Any visitor | Education, social proof | 30-90 days |

**Exclusions, mandatory:** existing customers, recent converters (7-14 day window), bounced visitors under 10 seconds, irrelevant pages (careers, support).

### A4. Budget allocation

- **Testing (weeks 1-4):** 70% known/safe campaigns, 30% new audiences and angles.
- **Scaling:** consolidate budget into winners, increase 20-30% at a time, wait 3-5 days between increases for the algorithm to re-learn. Pause anything spending without conversions after 3x target CPA.

### A5. Pre-launch checklist

- [ ] Conversion tracking tested with a real conversion.
- [ ] Landing page loads under 3 seconds.
- [ ] Landing page mobile-friendly.
- [ ] UTM parameters working and consistent.
- [ ] Budget set and naming convention applied.
- [ ] Exclusions audience attached.
- [ ] At least 3 ad variants per ad set.

---

## Branch B: Creative

Two modes. Generate from scratch or iterate from performance data.

### B1. Mode pick

If the campaign is live with 1,000+ impressions per ad, go iterate mode. Otherwise generate.

### B2. Generate mode

**Step 1: Lock 3-5 angles.** Each angle is a different reason to click.

| Angle | Example |
|---|---|
| Pain point | "Stop wasting Mondays on reports" |
| Outcome | "Reports in 5 minutes, not 5 hours" |
| Social proof | "How 10,000+ teams report faster" |
| Curiosity | "The reporting move top ops teams use" |
| Comparison | "Unlike X, we do Y" |
| Identity | "Built for ops leaders, not analysts" |
| Contrarian | "Why dashboards are not the answer" |

**Step 2: Generate variations per angle.** Vary word choice, specificity (numbers vs general), tone (direct, question, command), structure (punchy vs full benefit).

**Step 3: Validate against platform specs:**

| Platform | Element | Limit | Count |
|---|---|---|---|
| Google RSA | Headline | 30 chars | up to 15 |
| Google RSA | Description | 90 chars | up to 4 |
| Meta | Primary text | 125 visible, 2,200 max | front-load the hook |
| Meta | Headline | 40 chars | 1 |
| LinkedIn | Intro text | 150 recommended | 1 |
| LinkedIn | Headline | 70 recommended | 1 |
| TikTok | Ad text | 80 recommended | 1 |
| X | Tweet text | 280 chars | 1 |

Flag anything over limit. Provide a trimmed alternative.

**Step 4: Organize for upload.** Group by angle, label headline and description with char counts, deliver in CSV for bulk upload when count is over 10.

### B3. Iterate mode

1. Pull top 20% by the metric that matters (ask which). Name winning themes, structures, and word patterns.
2. Pull bottom 20%. Name what is falling flat (too generic, wrong tone, no specificity).
3. Generate new wave: double down on winners with fresh phrasing, extend angles into adjacent variations, test 1-2 new angles, avoid loser patterns.
4. Log the round (date, top performers, patterns, variations shipped, angles retired) into the campaign folder.

### B4. Creative best practices

- **Image:** product UI, before/after, stat as the visual, real faces over stock, text overlay under 20%.
- **Video 15-30 sec:** pattern interrupt (0-3), relatable pain (3-8), product solving it (8-20), CTA (20-30). Captions always. Vertical for Stories/Reels, square for feed. Native beats polished.
- **Avoid:** all caps, vague claims, clickbait the page cannot deliver, RSA headlines that only work when paired.

---

## Branch C: Testing (A/B)

### C1. Lock the hypothesis

Weak: "Changing the button might increase clicks."

Strong:

```
Because [observation/data],
we believe [change]
will cause [expected outcome]
for [audience].
We will know this is true when [primary metric] moves by [X%].
```

If the hypothesis cannot be written in that format, the test is not ready.

### C2. Pick metrics

- **Primary:** one metric, tied to business value. The call goes on this.
- **Secondary:** 2-3, support interpretation.
- **Guardrails:** things that must not get worse (refund rate, support tickets, churn).

### C3. Calculate sample size

Quick reference at 95% confidence:

| Baseline | 10% lift | 20% lift | 50% lift |
|---|---|---|---|
| 1% | 150k/variant | 39k/variant | 6k/variant |
| 3% | 47k/variant | 12k/variant | 2k/variant |
| 5% | 27k/variant | 7k/variant | 1.2k/variant |
| 10% | 12k/variant | 3k/variant | 550/variant |

If the math says the test needs 6 weeks at current traffic, the test is not ready. Drive more traffic first or pick a bolder change.

### C4. Design the variant

Change one thing. If three things change, you cannot attribute the result.

**What to vary:** headline, hero visual, CTA copy, CTA placement, social proof presence, pricing presentation.

**Traffic split:** 50/50 default. Conservative 90/10 only when downside risk is high. Ramping (5% to 50%) only when there is technical risk.

### C5. Run and analyze

Pre-launch: hypothesis documented, primary metric defined, sample size calculated, variants QA'd on desktop and mobile, tracking validated end to end. During: monitor guardrails, do not peek and stop early, document external events.

**Peeking rule:** stopping early because it looks like a winner produces false positives. Commit to sample size.

Analysis order: sample size hit, statistically significant (p and CI), effect size meaningful, secondary metrics aligned, guardrails clean, segment differences. Outcomes: significant winner ships, significant loser stays as control with notes, no significant difference means more traffic or bolder change, mixed signals means segment before deciding.

### C6. Document the test

Write to `projects/[slug]/ads/experiments/[name].md`. Create the folder if it does not exist:

```
## [Test Name]
Date: [date]
Hypothesis: [hypothesis]
Sample size: [n per variant]
Result: [winner/loser/inconclusive] - [metric] changed by [X%] (95% CI: [range], p=[value])
Guardrails: [metrics and their outcomes]
Segment deltas: [notable differences]
Why it worked/failed: [analysis]
Pattern: [reusable insight]
Apply to: [other pages/flows]
Status: [implemented / parked / follow-up test]
```

Build a playbook of patterns over time. That is the compounding asset.

---

## Optimization levers (any branch)

- **CPA too high:** check landing page first, tighten targeting, test new angles, refresh creative, adjust bid.
- **CTR low:** creative not resonating, audience mismatch, or fatigue. Test hooks, refine targeting, then refresh.
- **CPM high:** audience too narrow, competition, or low relevance. Expand, try different placements, improve fit.

---

## Hard rules

- No campaign launches without validated conversion tracking. None.
- One angle change per creative test. One variable change per A/B test.
- Exclude existing customers and recent converters from every prospecting campaign.
- 50+ conversions before switching to automated bidding.
- Allow 1,000+ impressions before judging a creative.
- Never stop a test before sample size unless guardrails are bleeding.
- No AI tells in any output.

---

## When to stop

Definition of done:

- The right branch ran end to end.
- Spec, creative, or experiment doc exists in `projects/[slug]/ads/`.
- Conversion tracking confirms data is flowing.
- The operator can name the daily metric to watch and the weekly metric to call wins on.

Ship.
