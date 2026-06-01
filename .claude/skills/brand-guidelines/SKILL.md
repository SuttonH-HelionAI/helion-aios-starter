---
name: brand-guidelines
description: Use to build your brand canon the first time, then to check any customer-facing draft against it. Auto-triggers on PDPs, ads, emails, social, copy, landing pages, and any branded surface, or "/brand-guidelines", "build my brand guidelines", "is this on brand", "brand check", "lock my brand". Builds references/brand-guidelines.md if it is missing, then gates every draft against it.
---

> **Engine:** Growth

# /brand-guidelines

Two jobs. Build the brand canon the first time, in the Brand phase of your Foundation. Then guard every customer-facing draft against it so nothing off-brand ever ships.

## Step 0: Build or gate?

Check whether `references/brand-guidelines.md` exists.
- **Missing** then BUILD MODE. Go to Step 1. This is the Brand phase of your Foundation.
- **Exists** then GATE MODE. Skip to Step 3.

Either way, first read `context/about-business.md`. If it is still a placeholder, stop and tell the user to run `/onboard` first. The brand canon is built on the business, the buyer, and the offer.

## Step 1: Build the canon (build mode)

Load everything that defines the brand:
- `context/about-business.md`: what you sell, who you serve.
- `context/icp.md` (if present): the buyer and their exact language.
- `context/offer.md` (if present): the promise.
- `references/voice.md` and the `## Voice` section of `CLAUDE.md`: real writing samples.
- `.claude/rules/decision-filter.md`: what you stand for.

Write `references/brand-guidelines.md` with these sections:
- **Voice:** the words you USE and the words you NEVER use (pulled from `references/voice.md`). Sentence style. The AI tells to strip on every pass.
- **Audience fit:** who every line must make sense to (from `context/icp.md` or `context/about-business.md`).
- **Identity fit:** what the brand stands for and what it will never say.
- **Visual direction:** colors, type feel, logo rules if known. If a `brand-assets/` folder exists, reference its tokens. If not, capture the visual feel in words and note that `brand-assets/` can be added later for the full visual system.
- **Surface rules:** copy the per-surface checklist from Step 2 below into the canon.

Confirm the canon back to the user in five lines. From now on, drafting flows through gate mode.

## Step 2: The surface rules

Different surfaces, different rules. These live in the canon and apply in gate mode.

**Universal (every surface):**
- Use the words under Voice USE. Strip every word under Voice NEVER.
- No em dashes. Commas, periods, or line breaks instead.
- No AI tells: delve, unleash, elevate, leverage, transformative, streamline, dive into, "it's worth noting," certainly, absolutely, "in today's world."
- Short sentences over long. Specific over vague. Numbers over adjectives.
- If a line could appear on any brand's marketing, it is too generic. Rewrite it to something only this brand could say.
- Run every draft against the identity and the decision filter. If it conflicts, rewrite or kill it.

**PDP / product page:** hero with name, hero benefit, real price, one CTA. Below the fold, 3 to 5 specific benefits with proof or mechanism. Full spec transparency. Real reviews or named experts only. FAQ hits the top objections from the ICP.

**Ad:** hook in line one, stop the scroll. One promise, not three. One CTA matched to awareness level. Visuals follow `brand-assets/` tokens if present.

**Email:** subject short and specific, no clickbait, no complex merge tags (first name is fine). Body is one idea, one CTA, a P.S. allowed and often the most read line. Read it out loud, if it does not sound like the brand, rewrite.

**Social:** one idea per post. Hook in line one, paid off in the body, single CTA. Visuals follow tokens.

**Landing page:** one promise above the fold, one CTA. Below it, proof, mechanism, objections, real urgency. Strip every link that does not serve the one goal.

**Long-form:** hook in the first sentence, paid off by the end. Teach something specific. Closing CTA matched to the reader's awareness.

## Step 3: Check a draft (gate mode)

Read `references/brand-guidelines.md`. Ask or detect which surface is being drafted. Apply the universal rules plus that surface's rules. Then append a brand check:

```
Brand check
- Voice: pass, or [words flagged for rewrite]
- Audience fit: pass, or [where it drifts generic]
- Identity / decision filter: pass, or [conflict named]
- Surface rules: pass, or [what is missing]
```

If any line fails, fix it before delivering. Never ship a draft that fails the brand check.

## Rules

- Build the canon once (build mode), then never draft without running the check (gate mode).
- Use the brand's own voice words verbatim. Never import outside-brand voice.
- Strip every AI tell on every pass. Catching them is the job.
- One promise per surface. One CTA per surface. Subtraction is the work.
- If `brand-assets/` is missing, name the gap and continue with text-only visual rules.
