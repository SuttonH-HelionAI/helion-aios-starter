---
name: offer
description: Use when someone wants to build, sharpen, or rescue an offer, or asks for a "Grand Slam Offer", "Godfather offer", "irresistible offer", "value stack", "value equation", "offer they cannot refuse", or says "build my offer", "make this offer irresistible", "why is my offer not selling", "package my offer", "what should I charge for this". Builds ONE irresistible offer for ONE buyer: scored on Hormozi's Value Equation, stacked Godfather-style like Sabri Suby, with a guarantee, a name, scarcity, bonuses, and a price. Writes context/offer.md. User-invocable as /offer.
argument-hint: [offer name, or "the offer for <buyer>"]
---

> **Engine:** Growth

# /offer: the Grand Slam / Godfather offer builder

You build ONE irresistible offer for ONE buyer. The kind a right-fit buyer would feel stupid saying no to. This fuses Alex Hormozi's Value Equation and Grand Slam Offer (100M Offers) with Sabri Suby's Godfather Offer (Sell Like Crazy). One offer, one buyer, fully stacked, scored, named, and priced.

## The one test everything rolls up to

> **"Would a right-fit buyer feel stupid saying no?"**

If the answer is not a clear yes, the offer is not done. Return to this test after every step.

## Step 0: Load the buyer and the business

Read first, in this order:
- `context/icp.md`: the dream buyer, their dream outcome, their pains, what they have already tried, their exact language. THIS is who the offer is for. If it does not exist, stop and tell the user to run `/icp` first. An offer is only as good as the buyer it is built for.
- `context/about-business.md`: what you sell, how you deliver, your price range, any existing offer.
- `context/about-me.md` and `references/voice.md`: so the offer reads in the founder's voice.

Then state in one line who this is for: pull the ICP's name and their dream outcome. If `context/about-business.md` already describes a live offer, say so. You will diagnose it first (Step 5) before rebuilding the weak parts. If there is no offer yet, you build fresh from the dream outcome.

## Step 1: The dream outcome

Hormozi calls it the dream outcome. Sabri calls it the massive promise. Same thing: the result they desperately want.

State it in the buyer's words, specific and vivid. Not "get more leads," but "wake up to five sales calls booked before you open your laptop." Push past the feature to the felt, status-level result. One sentence. This is the spine of the whole offer.

## Step 2: List every problem between them and the dream

Brainstorm every problem, fear, and obstacle standing between the buyer and the dream outcome. Be exhaustive, aim for 10 or more. Group them: before they start, during the work, after they get a result. Each problem is a future piece of the offer. Do not solve yet, just list.

## Step 3: Turn every problem into a solution

Flip each problem into a solution statement: what you would give them or do for them to remove it. This is the raw deliverable list. One solution per problem.

## Step 4: Trim and stack (the value stack)

For each solution, brainstorm delivery vehicles, the ways you could actually deliver it: one-on-one, group, a course, a template, done-for-you, a tool, a checklist, a community, a live call.

Now TRIM. Cut anything that is high cost to you AND low value to them. Keep the high-value items, especially the ones that are high value to them and low cost to you (those are gold). What remains is your stack.

Assign each stacked item a real, defensible standalone dollar value. Sum them. **The total stacked value must dwarf the price, 10x or more** (Sabri's rule). If it does not, keep stacking or cut the price. List the stack with values and the total.

## Step 5: Score it on the Value Equation

Hormozi's Value Equation:

```
            Dream Outcome  x  Perceived Likelihood of Achievement
Value  =  -----------------------------------------------------------
                  Time Delay  x  Effort and Sacrifice
```

Score the current offer 1 to 10 on each of the four levers:
- **Dream Outcome**: how big and desirable is the promise?
- **Perceived Likelihood**: how sure is the buyer it will work for THEM? (proof, track record, guarantee)
- **Time Delay**: how long until they get a result, especially the first win? (lower is better)
- **Effort and Sacrifice**: how much work and pain falls on them? (lower is better)

Find the WEAKEST lever and fix it before going further:
- Low likelihood: add proof, a case study, a stronger guarantee, risk reversal.
- High time delay: add a fast first win, a "results in X days" path, a done-for-you fast start.
- High effort: remove steps, do more for them, add tools and templates, "we handle X so you do not have to."

State the weak lever and the before/after fix. A weak lever sinks the whole offer.

## Step 6: The guarantee (reverse the risk)

Design the strongest HONEST guarantee. Pick the type:
- **Unconditional**: money back, no questions. The boldest.
- **Conditional**: "do X, Y, Z, and if you do not get [result], you get [refund / we work free until you do / you pay nothing]."
- **Anti-guarantee**: all sales final. Only for high-ticket or genuinely exclusive offers.
- **Implied / performance**: you win when they win (revenue share, pay-on-results).

Write it in one or two plain sentences. The goal: make saying yes feel safe and saying no feel like the real risk.

## Step 7: Scarcity and urgency (real, never fake)

Add a TRUE reason to act now. Scarcity (limited spots, units, a capped cohort) or urgency (a real deadline, price rising, a bonus window closing, a season). It must be real. Fake limits kill trust and the brand. If none exists naturally, build an honest one: a real cohort cap, a real fast-action bonus that actually expires. State it plainly.

## Step 8: Bonuses

Add 2 to 4 bonuses. Each one kills a specific remaining objection or speeds up the result. For each: name it, give it a standalone dollar value, and tie it to the exact objection it removes. Bonuses often sell the offer harder than the core. Stack their value into the total.

## Step 9: Name it (MAGIC)

Name the offer with Hormozi's MAGIC formula:
- **M**agnetic reason why (why this, why now)
- **A**vatar (who it is for)
- **G**oal (the dream outcome)
- **I**nterval (the time frame)
- **C**ontainer (the word: challenge, blueprint, system, accelerator, intensive, sprint)

Generate 3 names. Pick the strongest. No hype words, no AI tells.

## Step 10: Price and frame it

Set or sanity-check the price against the stacked value. Price is a fraction of total value, usually 1/5 to 1/10. Then frame it three ways:
- Anchor against the total stack value.
- Anchor against the cost of NOT solving it (pull the ICP's cost of inaction: money, time, status lost over 12 months).
- Anchor against the alternatives (hiring, doing nothing, a competitor).

Add payment framing if it helps (one-time vs split). State the price and justify it in the buyer's terms.

## Step 11: Write the offer doc

Write everything to `context/offer.md` (create the file). This is now canonical: `/copy`, `/ads`, `/email`, `/pricing`, and `/lead-magnets` all read it. Use the template below. Then offer to append a one-line summary to the Knowledge base section of `CLAUDE.md` so the whole OS knows the offer.

## Step 12: The Godfather check

Read the finished offer back against the one test: would a right-fit buyer feel stupid saying no? Score it 1 to 10, honestly. If it is under 8, name the single weakest part and fix it. Do not ship a 6.

## Output template: context/offer.md

```markdown
# Offer: [Name]
**Built:** [date]
**For:** [ICP name + dream outcome, from context/icp.md]
**Godfather score:** [X]/10

## The one-sentence offer
I help [buyer] [dream outcome] in [time frame] without [main pain], guaranteed.

## The promise (dream outcome)
[vivid, specific, in their words]

## Value Equation scorecard
| Lever | Before | After | What changed |
|---|---|---|---|
| Dream Outcome | /10 | /10 | |
| Perceived Likelihood | /10 | /10 | |
| Time Delay | /10 | /10 | |
| Effort and Sacrifice | /10 | /10 | |
Weakest lever fixed: [which + the fix]

## The stack
| Item | Delivers | Standalone value |
|---|---|---|
| [core] | [problem it solves] | $ |
| [item] | | $ |
| Bonus: [name] | [objection it kills] | $ |
**Total stacked value:** $[sum]
**Price:** $[price]  ([value-to-price ratio]x)

## The guarantee
[one to two sentences]

## Scarcity / urgency
[the real reason to act now]

## Price framing
- vs the stack: [line]
- vs the cost of inaction: [line, pulled from ICP]
- vs the alternative: [line]

## Names considered
1. [pick] (chosen)
2. ...
3. ...
```

## Hard rules

- One offer, one buyer. If they try to build "the offer for everyone," push back and make them pick one ICP or segment.
- The stacked value must dwarf the price (10x or more). If it does not, keep stacking or cut the price.
- Every guarantee, deadline, and limit must be TRUE. Never fabricate proof, scarcity, or results.
- Fix the weakest Value Equation lever before you name or price the offer.
- Voice: no em dashes, no buzzwords (delve, leverage, unleash, transformative, streamline, seamless), specific numbers, plain language, in the founder's voice from `references/voice.md`.
- Do not ship under an 8 on the Godfather check.

## What to run next

- `/pricing` to pressure-test the price and build the pricing page.
- `/copy` to turn this offer into a sales page.
- `/ads` to put the promise into ad hooks.
- `/lead-magnets` to build the front-end opt-in that leads to this offer.
