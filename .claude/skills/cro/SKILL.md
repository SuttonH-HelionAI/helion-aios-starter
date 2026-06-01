---
name: cro
description: Conversion optimization across pages, signup flows, onboarding, popups, and paywalls. Auto-triggers on phrases like "CRO", "improve conversions", "this page is not converting", "signup conversions", "registration friction", "activation rate", "users not activating", "popup", "modal", "exit intent", "paywall", "upgrade screen", "freemium conversion", "form abandonment". User-invocable as `/cro`.
---
> **Engine:** Growth

# /cro

Five branches: full page, signup flow, onboarding/activation, popup or modal, paywall or upgrade. One skill that fixes whatever surface is bleeding.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Check `context/about-business.md` and `context/about-me.md`. Pull positioning, ICP, JTBD, objections, what you sell, who you serve.
2. Check `references/voice.md` and the `## Voice` section of `CLAUDE.md`. Pull the register to write in.
3. Check `context/priorities.md` for what matters this quarter. If conversion events are not defined anywhere, recommendations will guess.
4. Check the user's last message for URL, screenshot, current conversion rate, and traffic volume.

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only what is missing for this specific run.
- **Partial:** "I have [list]. Missing [list]. Quick three-question intake to fill the gaps."
- **Fresh:** "Workspace has no context yet. Run `/onboard` first, takes 10 minutes, then come back. This skill needs grounding to produce real value."

Never proceed without at least Loaded or Partial context.

**One branch per run, no exceptions.** If the user lists 2+ surfaces, ship audit on the most-bleeding one only, queue the rest for a follow-up run. State out loud: "Running [branch] this session. Queued for next run: [list]." Never attempt parallel branches in one invocation.

---

## Step 1: Route

Ask exactly one question:

> "What are we optimizing? Pick one: a full page (homepage/landing/pricing), a signup or registration flow, post-signup activation, a popup/modal, or a paywall/upgrade flow."

Run the matching branch.

---

## Branch A: Full page

### A0. Stop check

Before walking dimensions, confirm: page URL accessible, current conversion rate, primary traffic source, and the single primary conversion event. If any one is unknown, stop and ask. Do not recommend headline rewrites or CTA changes against a phantom baseline.

### A1. Identify the page type and goal

Homepage, landing, pricing, feature, blog, about. Single primary conversion. Where the traffic comes from (organic, paid, email, social) shapes message match.

### A2. Walk seven dimensions in order of impact

**1. Value proposition clarity.** Can a visitor understand what this is and why they should care in 5 seconds? Benefit-focused, not feature-focused. Customer language, not company jargon.

**2. Headline effectiveness.** Communicates the core value prop. Specific. Matches the traffic source. Patterns that work: outcome-focused ("Get X without Y"), specificity ("Cut reporting time 75%"), social proof ("Join 10,000+ teams").

**3. CTA placement, copy, hierarchy.** One clear primary action above the fold. Button copy communicates value, not just action ("Start Free Trial" beats "Submit"). Repeated at key decision points. Primary vs secondary hierarchy is clear.

**4. Visual hierarchy and scannability.** Skimmer can get the message. Important elements visually prominent. White space. Images support, not distract.

**5. Trust signals and social proof.** Real logos near CTAs. Testimonials with names and photos. Case study numbers. Review scores. Security badges where relevant.

**6. Objection handling.** Address price, fit, implementation, risk. FAQ, guarantees, comparison content, process transparency.

**7. Friction points.** Form fields, navigation, mobile experience, load time, anything that makes the visitor think.

### A3. Page-type playbooks

| Type | Focus |
|---|---|
| Homepage | Clear positioning for cold visitors, fast path to common conversion, handle both ready-to-buy and still-researching |
| Landing | Message match with traffic source, remove nav, complete argument on one page, single CTA |
| Pricing | Plan comparison, recommended tier called out, address "which plan is right for me" anxiety |
| Feature | Connect feature to benefit, use cases, clear path to try or buy |
| Blog | Contextual CTAs matching topic, inline CTAs at natural stops |

### A4. Output

Write a single file to `projects/[business]/cro/[slug]/audit.md` with this fixed table of contents in this order:

1. **Quick wins**: changes shippable today with likely impact.
2. **High-impact changes**: bigger lifts that need design or copy effort.
3. **Tests**: items worth A/B testing rather than assuming, with hypothesis, primary metric, sample-size note.
4. **Spec**: redesigned page brief with copy alternatives (2-3 options for headline and primary CTA with rationale), section order, mobile notes, tracking events.

Create the folder if it does not exist. One file, four sections, in that order. No other output artifacts from this branch.

---

## Branch B: Signup flow

### B0. Stop check

Before recommending field cuts or step reorders, confirm: current signup completion rate, field-level drop-off (if measured), required vs optional flags, and whether email verification is on. If completion rate is unknown, stop and ask for it. Do not recommend field cuts blind.

### B1. Read the flow

Count steps. Count fields. Note which are required. Ask for the current completion rate and field-level drop-off if available.

### B2. Field-by-field grade

For each field ask: do we truly need this before they can use the product? Can we defer through progressive profiling? Can we infer it?

| Priority | Fields |
|---|---|
| Essential | Email or phone, password |
| Often needed | Name |
| Deferrable | Company, role, team size, phone, address |

**Field rules:**

- Email: single field, inline format validation, typo correction (gmial to gmail), clear errors.
- Password: show toggle, requirements shown upfront, allow paste, strength meter beats rigid rules.
- Name: single "Full name" beats first/last split unless personalization needs the split.
- Social auth: prominent placement, often outperforms email. B2C uses Google, Apple, Facebook. B2B uses Google, Microsoft, SSO.
- Phone: defer unless verification or sales calling is required.
- Company: defer, auto-suggest, or infer from email domain.

### B3. Single-step vs multi-step

| Pattern | Use when |
|---|---|
| Single-step | 3 or fewer fields, simple B2C, high-intent visitors |
| Multi-step | 4+ fields, B2B segmentation needed, info types are different |

**Multi-step best practices:** progress indicator, easy questions first, hard questions later, allow back navigation, save progress on refresh.

**Progressive commitment:** email first (lowest barrier), then password and name, then customization (optional).

### B4. Trust and microcopy

- "No credit card required" if true.
- Trial length in the CTA: "Start 14-day free trial" beats "Get started".
- "We never share your email" near the form.
- Labels always visible. Placeholders are for examples, not labels.
- Error messages specific ("Email already registered. Sign in instead?") not generic.

### B5. Mobile

44px+ touch targets. Correct keyboard types (email, tel). Autofill on. Single column. Sticky CTA. Test on real devices.

### B6. Output

Write a single file to `projects/[business]/cro/signup/audit.md` with this fixed table of contents:

1. **Quick wins**: field cuts, label fixes, social auth placement, microcopy.
2. **High-impact changes**: single vs multi-step rework, validation logic, mobile flow.
3. **Tests**: hypothesis, primary metric, sample-size note for each test idea.
4. **Spec**: redesigned form with field order, labels, placeholders, button copy, error states, mobile notes.

Create the folder if it does not exist. One file, four sections, in that order.

---

## Branch C: Onboarding / activation

### C0. Stop check

Before mapping the flow, confirm: the defined activation event, current % of signups who hit it, time-to-activation median, and step-level drop-off if measured. If activation is undefined, stop and define it with the operator first. Recommending checklist items against an unknown aha moment is wasted work.

### C1. Define activation

What action correlates most with retention. The "aha moment". Examples:

| Product | Aha |
|---|---|
| Project management | Create first project + invite teammate |
| Analytics | Install tracking + see first report |
| Design tool | Create first design + export or share |
| Marketplace | Complete first transaction |

Track: % of signups who hit activation, time to activation, steps to activation, activation by cohort.

### C2. Map the flow

First 30 seconds matters most. Three patterns:

| Approach | Best for | Risk |
|---|---|---|
| Product-first | Simple B2C, mobile | Blank slate overwhelm |
| Guided setup | Products needing personalization | Adds friction before value |
| Value-first (demo data) | Products with rich UIs | May not feel "real" |

Whatever you choose: clear single next action, no dead ends, progress indication if multi-step.

### C3. Use the right primitive

- **Onboarding checklist:** 3-7 items, ordered by value, quick wins first, dismissable. Use when there are multiple setup steps to discover.
- **Empty states:** explain the area, show what it looks like with data, clear primary action, optional pre-populated example.
- **Tooltips / tours:** max 3-5 steps, dismissable, do not repeat for returning users. Use for non-self-evident features.

### C4. Multi-channel coordination

Email reinforces in-app, does not duplicate it:

| Trigger | Email |
|---|---|
| Signup | Welcome, single next step |
| Incomplete onboarding 24h | Reminder of value, address blockers |
| Activation hit | Celebration + the next milestone |
| Stalled 3-7 days | Re-engagement, offer help, address objections |

### C5. Output

Write a single file to `projects/[business]/cro/onboarding/audit.md` with this fixed table of contents:

1. **Quick wins**: first-30-seconds fixes, empty state copy, checklist tweaks.
2. **High-impact changes**: flow pattern shift (product-first vs guided vs demo data), email trigger additions.
3. **Tests**: hypothesis, primary metric, sample-size note for each.
4. **Spec**: activation goal stated, step-by-step flow, checklist items, empty state copy, email triggers, metrics plan, drop-off funnel with target lifts.

Create the folder if it does not exist. One file, four sections, in that order.

---

## Branch D: Popups and modals

### D0. Stop check

Before designing the popup, confirm: traffic volume to the page that hosts it, current capture rate or baseline, audience segment, and whether existing popups already fire on that page. If traffic is under 500 sessions/week or baseline is unknown, stop and surface that. Popups need volume to learn from.

### D1. Set the goal

Email capture, lead magnet, discount, announcement, exit save, feature promo, feedback. One purpose per popup.

### D2. Pick the trigger

| Trigger | Use for | Note |
|---|---|---|
| Time delay 30-60 sec | General visitors | Avoid 5-second popups |
| Scroll 25-50% | Long-form content | Indicates engagement |
| Exit intent | E-commerce, lead gen | Last chance, mobile uses back button or scroll-up alt |
| Click-triggered | Lead magnets, gated content | Zero annoyance, self-selected |
| Page count | Multi-page research behavior | Reward investigation |
| Behavior-based | Cart abandon, pricing page | High-intent segments |

### D3. Design

**Visual hierarchy:** headline (largest), value prop, form/CTA, close (easy to find).

**Sizing:** 400-600px on desktop, do not cover full screen. Mobile uses bottom slide-up or center, never full-screen.

**Close button:** visible top right, large enough to tap, "No thanks" text link, click-outside-to-close.

**Imagery:** product preview or face if relevant. Minimal for speed. Copy alone often wins.

### D4. Copy formulas

| Element | Pattern |
|---|---|
| Headline | Benefit-driven ("Get X in Y"), question, command, social proof, curiosity |
| Subhead | Expand the promise, address objection ("No spam, ever"), set expectation ("Weekly, 5 min") |
| CTA | First person ("Get My Discount"), value-focused ("Send Me the Guide") |
| Decline | Polite, not guilt-trippy ("No thanks") |

### D5. Frequency rules

- Max once per session.
- Remember dismissals in cookie or localStorage.
- 7-30 days before showing again.
- Exclude converted users and recent dismissals.
- Skip checkout and conversion flows.

### D6. Compliance and accessibility

GDPR consent language, link to privacy, no pre-checked opt-ins. Keyboard navigable, focus trap while open, screen reader compatible. Avoid full-screen interstitials on mobile (SEO penalty).

### D7. Output

Write a single file to `projects/[business]/cro/popup/audit.md` with this fixed table of contents:

1. **Quick wins**: copy fixes, close button visibility, frequency cap adjustments.
2. **High-impact changes**: trigger shift, targeting segment, design rework.
3. **Tests**: hypothesis, primary metric, sample-size note for each.
4. **Spec**: type, trigger, targeting rules, frequency, copy (headline, subhead, CTA, decline), design notes, expected conversion benchmark (2-5% email, 3-10% exit intent, 10%+ click-triggered).

Create the folder if it does not exist. One file, four sections, in that order.

---

## Branch E: Paywalls and upgrade flows

### E0. Stop check

Before designing the screen, confirm: the trigger point, current free-to-paid conversion rate, whether the user has hit the aha moment before the paywall fires, and the price points already in market. If aha-moment status is unknown, stop and ask. Paywalls in front of value convert at 1%.

### E1. Identify the trigger point

| Trigger | When |
|---|---|
| Feature gate | User clicks a paid-only feature |
| Usage limit | User hits a quota |
| Trial expiration | Days remaining on free trial |
| Time-based | Gentle prompt after X days of free use |

### E2. Confirm value has been delivered

Hard rule: never ask before the aha moment. The upgrade should feel like a natural next step. If the user has not experienced value yet, the paywall converts at 1%.

### E3. Build the screen

Required components:

1. **Headline:** focus on what they get. "Unlock [feature] to [benefit]."
2. **Value demonstration:** preview, before/after, "With Pro you could..."
3. **Feature comparison:** highlight key differences. Current plan marked.
4. **Pricing:** clear, simple. Annual vs monthly toggle.
5. **Social proof:** quote or "X teams use this."
6. **CTA:** specific and value-oriented ("Start Getting [Benefit]").
7. **Escape hatch:** clear "Not now" or "Continue with Free." No dark patterns.

### E4. Patterns by trigger

**Feature lock:**

```
This feature is on Pro
[Preview]
[Feature] helps you [benefit]
- Capability
- Capability
[Upgrade to Pro - $X/mo]
[Maybe Later]
```

**Usage limit:**

```
You hit your free limit
[Progress at 100%]
Free: 3 projects | Pro: Unlimited
[Upgrade]  [Delete a project]
```

**Trial expiration:**

```
Trial ends in 3 days
What you'll lose: [features used]
What you accomplished: [projects, count, etc.]
[Continue with Pro]
[Remind me later]  [Downgrade]
```

### E5. Frequency

Limit per session. Cool-down after dismiss (days, not hours). Track annoyance signals. Never block critical flows.

### E6. Test what matters

| Variable | Why |
|---|---|
| Trigger timing | When in the journey it fires |
| Headline | Benefit framing |
| Price presentation | Anchoring and decoy |
| Feature emphasis | Which capability sells the upgrade |
| Trial length | 7 vs 14 vs 30 day |

Metrics: paywall impression rate, click-through to upgrade, upgrade completion rate, revenue per user, post-upgrade churn.

### E7. Output

Write a single file to `projects/[business]/cro/paywall/audit.md` with this fixed table of contents:

1. **Quick wins**: headline rewrites, CTA copy, decline language, social proof placement.
2. **High-impact changes**: trigger shift, value-delivered gate, pricing presentation.
3. **Tests**: hypothesis, primary metric, sample-size note for each test in the backlog.
4. **Spec**: trigger map, full screen spec, copy, frequency rules, post-upgrade flow notes.

Create the folder if it does not exist. One file, four sections, in that order.

---

## Hard rules (apply to every branch)

- Read the context docs first. Recommendations grounded in ICP and JTBD beat generic best practices. If you have the `/icp` skill installed, its output sharpens every branch.
- Recommendations get prioritized: quick wins, high-impact, test ideas. Never a single flat list.
- Every copy alternative comes with rationale, not vibes.
- Never recommend dark patterns: hidden close buttons, guilt-trip decline copy, pre-checked opt-ins, blocked critical flows.
- Mobile is not an afterthought. Audit on mobile or do not ship.
- No AI tells in any output.

---

## When to stop

Definition of done:

- The right branch ran end to end.
- Audit and recommendations exist in `projects/[business]/cro/[surface-slug]/`.
- The operator knows which two changes to ship this week and which two to test.
- Tracking exists for the metrics that will tell you if it worked.

Ship.
