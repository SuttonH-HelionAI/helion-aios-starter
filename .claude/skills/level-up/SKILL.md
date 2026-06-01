---
name: level-up
description: Weekly ritual for the Helion AIOS. Finds and ships ONE build by walking the Brain's three moves, Shift, Scope, Ship. One run produces one decisions/log.md entry and one scaffolded artifact. Triggers on "/level-up", "what should I build next", "find me leverage", or a Friday build ritual.
---

# Level Up: find one build, ship it

This is the weekly engine of the whole kit. `/audit` tells you the engine is built right. `/level-up` finds the leverage you are still missing and ships it. One run = one shipped artifact. Not three. One.

It walks the Brain (`references/the-brain.md`): Shift to find the candidate, Scope to define it, Ship to build it.

## What you read first

- `context/priorities.md` (what matters this quarter)
- `context/about-me.md` (the time-suck, who they are)
- `connections.md` (what is reachable, tagged by engine)
- `references/the-brain.md` (the three moves, the rules)
- `decisions/log.md` (what was already scoped or built)
- `.claude/skills/` frontmatter (what hands already exist)
- the most recent file in `audits/` (the named gap, if they just ran /audit)

## Phase 1, SHIFT (find the candidate)

Shift always runs first. Even if the operator arrives with a build in mind, you still surface candidates and let them choose. The idea they walk in with is rarely the highest-leverage one.

Ask, conversationally, not as a form:

- What did you do three or more times this week? (frequency)
- What felt manual or copy-paste? (drudgery)
- What could a smart intern have handled? (delegation)
- If demand 10x'd on Monday, what breaks first? (constraint)
- What would give you 10x the demand? (growth lever)

The last two are the Brain's two constraint questions. One finds what is broken. One finds what could scale.

Surface 1 to 3 candidates. For EACH one, tag:
- the **engine** it serves (Growth or Fulfillment)
- the **layer** it builds (Memory, Reach, Hands, or Pulse)

Quote a Brain principle where it fits ("break the function down," "default to AI," "boring is beautiful"). Then ask: **pick one to scope.**

## Phase 2, SCOPE (scope the one they picked)

Walk the Brain's Scope pipeline in order.

**Find the constraint.** Confirm which of the two questions this build answers. Is it killing a bottleneck, or pulling a growth lever?

**Run EAD, Eliminate, Automate, Delegate, in that order.**
1. **Eliminate first.** Ask: "What happens if we just stop doing this?" If nothing breaks, exit cheerfully. Log it as a win in `decisions/log.md` ("eliminated, not automated") and stop. Do not automate waste. Killing a task is a better outcome than automating it.
2. **Automate second.** If it must exist, apply 60/30/10: about 60 percent fully automated, about 30 percent AI-assisted with human review, about 10 percent manual. Full automation is rarely the goal.
3. **Delegate third.** Too complex, too variable, too much judgment? Hand it to a person. Not everything should be automated.

**Map the process.** Five parts: trigger, sources, transformations, decision points, destination. If the operator cannot articulate the steps, tell them to sketch it on paper first, then stop the session. You cannot explain to an AI what they cannot explain to a person.

**Set the autonomy level.** Assign L0 to L4 per step. Default to the lowest level that works. Push back hard on L4. Workflows beat agents. If a decision does not have to be made by AI, do not let AI make it.

**Tie it to a number.** Mandatory. The build must move one of three: more customers, more value per customer, or lower cost. Plus a specific metric (response time, error rate, conversion, hours saved). If they cannot name a bucket AND a metric, stop. No number, no build.

Write the scoped spec to `decisions/log.md` as a dated entry. Include: the build, the engine, the layer, the constraint it answers, the autonomy level, and the number it moves.

## Phase 3, SHIP (build it)

Ask how to ship, in this order. Default to the highest non-AI option that does the job. Boring is beautiful.

1. **Prompt-only template.** A reusable prompt or doc. No code.
2. **Deterministic tool or script.** Rules, no AI.
3. **AI-assisted skill.** A SKILL.md with AI in the loop.
4. **Sub-agent.** Last resort. Only when judgment genuinely has to be delegated.

Build with the **WAT split** (`references/the-brain.md`): Workflows are the instructions, Agents are the decision-makers, Tools are the execution. Keep them separate. Smallest blocks first. Deterministic before AI. Validate each step.

Scaffold the artifact now. Write the actual file inline, with frontmatter. If it is a skill, write the SKILL.md to `.claude/skills/{name}/SKILL.md`.

Every scaffolded artifact ships with two things in its frontmatter:
- `rollout-phase: 1`. Run it manually first. This is the kit's phased rollout. Even at 90 percent confidence, start with 10 percent of the volume and watch for a week.
- a tag for the engine and layer it serves (e.g. `engine: Growth`, `layer: Hands`)

## Output contract

One run produces exactly:
1. One dated entry in `decisions/log.md` (the scoped spec).
2. One scaffolded artifact (the file, written, with frontmatter).
3. A one-screen close: what was scoped, what was built, and the reminder: "Run it manually first. Watch it for a week before you trust it."

## Rules

- One interview, one artifact. Never ship three.
- Shift always runs first, even if they arrive with an idea.
- Eliminate-first can end the session as a win. A killed task beats an automated one.
- Default to the lowest autonomy level that works. Push back on L4.
- Default to the highest non-AI build option that works.
- Tie-to-number is mandatory. No number, no build.
- Read-only on everything EXCEPT `decisions/log.md` and the one new artifact.
- Never edit the three `references/*.md` framework files.
