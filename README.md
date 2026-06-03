# Helion AIOS: AI Operating System starter for Claude Code

A starter kit that turns Claude Code into your personal **AI Operating System (AIOS)**. Built for founders and operators who are the bottleneck in their own business. Pairs with the Helion course inside AI Infrastructure HQ.

Clone it, run `/onboard`, and the kit personalizes to you. Then two weekly skills (`/audit` and `/level-up`) keep building leverage, one piece at a time.

---

## Open the kit (read this first)

This kit is a folder of files. Claude Code only sees them when you open **this exact folder** as your workspace. Get this right and everything works. Get it wrong and you will see "Unknown command."

1. **Download and unzip.** The ZIP unpacks to a folder named **`helion-aios-starter-main`**. That folder is the kit.
2. **Open that folder, not the one above it.** In VS Code: **File → Open Folder →** select **`helion-aios-starter-main`**. The list on the left should show `CLAUDE.md` and a `.claude` folder at the very top. If instead you see a single `helion-aios-starter-main` folder you have to click into, you opened the parent (like Downloads). Go back and open the inner folder.
3. **In VS Code, reload the window.** Press **Cmd+Shift+P** (Mac) or **Ctrl+Shift+P** (Windows), type **Reload Window**, press Enter. This is what loads the commands. Opening a new chat is not enough.
4. **Type `/onboard`.** Type `/` first and you should see `onboard`, `audit`, `copy`, and more in the list.

**If `/onboard` says "Unknown command":** you opened the wrong folder (the parent) or skipped the reload. Open the folder that holds this README, reload the window, and try again.

On the terminal version of Claude Code the same rule applies: run `claude` from inside the `helion-aios-starter-main` folder.

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

Fourteen drop-in marketing skills, ready once `/onboard` knows your business:

`/icp` `/offer` `/customer-research` `/competitive-research` `/content-strategy` `/copy` `/ads` `/email` `/brand-voice` `/brand-guidelines` `/cro` `/lead-magnets` `/social` `/pricing`

Each is tagged to the Growth Engine, so `/audit` counts them in your coverage grid.

---

## Quick start

1. **Open the kit.** Follow "Open the kit (read this first)" above: download or clone, open the `helion-aios-starter-main` folder, reload the window.
2. **Send any message.** On a fresh kit, your first message auto-starts onboarding (or run `/onboard` yourself). It builds your Foundation: intake, then your business mapped across the seven buckets, then your buyer, your offer, and your brand, ending with one real deliverable that proves it works. It is resumable, so build it across sittings. This is the deep part. Do not rush it.
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
└── .claude/
    ├── commands/             ← typeable /commands, one per skill (works on any Claude Code version)
    └── skills/               ← 3 core skills + 14 Growth marketing skills (the logic)
        ├── onboard/  audit/  level-up/                      (core loop)
        ├── icp/  offer/  customer-research/  competitive-research/
        ├── content-strategy/  copy/  ads/  email/
        └── brand-voice/  brand-guidelines/  cro/  lead-magnets/  social/  pricing/  (Growth)
```

See `EXPANSIONS.md` for what to add as you outgrow the base.

---

## License and attribution

MIT License.

The Engine Model (Value, Growth, Fulfillment) is the scalable-business framing popularized by Ryan Deiss in *Get Scalable*, applied here to a personal AIOS. The Brain (Shift, Scope, Ship) and the Architecture (the Value Engine in four layers) are Helion frameworks. Use freely.
