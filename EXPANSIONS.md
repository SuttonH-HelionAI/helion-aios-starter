# Expansions: What to Add as You Grow

The kit ships lean on purpose. A clean AIOS is faster to reason over and easier to trust. Your system should look like a small, well-run business, not a hoarder's basement. Add a folder only when the work demands it, never before.

---

## What ships, and you don't remove

The base. Every one of these earns its place on Day 1. Do not delete them.

| Path | What it holds |
|---|---|
| `context/` | About you, your business, your priorities. The Memory layer. |
| `references/` | The frameworks, your voice sample, API guides as you wire tools. |
| `decisions/log.md` | Append-only record of decisions and why. |
| `audits/` | Saved `/audit` reports, so you track the score over time. |
| `archives/` | Old stuff. Never delete. Move here. |
| `connections.md` | Every system your AIOS can reach, tagged by engine. |
| `.claude/skills/` | Your Hands. The three starter skills, plus what you build. |
| `aios-intake.md` | Source of truth for `/onboard`. Edit and re-run any time. |
| `CLAUDE.md` | Your operating manual. Filled by `/onboard`. |

---

## What to add as you grow

Add each one when the trigger hits. Not before.

| Add | When | Why |
|---|---|---|
| `projects/` | You are running 2 or more active workstreams | Keeps separate efforts from bleeding into each other. One folder per workstream. |
| `templates/` | You catch yourself copy-pasting the same prompt twice | Save it once. Reuse it forever. |
| `brand-assets/` | You start making visual content | Logos, fonts, colors in one place the AIOS can reach. |
| `references/sops/` | You document a repeatable process | A standard operating procedure the AIOS can run the same way every time. |
| `references/{tool}-api.md` | You wire an API | The endpoints, auth, and request shape for a tool. Researched once, saved forever. |
| `scripts/` | A Tool needs to hit an API directly | Small scripts the AIOS calls to reach a system. |
| `.claude/agents/` | One assistant is doing too many jobs | Sub-assistants with a narrow focus. A research agent, a drafting agent. |
| A sub-OS folder | A vertical grows its own data and rhythm | A self-contained mini-AIOS for one product line or business unit. |

Tie growth to the engine it serves. A content skill is a Growth Engine hand, so it lives in `.claude/skills/` and feeds the Growth side of your coverage grid. A client-delivery or reporting skill is a Fulfillment Engine hand. When you add a folder for a new workstream, know which engine it feeds before you build into it.

---

## What NOT to add

These are the patterns that rot an AIOS. They feel productive. They are clutter.

- **No graveyard folders.** No `notes/`, `misc/`, `tmp/`, or `inbox/`. These become where things go to be forgotten. If a file matters, it has a real home. If it does not, it goes to `archives/`.
- **No folder-of-folders.** If a directory only holds other directories and no real files, you have over-organized. Flatten it.
- **No raw archives in `references/`.** `references/` is for guides the AIOS actively reads. Old material goes to `archives/`, not here.
- **Do not fork `CLAUDE.md`.** One operating manual. Per-context instructions live in the skill or the project README, not a second CLAUDE.md.
- **Do not pre-create empty folders.** An empty folder is a promise you have not kept. Create it the day you have something to put in it.

---

## How to tell when it is time to add a folder

Three checks. If you cannot pass all three, do not add it.

1. **Is it conceptually new?** Does this hold a kind of thing nothing else holds? If it fits in an existing folder, put it there.
2. **Will you touch it 3 or more times this month?** A folder you open once is a file, not a folder. Wait until the volume is real.
3. **Could `/level-up` route a skill into it?** If you can picture a skill writing to or reading from it, the folder has a job. If not, it is decoration.
