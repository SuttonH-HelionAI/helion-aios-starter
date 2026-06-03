# The Architecture: The Value Engine, In Four Layers

> The brain (`the-brain.md`) is how you think. The architecture is what you build. Your AIOS is your Value Engine. You build it as two engines, each through four layers, in order.

Your AIOS is your **Value Engine** (see `engine-model.md`). It runs on two engines: **Growth** and **Fulfillment**. You build each one through the same four layers, bottom to top. Skip a layer and the ones above it have nothing to stand on.

```
                THE VALUE ENGINE  (your AIOS)
               /                          \
        GROWTH ENGINE              FULFILLMENT ENGINE
        get + grow revenue         deliver + keep the promise

        each engine, built through four layers:

   4 · PULSE    runs without being asked
   3 · HANDS    produces the work
   2 · REACH    touches your live data
   1 · MEMORY   knows you and the business
```

---

## Layer 1: MEMORY (knows you and the business)

What the AIOS knows. Who you are, what you sell, who you serve, your voice, your priorities, the decisions you have made and why.

Everything else sits on this. A system with no memory answers like a stranger. A system with good memory answers like a teammate who has been with you for years.

**In place when:** a fresh session answers *"what does this business do and who works here?"* with no browsing and no paste.

Lives in: `context/` (including `context/business-map.md`, your seven buckets mapped), `CLAUDE.md`, `decisions/log.md`, `references/`.

## Layer 2: REACH (touches your live data)

What the AIOS can pull from and act on. Your tools, your accounts, your live data. The important data is not on the public web. It is locked inside your tools. Reach is how the system gets to it.

The **seven buckets** every business runs on (the full map is in `references/the-seven-buckets.md`):

| # | Bucket | Engine it usually feeds |
|---|---|---|
| 1 | Revenue | Growth |
| 2 | Customer | Growth |
| 3 | Calendar | Both |
| 4 | Comms | Both |
| 5 | Tasks | Fulfillment |
| 6 | Meetings | Fulfillment |
| 7 | Knowledge | Both |

**In place when:** *"what is due tomorrow and what came in today?"* returns live data, no copy-paste.

Lives in: `connections.md`, `.env`, `references/{tool}-api.md`.

## Layer 3: HANDS (produces the work)

What the AIOS can actually do. Skills that turn a short ask into a finished deliverable. Not answers to questions. Real output.

This is where most of your leverage is built. Every skill you make belongs to one engine. A content skill is a Growth hand. A client-report skill is a Fulfillment hand.

**In place when:** a short phrase triggers a multi-step skill that hands you a real artifact, not a follow-up question.

Lives in: `.claude/skills/`.

## Layer 4: PULSE (runs without being asked)

What runs while your laptop is closed. Scheduled and triggered work. The morning brief that lands before you wake up. The follow-up that fires when a deal goes quiet.

You earn this last. Never put a workflow on a schedule until it works by hand. Automating a broken process just breaks it faster.

**In place when:** your laptop is shut and an output still lands. A brief, a draft, an alert, a logged decision.

Lives in: schedules, hooks, and the `Pulse`-tagged skills you graduate from Hands.

---

## Build order

1. **Memory first.** Non-skippable. Run `/onboard`.
2. **Reach and Hands in parallel.** Wire a tool, build a skill. They feed each other.
3. **Pulse last.** Only once a skill is proven by hand.

## The build loop: audit, scope, install, maintain

This is Helion's client method, now your personal loop. You run it on yourself, one layer and one engine at a time.

- **Audit**: `/audit` scores all eight cells (two engines by four layers) and names the biggest gap.
- **Scope**: `/level-up` walks Shift, Scope, Ship to define one build that closes that gap.
- **Install**: you build it. Memory file, wired tool, new skill, or a schedule.
- **Maintain**: keep it working, or hit the kill switch when it stops earning its keep.

## The coverage grid

A complete AIOS covers all eight cells.

| Layer | Growth Engine | Fulfillment Engine |
|---|---|---|
| Pulse | | |
| Hands | | |
| Reach | | |
| Memory | | |

`/audit` fills this in and scores it. Empty cells are your roadmap.

---

> **The litmus test.** While you are away from your desk, your Value Engine observes one real event and produces an output that is faster and more accurate than what you would make yourself. Every layer, skill, and connection rolls up to that. If it does not contribute, it does not ship.
