# Helion AIOS: AI Operating System starter for Claude Code

A starter kit that turns Claude Code into your personal **AI Operating System (AIOS)**. Built for founders and operators who are the bottleneck in their own business. Pairs with the Helion course inside AI Infrastructure HQ.

Clone it, run `/onboard`, and the kit personalizes to you. Then two weekly skills (`/audit` and `/level-up`) keep building leverage, one piece at a time.

---

## The litmus test

> **While you are away from your desk, your AIOS observes one real event and produces an output that is faster and more accurate than what you would make yourself.**

Every part of this kit rolls up to that. If a file, skill, or layer does not move you toward it, it does not ship.

---

## How you will know it is working

Three things you will feel in your week. Not metrics. Lived experience.

1. **You ask your own system first.** A teammate asks you something. You realize your AIOS would answer it faster, and with the exact source. So you ask it too. That is the moment you stop being the bottleneck for your own knowledge.
2. **You stop opening tabs.** Something new lands. Your first move is to ask the AIOS, not to open six apps. The default place you do thinking work quietly shifts.
3. **Your head empties.** You stop trying to remember business facts. You trust the system to hold the truth. You hold the questions.

Hit two of three in the first month and it took.

---

## How it is built: one lens, two frameworks

**The lens: the Engine Model.** Your AIOS is a **Value Engine**. It runs on two engines, and everything you build serves one of them.
- **Growth Engine**: get and grow revenue
- **Fulfillment Engine**: deliver the promise and keep it

Full breakdown: `references/engine-model.md`.

**The Brain: Shift, Scope, Ship.** How you think, decide, and build with AI.
- **Shift**: default to AI, break the job down, stay curious
- **Scope**: find the constraint, decide what to automate, tie it to a number
- **Ship**: build with Workflows, Agents, and Tools; smallest blocks first; keep a kill switch

Full breakdown: `references/the-brain.md`. The `/level-up` skill walks it weekly.

**The Architecture: the Value Engine, in four layers.** What you build, in order.
- **Memory**: knows you and the business
- **Reach**: touches your live data
- **Hands**: produces the work
- **Pulse**: runs without being asked

Full breakdown: `references/the-architecture.md`.

---

## What ships: a core loop plus a Growth Engine pack

Three core skills run the operating loop. Twelve marketing skills come pre-loaded so your Growth Engine has hands on day one. Your Fulfillment Engine is yours to build, and `/level-up` points you there next.

**Core loop**

| Skill | When to run |
|---|---|
| `/onboard` | Day 1, right after clone. A short interview. Fills your context and `CLAUDE.md`. |
| `/audit` | Day 7, then weekly. Scores your Value Engine across both engines and four layers. Read-only. |
| `/level-up` | Day 14, then weekly. The Shift, Scope, Ship interview. One run = one shipped build. |

`/audit` asks "is the engine built right?" `/level-up` asks "what am I still missing?" Run them in that order.

**Growth Engine pack (marketing)**

Thirteen drop-in marketing skills, ready once `/onboard` knows your business:

`/icp` `/offer` `/customer-research` `/competitive-research` `/content-strategy` `/copy` `/ads` `/email` `/brand-voice` `/cro` `/lead-magnets` `/social` `/pricing`

Each is tagged to the Growth Engine, so `/audit` counts them in your coverage grid.

---

## Quick start

1. **Clone** this repo to a folder on your machine.
2. **Open it in Claude Code** and run `/onboard`. Answer the questions honestly. Paste your writing samples, do not retype them. About 15 minutes.
3. **Use it for a week.** Bring real questions. Make real decisions. Log them in `decisions/log.md`.
4. **Day 7:** run `/audit`. Read the coverage grid. Pick one empty cell.
5. **Day 14:** run `/level-up`. It scopes one build worth shipping. Build it.
6. **Week 3 and on:** weekly `/level-up`. One shipped build per week.

---

## Repo layout

```
helion-aios-starter/
├── README.md
├── CLAUDE.md                 ← your operating manual (filled by /onboard)
├── EXPANSIONS.md             ← what to add as you grow
├── LICENSE
├── aios-intake.md            ← source of truth for /onboard. Edit and re-run any time.
├── connections.md            ← every system your AIOS can reach, tagged by engine
├── context/                  ← about you and your business (filled by /onboard)
├── references/
│   ├── engine-model.md       ← the lens
│   ├── the-brain.md          ← Shift, Scope, Ship
│   └── the-architecture.md   ← the Value Engine in four layers
├── decisions/log.md          ← append-only record of decisions and why
├── audits/                   ← saved audit reports
├── archives/                 ← old stuff. Don't delete. Move here.
└── .claude/skills/        ← 3 core skills + 13 Growth marketing skills
    ├── onboard/  audit/  level-up/                          (core loop)
    ├── icp/  offer/  customer-research/  competitive-research/
    ├── content-strategy/  copy/  ads/  email/
    └── brand-voice/  cro/  lead-magnets/  social/  pricing/  (Growth Engine)
```

See `EXPANSIONS.md` for what to add as you outgrow the base.

---

## License and attribution

MIT License.

The Engine Model (Value, Growth, Fulfillment) is the scalable-business framing popularized by Ryan Deiss in *Get Scalable*, applied here to a personal AIOS. The Brain (Shift, Scope, Ship) and the Architecture (the Value Engine in four layers) are Helion frameworks. Use freely.
