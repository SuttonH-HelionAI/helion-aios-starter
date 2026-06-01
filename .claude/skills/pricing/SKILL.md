---
name: pricing
description: Builds and restructures pricing strategy, tiers, value metrics, and pricing page specs. Auto-triggers on phrases like "pricing", "tiers", "freemium", "free trial", "value metric", "Van Westendorp", "willingness to pay", "price increase", "how much should I charge", "pricing page", "annual vs monthly". User-invocable as `/pricing`.
---
> **Engine:** Growth

# /pricing

You design pricing that captures value, not pricing that copies competitors. Three modes: design from scratch, restructure existing tiers, stage a price increase.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Check `context/about-business.md` and `context/about-me.md`. Pull positioning, ICP, JTBD, competitors, value themes, what you sell, who you serve.
2. Check `references/voice.md` and the `## Voice` section of `CLAUDE.md`. Pull the register to write in.
3. Check `projects/[business]/pricing/pricing-strategy.md` and the live pricing page. If found, this run is an audit or restructure.
4. Check the user's last message for current price, current conversion, and the goal.

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only what is missing for this specific run.
- **Partial:** "I have [list]. Missing [list]. Quick four-question intake to fill the gaps."
- **Fresh:** "Workspace has no context yet. Run `/onboard` first, takes 10 minutes, then come back. This skill needs grounding to produce real value."

Never proceed without at least Loaded or Partial context.

---

## Step 1: Four-question intake

Ask one at a time:

1. "What is the business model and motion? SaaS, marketplace, service, DTC. Self-serve, sales-led, hybrid."
2. "What is the primary value the customer gets, and what alternative would they pick if you did not exist?"
3. "What is current ARPU, current conversion rate, and current churn? If any."
4. "What is the goal of this run? Set pricing, restructure tiers, raise prices."

Route on answer four.

---

## Step 2: Lock the three pricing axes

Every pricing decision rolls up to three things. Name them out loud before sketching tiers.

| Axis | Question | Output |
|---|---|---|
| Packaging | What is in each tier? | Feature and limit map |
| Pricing metric | What do you charge for? | Per user, per usage, per contact, flat |
| Price point | How much per unit? | Dollar amount per tier |

Set the floor and ceiling before picking the number.

- **Floor:** The next best alternative. Includes DIY and do-nothing.
- **Ceiling:** Customer's perceived value. The most they could rationally pay.
- **Your price:** Between the two. Cost to serve is a baseline, not the basis.

---

## Step 3: Pick the value metric

The value metric is what the price scales with. Ask: "As a customer uses more of this, do they get more value?" If yes, it is a viable metric.

| Metric | Best for | Examples |
|---|---|---|
| Per user / seat | Collaboration tools | Slack, Notion |
| Per usage | Variable consumption | AWS, Twilio, OpenAI |
| Per contact or record | CRM, email tools | Mailchimp, HubSpot |
| Per transaction | Payments, marketplaces | Stripe |
| Per feature | Modular products | HubSpot add-ons |
| Flat fee | Simple products | Basecamp |

Strong metrics align price with value, are easy to explain, scale with the customer, and are hard to game. If your metric fails any of those, swap it.

---

## Step 4: Design the tiers

Default to a three-tier structure. The template depends on the business model from Step 1.

### Branch A: SaaS (Good-Better-Best)

| Tier | Role | Price anchor |
|---|---|---|
| Good | Entry. Core features. Hard limits. Drives volume. | Low |
| Better | Recommended. Full features. Reasonable limits. | The anchor |
| Best | Premium. Everything plus advanced. Drives ARPU. | 2x to 3x Better |

### Branch B: DTC and physical products (Bundle / Subscription / One-time)

| Tier | Role | Price anchor |
|---|---|---|
| One-time | Single unit. Trial purchase. Drives first conversion. | Base price |
| Subscription | Recurring delivery, 10-20% off, cancel anytime. The recommended. | 0.8x to 0.9x of one-time |
| Bundle | Multi-product or multi-month pack. Drives AOV and LTV. | 2x to 4x one-time, with 15-25% bundle discount |

The recommended tier is the subscription. The bundle is the anchor that makes the subscription feel small. AOV target: bundle at 2-3x the base SKU.

### Branch C: Services and agencies (Project / Retainer / Productized)

| Tier | Role | Price anchor |
|---|---|---|
| Project | One-time scoped engagement. Drives trial relationships. | Defined scope, fixed fee |
| Retainer | Monthly recurring, capped hours or capped deliverables. The recommended. | 1.5x to 3x project monthly equivalent |
| Productized | Fixed-scope, fixed-price, fixed-timeline package. Drives velocity and margin. | Premium per-deliverable rate |

For services, productized tiers (the "Done in 14 days" or "Audit + 3 sprints" packages) carry the highest margin and the strongest positioning. Lead with a productized tier when the buyer wants certainty over flexibility. Creators selling courses, coaching, or done-with-you offers map cleanly into this branch: course = project, group coaching = retainer, 1:1 done-for-you = productized.

**Worked creator and agency example:** A solo creator selling email-list growth services builds three tiers. Project: "Newsletter audit and 30-day rebuild plan, $1,500 flat." Retainer: "Newsletter operator, 4 sends per month, $2,500/mo, 3-month minimum." Productized: "Done-with-you launch sprint, 6 weeks, $7,500, includes audit + rebuild + first 4 sends + handoff Loom." The retainer is the recommended tier. The productized sprint is the anchor that makes the retainer feel like a reasonable trial commitment.

### Tier differentiation, pick at least two (all branches)

- Feature gating (basic vs advanced) or scope gating (deliverable count).
- Usage limits (same features, different ceilings) or volume limits (units, hours, sends).
- Support level (community to email to dedicated, or async to weekly call to Slack channel).
- Access (API, SSO, custom branding, audit logs, or exclusivity, white-label rights, source files).

Highlight the recommended tier. Make the middle the obvious value. Use the top tier as the anchor that makes the middle feel cheap.

---

## Step 5: Find the price point

Two paths depending on data.

**Path A: With data.** Run a Van Westendorp survey. Four questions, send to 50+ qualified prospects or customers:

1. At what price is this too expensive that you would not consider it?
2. At what price is this so cheap you would question the quality?
3. At what price does it start to feel expensive but you might still consider it?
4. At what price does it feel like a bargain?

Plot the cumulative curves. The intersection of "too cheap" and "too expensive" is the optimal range. The intersection of "expensive" and "bargain" is the acceptable range.

**Small-list fallback (under 200 subscribers or customers):** if you cannot get 50 survey responses, run 10 to 15 customer or prospect calls and ask the same four questions verbatim, one at a time, on the call. Note the answer, do not negotiate. After 10 calls you will see clusters around two or three price points, those are your optimal and acceptable bands. Slower, noisier, still defensible. Beats picking a number out of the air.

Pair with MaxDiff if you also need to learn which features carry the most value: show sets of features, ask most and least important, score the deltas.

**Path B: No data, pre-launch.** Use the competitor band as a starting range, then pick where you land inside the band based on positioning. Premium positioning means top quartile of the band. Value positioning means bottom quartile. Default to charging more than feels comfortable. The downside of underpricing is bigger than the downside of pricing high and getting a few "too expensive" responses.

---

## Step 6: Price increase mode (only if applicable)

Use this when restructuring with existing customers on legacy plans.

**Signals you are ready for an increase:**

- Conversion rate over 40 percent and prospects do not flinch.
- Monthly churn under 3 percent.
- Significant value added since the last pricing move.
- Competitors have moved up.

**Increase strategies:**

| Strategy | Use when |
|---|---|
| Grandfather existing customers | You want zero existing-customer churn. Slowest path but lowest risk. |
| Delayed increase, announced 3-6 months out | You want notice and goodwill. |
| Tied to value, raise price plus add features | You can ship a real new feature inside the window. |
| Plan restructure | Tiers are wrong, not just prices. Rebuild from scratch. |

Always pair with a comms plan: who hears first, what the message is, how the rollback works if churn spikes.

---

## Step 7: Pricing page spec

Hand design and copy a spec, not a draft page. Write to `projects/[business]/pricing/page-spec.md`.

**Above the fold:**

- Tier comparison table with three columns max.
- Recommended tier highlighted with a label.
- Monthly and annual toggle, annual default if discount is meaningful.
- Primary CTA per tier, value-focused copy ("Start Free Trial," "Get Started," "Talk to Sales").

**Below the fold:**

- Feature comparison table that lists every feature once with checks.
- Who each tier is for, one line each.
- FAQ section that addresses the top five real objections.
- Annual discount callout, 17-20% is the conventional anchor.
- Money-back or cancel-anytime line.
- Customer logos or two strong testimonials near the CTA.

**Pricing psychology checklist:**

- Anchor the highest tier first when read top to bottom or left to right.
- Make the middle tier the obvious best value. Decoy effect.
- Charm pricing ($49) for value-positioned products, round pricing ($50) for premium.
- Avoid splitting the cognitive load. One price per tier on first read, details on hover.

---

## Output format

Write two files. Create the `projects/[business]/pricing/` folder if it does not exist.

1. `projects/[business]/pricing/pricing-strategy.md` with value metric, tier table, price points, reasoning, alternatives considered, rollout plan.
2. `projects/[business]/pricing/page-spec.md` with the page sections, copy, and CTA logic.

End with a 30-day rollout plan: announcement copy, internal alignment list, the cohort that gets grandfathered, the metric to watch.

---

## Hard rules

- Price between alternatives and perceived value, never against cost to serve.
- One value metric per pricing model. Two metrics confuse buyers.
- Three tiers default. Four only if you have a real enterprise offer.
- Never ship a price increase without a comms plan.
- Annual toggle defaults to annual when the discount is real.
- No AI tells in any output.

---

## When to stop

Definition of done:

- Strategy doc exists with value metric, tier table, price points, reasoning.
- Page spec exists ready for design and copy.
- Rollout plan names dates, comms, grandfathering rules.
- The operator can explain "why this costs what it costs" in one sentence.

Ship.
