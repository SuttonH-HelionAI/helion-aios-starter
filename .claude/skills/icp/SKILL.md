---
name: icp
description: Ideal Customer Profile builder. One offer, one buyer, in their words. Scores PVP (Personal x Value x Profitability), enforces a halo gate, pulls five verbatim language quotes for the swipe file. Two modes, interview or draft. Auto-triggers on phrases like "find my ideal customer", "build an ICP", "who is my dream buyer", "define the avatar for X". User-invocable as `/icp [business] [offer]`.
argument-hint: [business] [offer-or-funnel-slug]
---

> **Engine:** Growth

# /icp

You build one specific, halo-grade ICP for one offer. Not a persona deck. Not a "everyone who could buy" doc. One offer, one buyer, in their words.

---

## Step 0: Context check

Before doing anything, scan the workspace.

1. Check `context/about-business.md` for the offer, what you sell, who you serve. Check `context/about-me.md` for who you are.
2. Read the voice from `references/voice.md` and the `## Voice` section of `CLAUDE.md` so the doc lands in the right register.
3. Check `projects/[business]/README.md` for the offer brief, pricing, status, if it exists.
4. Check `projects/[business]/research/quote-bank.md` (output of `/customer-research`). If it exists, treat it as the canonical source for Q37 verbatim quotes, pull from it rather than re-gathering. Also check `projects/[business]/research/` for raw call notes and review files.

Decide which path you are on, say it out loud:

- **Loaded:** "I have enough context to draft. Here is what I pulled: [one-line summary]." Confirm offer slug, then go.
- **Partial:** "I have positioning. Missing offer-specific brief. Three quick questions then I draft."
- **Fresh:** "No business context yet. Run `/onboard` first to fill `context/about-business.md`, takes about 10 minutes. This skill needs grounding to produce a real ICP, not a generic persona."

Never proceed without at least Loaded or Partial.

---

## Step 1: Parse arguments and pick mode

`$1` = business slug (e.g. `acme-saas`). `$2` = offer slug (e.g. `core-client`, `pro-tier`, `holiday-bundle`). If either is missing, ask.

Then ask the user which mode:

- **Interview mode (default):** walk the 44 questions one section at a time, capture verbatim. 25 to 40 minutes. Use for new offers, pivots, or when context is thin.
- **Draft mode:** read existing context, fill best-effort answers, mark every guess with `[GUESS, confirm]`. 5 minutes plus user review. Use when project context is rich.

---

## Step 2: Walk the 8 parts

Read the full questionnaire from the Reference section below. Walk each part in order. Do not skip ahead. Capture answers verbatim. Push back on corporate-speak.

After Part 4 (Halo Filter), state the verdict before continuing.
After Part 5 (PVP Scorecard), state the score and verdict before continuing.
After Part 6 (Language), pull five verbatim quotes into a swipe-file callout block.

---

## Step 3: Write the output doc

Output template lives in the Reference section. Fill it completely. Save to `projects/[business]/icp/[offer-slug].md`. Create the `projects/[business]/icp/` folder if it does not exist yet, `projects/` is a grow-into folder in this kit.

Append a one-liner to `projects/[business]/README.md` under an "ICPs" section. Create the README and the section if missing.

```
## ICPs

- [core-client](icp/core-client.md), one-line summary (built YYYY-MM-DD, PVP 540, optimize)
```

---

## Step 4: Print the close-out

After save, print:

- PVP score and verdict
- Halo verdict (halo or broad market, with reason)
- The single highest-impact copy line this ICP unlocks
- Three next moves (specific, named)

---

## Hard rules

- One offer, one ICP. If the user tries to build "the ICP for the whole company," push back and make them pick one offer.
- Halo gate is non-negotiable. One "no" on Q23 through Q26 drops the buyer to broad-market.
- No corporate-speak in answers. Capture in the founder's voice or the customer's voice, never sanitize.
- Never invent verbatim quotes. If no real reviews or calls exist, mark Q37 `[needs 5 customer interviews]` and queue the gather work with `/customer-research`.
- PVP under 200 stops the run with a warning. Ask before proceeding.

---

## Reference: The 44-question questionnaire

### Part 1, Identity (8 questions)

1. What is their first name? Pick one real person who fits. If nobody fits, red flag.
2. Age, gender, marital status, kids?
3. Job title and income range?
4. Where do they live? (City type, neighborhood, suburb vs urban?)
5. What do they drive?
6. What is on their phone home screen? Apps tell you more than demographics.
7. Who do they follow on Instagram, X, YouTube?
8. What podcasts are in their queue right now?

### Part 2, The Pain (8 questions)

9. What is the one frustration that hits them in the gut every single morning?
10. What did they Google at 11pm last night when nobody was watching?
11. What do they complain about to their spouse, friends, coworkers?
12. What have they tried before that did not work? Name brands, programs, products.
13. Why did those not work? In their words, not yours.
14. What do they secretly believe is wrong with them that they would never say out loud?
15. What "thing they should not have to do anymore" are they still doing?
16. What is the cost of the problem if they do nothing for 12 months? Money, time, relationships, identity.

### Part 3, The Dream (6 questions)

17. If the problem disappeared overnight, what would they do tomorrow that they cannot do today?
18. What would they brag about to their best friend, their rival, their dad?
19. What status would they gain in their tribe?
20. What would they stop being afraid of?
21. What identity do they want to step into? ("I am a person who...")
22. What would they pay any amount to have, but cannot buy at any price right now?

### Part 4, The Halo Filter (6 questions)

The dream buyer has BOTH urgent pain AND the means to pay. Most businesses sell to "anyone with the problem." The halo is narrower.

23. Do they have the money to pay your premium price without flinching?
24. Have they already paid for solutions in this category? Buyers buy. Tire-kickers tire-kick.
25. Is the pain urgent? Meaning if you offered the solution today, they would act this week, not "someday."
26. Are they the decision-maker, or do they need a spouse, boss, or board to greenlight?
27. Are they sophisticated enough to recognize value, or do they need to be educated from zero?
28. Do they already believe the problem exists, or do you have to convince them?

Halo gate: If ANY of Q23 through Q26 is "no," the described buyer is the broad market, not the halo. Flag it.

### Part 5, PVP Scorecard (3 questions)

Rate the customer 1 to 10 on each:

29. **Personal fulfillment:** do you actually want to serve these people every day?
30. **Value to market:** how badly do they need you on a 1 to 10?
31. **Profitability:** what does one of them pay you over their lifetime?

Multiply the three. **Under 200 = wrong avatar.** Surface the warning before continuing.

### Part 6, Language (6 questions)

32. What exact phrase do they type into Google for this problem?
33. What do they call the problem in casual conversation? Not the clinical term, the slang.
34. What do they call the desired outcome?
35. What metaphors do they use? Sports, war, food, building, family?
36. What words make them roll their eyes? Corporate-speak, industry jargon, AI tells.
37. Pull 5 verbatim quotes for the swipe-file callout. Source priority: (a) `projects/[business]/research/quote-bank.md` from `/customer-research` if it exists, (b) raw reviews, DMs, comments, call notes in `projects/[business]/research/`, (c) flag `[needs 5 customer interviews]` and queue a `/customer-research` run if neither exists.

### Part 7, Where They Live (3 questions)

38. What 3 places online could you reach 100 of them tomorrow? Specific subreddits, IG accounts, FB groups, forums, podcasts.
39. What 3 places offline? Gyms, churches, conferences, retail.
40. Who already has their attention? Influencer, brand, podcast. That is your distribution shortcut.

### Part 8, Disqualifiers (4 questions)

41. Who looks like them on paper but is wrong for the offer? Be specific.
42. What customer behavior is a refund waiting to happen?
43. What red flags on a sales call mean "do not enroll"?
44. What price floor filters out the time-wasters?

---

## Reference: Scoring rubric

**PVP Index:** Personal x Value x Profitability (each 1 to 10).

- 700+ = ideal halo, scale this offer hard
- 400 to 699 = solid, optimize and ramp
- 200 to 399 = workable but constrained, pick one variable to lift
- Under 200 = wrong avatar, rebuild the offer or pick a different buyer

**Halo gate:** Q23 through Q26 must all be "yes" for halo classification. One "no" drops the buyer to broad-market and changes the entire copy and pricing strategy.

**Language sufficiency:** If Q37 has fewer than 5 real verbatim quotes, the ICP is incomplete. Mark `[needs 5 customer interviews]` and queue the call work as a follow-up.

---

## Reference: Output template

```markdown
# ICP, [Business] / [Offer Slug]
**Built:** YYYY-MM-DD
**Mode:** Interview | Draft
**PVP Score:** [P x V x P = total]
**Halo Status:** Halo | Broad Market (with reason)

## Part 1, Identity
1. Name: ...
[continue through Q8]

## Part 2, The Pain
9. Morning gut-punch: ...
[continue through Q16]

## Part 3, The Dream
17. Day-after fantasy: ...
[continue through Q22]

## Part 4, Halo Filter
23. Pays premium without flinching: yes/no, ...
[continue through Q28]
**Halo verdict:** [pass/fail with reason]

## Part 5, PVP Scorecard
29. Personal: X/10, ...
30. Value to market: X/10, ...
31. Profitability: X/10, LTV $...
**Total:** X
**Verdict:** [scale | optimize | constrained | rebuild]

## Part 6, Language
32. Google query: "..."
33. Slang for the problem: "..."
34. Slang for the outcome: "..."
35. Metaphors: ...
36. Eye-roll words: ...
37. Verbatim swipe file:
   > "..."
   > "..."
   > "..."
   > "..."
   > "..."

## Part 7, Where They Live
38. Online (3): ...
39. Offline (3): ...
40. Whose attention to borrow: ...

## Part 8, Disqualifiers
41. Lookalikes that are not a fit: ...
42. Refund-prone behavior: ...
43. Sales-call red flags: ...
44. Price floor: $...

---

## Highest-impact copy line this unlocks
[One sentence the user can paste into the next ad, email, or page.]

## Next moves
1. ...
2. ...
3. ...
```

---

## Anti-patterns

- Building "the ICP for the whole company." Always one offer.
- Sanitizing the customer's language into corporate-speak.
- Inventing verbatim quotes when no source exists.
- Skipping the halo gate to make the score look better.
- Treating the doc as final on first pass. ICPs sharpen with every customer interview.

---

## When to stop

Definition of done:

- All 8 parts filled in `projects/[business]/icp/[offer-slug].md`
- PVP score and verdict stated
- Halo verdict stated
- Swipe-file callout has 5 quotes (or `[needs 5 customer interviews]` flag)
- One unlocked copy line written
- Three next moves listed
- Index entry added to project README
