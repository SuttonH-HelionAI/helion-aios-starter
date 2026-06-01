---
name: onboard
description: Builds the operator's Foundation. A resumable chain that loads the Memory layer deep: intake, then the buyer, the offer, and the brand, ending with one real deliverable that proves it works. Triggers on "set me up", "onboard me", "/onboard", "build my foundation", "fill in my AIOS", or a fresh clone of the starter kit.
---

# Onboard: build your Foundation

This is the deepest and most important thing the operator runs. It is not a quick setup. It is a Foundation: a chain that loads the Memory layer (see `references/the-architecture.md`) so deep that when the operator later asks the OS for real work, it is flawless, because it already knows their buyer, their offer, and their voice cold.

Depth over speed. This can take a couple of hours. It is resumable. The operator runs it across sittings.

## How the chain works

Five phases plus a proof step, in order. Each phase writes a canonical file the next phase reads. No skipping ahead: you cannot build an offer without a buyer, or lock a brand without an offer.

```
Phase 1  Intake    -> context/about-me, about-business, priorities, voice, connections
Phase 2  Evidence  -> real market + customer data (optional, recommended)
Phase 3  Buyer     -> context/icp.md            (/icp)
Phase 4  Offer     -> context/offer.md          (/offer)
Phase 5  Brand     -> references/brand-guidelines.md + voice.md  (/brand-guidelines, /brand-voice)
Capstone Proof     -> one real flagship deliverable from the full stack
```

## Resume logic (do this first, every run)

Read `context/.foundation.md` if it exists. It tracks which phases are done.
- **Missing**: first run. Create it from the template below, all unchecked. Start at Phase 1.
- **Exists**: resume at the first unchecked phase. Tell the operator where they are: "You are through [N] of 6. Picking up at [phase]."

After each phase completes, check its box in `context/.foundation.md`, then ask: "Keep going to [next phase] now, or pause here? You can resume any time by running `/onboard`." Honor the answer.

### Status template (`context/.foundation.md`)

```markdown
# Foundation status
- [ ] Phase 1: Intake
- [ ] Phase 2: Evidence (optional)
- [ ] Phase 3: Buyer (/icp)
- [ ] Phase 4: Offer (/offer)
- [ ] Phase 5: Brand (/brand-guidelines, /brand-voice)
- [ ] Capstone: Proof
```

---

## Phase 1: Intake

Capture who they are and what they do. Builds the base of the Memory layer.

**The intake file.** `aios-intake.md` (repo root) is the source of truth. Read it. If it is missing, create it from the seed in `aios-intake.md`'s structure (seven questions, placeholder answers), then continue.

**Interview.** Seven questions, ONE AT A TIME. Write each answer into `aios-intake.md` the moment you get it. Hard cap at seven. No Q8. No bundling.

1. Who are you, what do you sell, who do you serve? One paragraph. Name the offer and the buyer.
2. Paste one or two writing samples, raw, from a real email or post you already sent. HARD RULE: if they type fresh prose instead of pasting, refuse. "Do not write me something new. Paste raw from something you already sent. The point is how you actually write, not how you write for an AI." Never accept fresh prose.
3. Top two or three priorities for the next 90 days. Push back on vague. Make each one carry a number or a deadline.
4. Where does revenue land and get tracked? Name the real tools.
5. Where do you talk to customers, your team, and the outside world?
6. Where do meeting recordings, notes, and docs live?
7. The one task that eats your week, and where you track work?

**Scaffold (one batch, back up any existing file to `archives/intake-{date}/` first):**
1. `context/about-me.md` from Q1 + Q7.
2. `context/about-business.md` from Q1 + Q4.
3. `context/priorities.md` from Q3 (numbered, keep numbers and dates).
4. `references/voice.md` from Q2, pasted verbatim, with a one-line header on how to use it.
5. `connections.md`, the seven-domain table from Q4 to Q7, each row tagged by engine per `references/the-architecture.md`. Mechanism "not yet connected", auth "none".
6. `CLAUDE.md`, fill every `{{...}}` placeholder ({{business_name}}, {{your_name}}, {{primary_priority}}, knowledge base, voice summary, connections summary).

No `.env` writes. Reach gets wired later.

Mark Phase 1 done in `context/.foundation.md`.

---

## Phase 2: Evidence (optional, recommended)

Before building the buyer and the offer, ground them in real data instead of memory alone.

Offer it: "Want to ground your buyer and offer in real evidence first? I can run `/competitive-research` and `/customer-research`. It adds time, but the ICP and the offer come out far sharper. Skip if you want to move fast."

- **Yes**: run `/competitive-research`, then `/customer-research` (read and follow each skill's `SKILL.md`). They write research files the next phases read.
- **Skip**: note it and move on.

Mark Phase 2 done (or note skipped).

---

## Phase 3: Buyer (/icp)

Announce: "Now we build the one buyer this whole system serves."

Run `/icp`: read and follow `.claude/skills/icp/SKILL.md`. It writes `context/icp.md`.

Confirm `context/icp.md` exists and is filled. Mark Phase 3 done.

---

## Phase 4: Offer (/offer)

Announce: "Now we build the offer they would feel stupid saying no to."

Run `/offer`: read and follow `.claude/skills/offer/SKILL.md`. It reads `context/icp.md`, scores the Value Equation, stacks the offer, and writes `context/offer.md`.

Confirm `context/offer.md` exists. Mark Phase 4 done.

---

## Phase 5: Brand

Announce: "Now we lock how the brand looks and sounds. This canon is what every piece of output obeys."

1. Run `/brand-guidelines` in build mode: read and follow `.claude/skills/brand-guidelines/SKILL.md`. It reads the buyer, offer, and voice, and writes `references/brand-guidelines.md`.
2. Run `/brand-voice`: read and follow `.claude/skills/brand-voice/SKILL.md` to lock the voice from `references/voice.md`.

Confirm `references/brand-guidelines.md` exists. Mark Phase 5 done.

---

## Capstone: prove it

Announce: "Your Memory is loaded. Let's prove it. I will make one real thing from everything we built."

Offer one flagship deliverable, operator's pick:
- a homepage hero section (run `/copy`), or
- a hero ad (run `/ads`), or
- a launch email (run `/email`).

Run the chosen skill. It reads `context/icp.md`, `context/offer.md`, `references/brand-guidelines.md`, and `references/voice.md`, and produces a real draft. Show it.

Land it: "You gave me one line of intent and got that, because the OS knows your buyer, your offer, and your voice. That is the Foundation. Every skill works like this now."

Mark Capstone done.

---

## Close

- Update the Knowledge base section of `CLAUDE.md` to point at the canon: `context/icp.md` (buyer), `context/offer.md` (offer), `references/brand-guidelines.md` (brand), `references/voice.md` (voice).
- Run `/audit` so they see the Memory layer filled and the coverage grid.
- One line: "Foundation built. Run `/audit` weekly. Run `/level-up` to start building your Fulfillment Engine, the side this kit does not pre-load."

## Critical rules

- The chain is ordered. Never run a later phase before its inputs exist.
- Each phase invokes its skill by reading and following that skill's `SKILL.md`. Do not reimplement those skills here.
- Resumable. Always read `context/.foundation.md` first and resume from the first unchecked phase.
- Phase 1 intake: seven-question cap, voice paste cannot be faked, back up before overwriting.
- Confirm before each phase. The operator can pause and resume any time.
- The three framework files in `references/` (engine-model, the-brain, the-architecture) are read-only.
- No `.env` writes during onboarding. Reach gets wired later via `/level-up`.
