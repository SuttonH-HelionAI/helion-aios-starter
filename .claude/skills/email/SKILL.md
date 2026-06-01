---
name: email
description: Writes cold outreach, lifecycle sequences, broadcast campaigns, or transactional emails. One skill, four branches. Auto-triggers on phrases like "cold email", "prospecting email", "outbound", "follow-up sequence", "welcome sequence", "nurture sequence", "drip campaign", "lifecycle emails", "email automation", "broadcast", "newsletter", "send a campaign", "failed payment email", "renewal reminder". User-invocable as `/email`.
---

> **Engine:** Growth

# /email

One skill for every email. Routes to Cold, Lifecycle, Broadcast, or Transactional.

---

## Step 0: Context check

Before doing anything, scan the workspace for context. We do not run blind.

1. Read `references/voice.md` plus the `## Voice` section of `CLAUDE.md`. Match every email to that register.
2. Read `context/about-business.md` and `context/about-me.md`. Pull positioning, who you serve, the offer, objections.
3. Check `context/priorities.md` so the email points at the live quarter priority.
4. Check `projects/[current-slug]/brief.md`. If a project is active, pull the campaign brief.
5. Check the user's last message for inline context (trigger, audience, goal).

**Decide which path you are on, say it out loud:**

- **Loaded:** "I have enough context to start. Here is what I pulled: [one-line summary]." Ask only what is missing for this specific run.
- **Partial:** "I have [list]. Missing [list]. Quick three-question intake to fill the gaps."
- **Fresh:** "Context is thin. Run `/onboard` first to fill `context/about-business.md` and `references/voice.md`, then come back. This skill needs grounding to produce real value."

Never proceed without at least Loaded or Partial context.

---

## Step 1: Routing question

Ask once:

> "What kind of email? Pick one: cold outreach (B2B), lifecycle or drip sequence, broadcast or campaign, or transactional."

---

## Branch A: Cold outreach

### A0. Off-ramp gate

Cold outreach is a B2B service or B2B SaaS motion. Before running this branch, confirm the operator actually has one. Ask:

> "Is this a B2B service, agency, or sales-led SaaS with a defined target account list?"

If the answer is no (DTC brand, ecommerce, creator, course, consumer app), do not run this branch. Route them instead:

- DTC or ecommerce → Branch B (Lifecycle, welcome + post-purchase) or Branch C (Broadcast).
- Creator, newsletter, course → Branch C (Broadcast) or Branch B (nurture).
- Consumer app → Branch B (Lifecycle, onboarding + re-engagement).

State the route out loud, then run the correct branch. Forcing a DTC member through cold outreach playbook is malpractice.

### Inputs

1. Who are you writing to (role, company, why them).
2. What outcome you want (reply, meeting, intro, demo).
3. The specific problem you solve for people like them.
4. Your strongest proof point (result, case, credibility signal).
5. Any research signal (funding, hiring, post, tech stack).

### Subject lines

- 2 to 4 words, lowercase, no punctuation, no first name.
- Should look like a colleague sent it: "reply rates", "Q2 forecast", "hiring ops", "trial delays".
- Anti-patterns that drop opens: salesy words, urgency, "!!!", numbers, emojis, fake "Re:".

### Body shape (pick one)

| Shape | Use when |
|---|---|
| Observation → Problem → Proof → Ask | You have a real signal about them |
| PAS (Problem → Agitate → Solution) | Default. Problem-aware prospect |
| BAB (Before → After → Bridge) | Transformation-driven offer |
| QVC (Question → Value → CTA) | C-suite, ultra-brief |
| Mouse Trap (Observation + binary question) | Maximum brevity, 1-2 sentences |

Personalization rule: if you can delete the personalized opening and the email still makes sense, the personalization is fake. The observation must lead into the problem.

### Length and CTA

- 25 to 75 words ships best. Under 75 words gets 83% more replies.
- One ask. Interest-based ("Worth exploring?") beats meeting requests in the first touch.
- C-suite: lower friction ("Curious?"). Mid-level: more specific value.

### Follow-up sequence

5 emails total, each with its own angle. Each must stand alone.

| Touch | Day | Angle |
|---|---|---|
| Initial | 0 | Hook + value prop + soft CTA |
| 1 | 3 | New angle, new value piece |
| 2 | 7-8 | Social proof from similar company |
| 3 | 14 | New insight, resource, or trend |
| 4 | 21-28 | Breakup, acknowledge silence, leave door open |

Breakup template (1-2-3 format works best):

> Since I have not heard back, I will keep it simple. Reply with a number:
> 1. Interested, let's talk.
> 2. Not now, check back in 3 months.
> 3. Not interested, please stop.

If you send a breakup, honor it. Do not contact again.

### Kill list

"I hope this email finds you well", "just checking in", "circle back", "leverage", "synergy", feature dumps, asking for a 30-min call in touch 1.

### Output format

Every cold sequence email writes in this block, no exceptions:

```
Email [#]: [touch label, e.g. Initial / Touch 1 / Breakup]
Trigger / send delay: [Day 0, Day 3, etc.]
Subject: [2-4 words, lowercase]
Preview: [optional, 90-140 chars]
Body: [full copy, 25-75 words]
CTA: [the single ask, interest-based or specific]
Segment / exit: [who gets this, when to stop the sequence]
```

Same shape every email. Operator pastes straight into the sending tool.

---

## Branch B: Lifecycle / drip

### Inputs

1. Trigger (signup, purchase, inactivity, milestone).
2. Goal (activate, convert, retain, win back).
3. What they already know about you when the sequence starts.

### Sequence templates

| Type | Length | Cadence | Goal |
|---|---|---|---|
| Welcome | 5-7 emails | 12-14 days | Activate, build trust, convert |
| Lead nurture | 6-8 emails | 2-3 weeks | Build expertise, convert |
| Onboarding (product) | 5-7 emails | 14 days | Activate to aha moment |
| Re-engagement | 3-4 emails | 2 weeks | Win back or clean list |
| Failed payment | 3-4 emails | 7-14 days | Recover revenue |
| Expired trial | 3-4 emails | 30 days | Convert or learn why |

### Welcome shape (default)

1. Welcome + deliver promised value (immediate)
2. Quick win (day 1-2)
3. Story or origin (day 3-4)
4. Social proof / case study (day 5-6)
5. Overcome top objection (day 7-8)
6. Core feature highlight (day 9-11)
7. Conversion ask with risk reversal (day 12-14)

### Per-email format

- Subject: 40-60 characters. Clear over clever. Specific over vague.
- Preview text: 90-140 chars. Do not repeat the subject.
- Hook (first line): grab attention.
- Body: short paragraphs, 1-3 sentences each. Mobile-first.
- One primary CTA. Buttons for primary, in-text links for secondary.
- Length: 50-125 words transactional, 150-300 educational, 300-500 story-driven.

### Output format

```
Email [#]: [purpose]
Trigger / send delay: [...]
Subject: [...]
Preview: [...]
Body: [full copy]
CTA: [button text] → [destination]
Segment / exit: [...]
```

---

## Branch C: Broadcast / campaign

### Inputs

1. The event or offer.
2. The window (Black Friday, launch week, end of quarter).
3. The audience segment.

### Campaign burst structure

| Email | Timing | Purpose |
|---|---|---|
| Announcement | T-0 | Reveal the offer, the why, the deadline |
| Reminder | Midpoint | Restate value, add proof, name urgency |
| Last chance | Final hours | Short, direct, deadline-led |

### Newsletter rules (if recurring)

- Same send day and time every week.
- One primary CTA. Mix of update, story, link, takeaway.
- Unsubscribe is fine. A clean list is a healthy list.

### Product update emails

- What is new in one sentence.
- Why it matters in one sentence.
- How to use it: direct link.
- Who asked for it: name the request publicly.

### Pricing change emails

- 30-60 days before: announce with the why.
- 14 days before: remind, offer annual lock-in.
- 7 days before: final notice. Be transparent.

### Output format

Every broadcast email writes in this block:

```
Email [#]: [Announcement / Reminder / Last chance]
Trigger / send delay: [T-0, midpoint, final hours]
Subject: [40-60 chars]
Preview: [90-140 chars]
Body: [full copy]
CTA: [button text] → [destination]
Segment / exit: [audience segment, exclusion rules]
```

Same shape every email.

---

## Branch D: Transactional

### Pick the set

Two sets live here. Pick the one that matches the business model.

- **SaaS / subscription:** failed payment, renewal reminder, cancellation survey, NPS.
- **DTC / ecommerce:** abandoned cart, post-purchase day 1 / day 7 / day 30, review request, win-back.

### Failed payment sequence

1. Day 0: friendly notice, assume it was an accident, single CTA to update card.
2. Day 3: reminder, service may interrupt.
3. Day 7: urgent, account will suspend.
4. Day 10-14: final notice, what they lose.

Tone: clear, direct, no guilt. Single CTA per email.

### Renewal reminder

- Send 14 or 30 days before renewal.
- Include date, amount, what is renewing, and the link to update plan or payment.
- Optional upsell only if relevant.

### Cancellation survey

- Send immediately after cancel.
- Ask: primary reason, what could we have done better, would anything change your mind.
- Personal outreach for high-value accounts.

### NPS

- Day 1: one question only, 0-10.
- Promoters (9-10): ask for review or referral.
- Passives (7-8): ask what would make it a 10.
- Detractors (0-6): personal outreach.

### DTC / ecom set

**Abandoned cart (3 emails):**

1. Hour 1: friendly reminder, show the items, single CTA back to cart.
2. Hour 24: address top objection (shipping, sizing, fit), one social proof line.
3. Hour 48-72: light incentive (free shipping, 10% off) if margin allows. Final.

**Post-purchase day 1:** order confirmation already sent. This is the "you made a great choice" note. Set delivery expectation, link to how-to-use content, no upsell yet.

**Post-purchase day 7:** how-to-use or "getting the most out of it" content. Soft cross-sell to one complementary product.

**Post-purchase day 30:** replenishment cue if consumable, or review request if durable. Single CTA.

**Review request:** day 14-30 depending on product use cycle. One question, one link, public review platform. No incentives that violate platform rules.

**Win-back (3 emails over 14 days):**

1. "We miss you" + one-line reminder of what they bought.
2. Show what's new since they last shopped.
3. Final incentive (discount or freebie) with deadline. After this, suppress.

### Output format

Every transactional email writes in this block:

```
Email [#]: [purpose, e.g. Abandoned cart 1 / Failed payment 2]
Trigger / send delay: [event + delay]
Subject: [40-60 chars]
Preview: [90-140 chars]
Body: [full copy, 50-125 words]
CTA: [button text] → [destination]
Segment / exit: [who gets this, when to stop]
```

Same shape every email across both sets.

---

## Hard rules

- Read every email out loud. If it sounds like marketing, rewrite it.
- One job per email. One primary CTA per email.
- Mobile-first. Short paragraphs. White space. Bold sparingly.
- Use "you" more than "I" or "we". Lead with the reader's world.
- No em-dashes. No exclamation points. No AI tells.
- Personalization must connect to the problem. If swapping the name still works, the personalization is fake.
- Honor unsubscribes and breakups. Always.

---

## Benchmarks (cold, 2024-2025)

| Metric | Average | Good | Excellent |
|---|---|---|---|
| Open rate | 27.7% | 40-45% | 50%+ |
| Reply rate | 4-5.8% | 5-10% | 10-15% |
| Bounce rate | 7.5% | <4% | <2% |
| Meeting booking | 0.5-1% | 1-2% | 2.3%+ |

Lifecycle: open 20-40%, click 2-5%, unsubscribe under 0.5%.

---

## When to stop

Definition of done:

- Branch ran end to end and output is on disk under `projects/[slug]/email/`. Create the folder if it does not exist.
- Every email has subject, preview, body, and CTA.
- Sequence has timing, trigger, goal, and exit conditions stated up top.
- Voice matches `references/voice.md`.
- No AI tells survived the final pass.

Ship.
