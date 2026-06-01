---
name: audit
description: Scores the Helion AIOS Value Engine across the four layers (Memory, Reach, Hands, Pulse) out of 100, builds the two-engine coverage grid, and ranks the top 3 gaps by leverage. Read-only. Run on Day 7, then weekly. Triggers on "/audit", "audit my AIOS", "score my setup", "is my AIOS working".
---

# Audit: score the Value Engine

Read-only health check. It answers one question: **is the engine built right?** (`/level-up` answers the other one: what leverage am I still missing.)

Fast. Read frontmatter, count folders, score. Under sixty seconds. Be honest, not generous. Most real setups land between 40 and 70. A perfect score means the operator is lying or you are.

## What you read

- `CLAUDE.md` (is the operating manual filled or still full of `{{...}}`)
- `context/` (which files exist and have real content)
- `references/` (voice sample, API guides)
- `decisions/log.md` (any entries)
- `connections.md` (the seven domains, their mechanism and auth)
- `.claude/skills/` (count the SKILL.md files, read their frontmatter)
- schedules, hooks, cron, or any skill named or tagged for Pulse
- `audits/` (recent reports, to track the climb)

Use the "in place when" tests from `references/the-architecture.md` as the standard for each layer.

## Score the four layers, 25 each, 100 total

### Memory (25): knows you and the business
- Operating manual (`CLAUDE.md`) is substantive, placeholders filled (5)
- Identity and voice captured (`context/about-me.md`, `references/voice.md`) (4)
- Business and priorities filled (`about-business.md`, `priorities.md`) (4)
- Foundation canon, the deep Memory: `context/icp.md` (4), `context/offer.md` (4), `references/brand-guidelines.md` (2)
- Decisions logged (`decisions/log.md` has real entries) (2)

Test: a fresh session answers "what does this business do and who works here?" with no browsing and no paste. A deep Memory also answers "who is our buyer and what is our offer?" straight from `context/icp.md` and `context/offer.md`. That depth is what the Foundation (`/onboard`) builds.

### Reach (25): touches your live data
- The seven domains in `connections.md`, ~3.5 points per domain reachable. Cap the raw domain count at ~14 points.
- Scale to 25 by adding: a reference guide present for wired tools, and at least one WRITE-capable connection (not every connection read-only).
- A domain counts as reachable via ANY mechanism: MCP, a script, or an API key plus a `references/{tool}-api.md` guide. "not yet connected" does not count.

Test: "what is due tomorrow and what came in today?" returns live data, no copy-paste.

### Hands (25): produces the work
- 3 or more skills present (10)
- At least one user-built skill beyond onboard, audit, and level-up (10)
- A sub-agent defined (5)

Test: a short phrase triggers a multi-step skill that hands back a real artifact, not a follow-up question.

### Pulse (25): runs without being asked
- A recurring or scheduled trigger, or a skill named or tagged for a schedule (10)
- Recent activity within 30 days (a dated entry, a saved audit, a logged decision) (10)
- Templates present (5)

Test: the laptop is shut and an output still lands.

## The coverage grid, the Helion differentiator

Build the 2-engine by 4-layer grid from `references/the-architecture.md`. For each of the eight cells, mark **covered** or **empty**.

- Use the engine tags in `connections.md` (each domain is Growth, Fulfillment, or Both) to decide which engine each Reach and Memory item serves.
- Read the `> **Engine:**` tag near the top of each skill's `SKILL.md` to place Hands and Pulse items by engine. If a skill has no tag, judge by what it does. (The pre-loaded marketing skills are all tagged Growth.)
- A "Both" tag counts toward both engines for that layer.

```
| Layer  | Growth Engine | Fulfillment Engine |
|--------|---------------|--------------------|
| Pulse  | covered/empty | covered/empty      |
| Hands  | covered/empty | covered/empty      |
| Reach  | covered/empty | covered/empty      |
| Memory | covered/empty | covered/empty      |
```

This is what makes the Helion audit different. It does not just say "is it built right." It says "is each ENGINE covered." An empty column is a whole side of the business with no leverage.

## Top 3 gaps, ranked by leverage

Leverage = points lost x impact multiplier. Heaviest multipliers:

| Condition | Multiplier |
|---|---|
| 0 domains reachable | 4x |
| Thin or missing operating manual | 3x |
| An entire ENGINE with no Hands (e.g. "your Growth Engine has no skills") | 3x |
| 0 skills | 2x |
| No Pulse | 2x |
| Everything read-only (no write connection) | 2x |

Rank the three highest. Each gap gets ONE concrete next step: run /level-up, wire a named domain, build a skill, or add a schedule.

## Output, the report

A markdown report, in this order:

1. **Score: X/100** with a stage label
   - 0-39 Foundation
   - 40-69 Built
   - 70-89 Compounding
   - 90-100 Autonomous

2. **Scoreboard**. The four layers, each with a simple bar:
   ```
   Memory  ████████░░  21/25
   Reach   ███░░░░░░░   7/25
   Hands   █████░░░░░  13/25
   Pulse   ██░░░░░░░░   5/25
   ```

3. **Coverage grid**. The 2x4 table above.

4. **Strengths**. 2 to 3 bullets.

5. **Top 3 gaps**. Each with its one-line next step.

6. **Suggested next**. One line, the single highest-leverage move.

7. Close with exactly: **"To find your next build, run /level-up."**

## Rules

- Read-only. The only writable side effect: after printing, offer to save the report to `audits/audit-{YYYY-MM-DD}.md`. Ask first.
- Honest, not generous. If the manual is full of placeholders, Memory is low. If nothing is wired, Reach is near zero. Say it plainly.
- Under sixty seconds. Read frontmatter and count folders. Do not deep-read every file.
- Do not edit the three `references/*.md` framework files. Do not fix anything. Auditing is not building. That is what /level-up is for.
