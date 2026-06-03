---
name: onboard
description: Builds the operator's Foundation. A resumable chain that loads the Memory layer deep: intake, then the buyer, the offer, and the brand, ending with one real deliverable that proves it works. Triggers on "set me up", "onboard me", "/onboard", "build my foundation", "fill in my AIOS", or a fresh clone of the starter kit.
---

# Onboard: build your Foundation

This is the deepest and most important thing the operator runs. It is not a quick setup. It is a Foundation: a chain that loads the Memory layer (see `references/the-architecture.md`) so deep that when the operator later asks the OS for real work, it is flawless, because it already knows their buyer, their offer, and their voice cold.

Depth over speed. This can take a couple of hours. It is resumable. The operator runs it across sittings.

## The depth standard (every phase obeys this)

Shallow Memory is the only way this fails. Generic in, generic out. Hold this bar and the operator ends with an OS that knows them cold.

- **No placeholders.** Never leave `{{...}}`, "TBD", or a vague stub in a file. Get the real answer first.
- **Push back on vague.** "Grow the business" is not a priority; "20 clients by Sept 30" is. "Busy founders" is not a buyer; a named role with a named pain is. One sharp follow-up whenever an answer is thin.
- **Use the real source.** Their site, their numbers, their real customer language, their named competitors. Fetch and read before you write. Guessing is what makes a generic OS.
- **Specifics only.** Names, numbers, dates, verbatim phrases. If a line could describe any business in their category, rewrite it until it could only be them.
- **Verify before you check the box.** Re-read the file you wrote. Substantive and specific, or filler? Fix filler before marking the phase done. A checked box on thin work is worse than an honest gap.

## How the chain works

Six phases plus a proof step, in order. Each phase writes a canonical file the next phase reads. No skipping ahead: you cannot build an offer without a buyer, or lock a brand without an offer.

```
Phase 1  Intake    -> context/about-me, about-business, priorities, voice, connections (skeleton)
Phase 2  Map       -> context/business-map.md (seven buckets) + connections.md tools  (the-seven-buckets)
Phase 3  Evidence  -> named competitors + real customer language (grounds the ICP)
Phase 4  Buyer     -> context/icp.md            (/icp)
Phase 5  Offer     -> context/offer.md          (/offer)
Phase 6  Brand     -> references/brand-guidelines.md + voice.md  (/brand-guidelines, /brand-voice)
Capstone Proof     -> one real flagship deliverable from the full stack
```

## Resume logic (do this first, every run)

Read `context/.foundation.md` if it exists. It tracks which phases are done.
- **Missing**: first run. Create it from the template below, all unchecked. Start at Phase 1.
- **Exists**: resume at the first unchecked phase. Tell the operator where they are: "You are through [N] of 7. Picking up at [phase]."

After each phase completes, check its box in `context/.foundation.md`, mark the win out loud ("That is [N] of 7 done"), then ask: "Keep going to [next phase] now, or pause here? You can resume any time by running `/onboard`, and it picks up exactly here." Honor the answer. The chain is long on purpose; keep the operator moving with small wins, not pressure.

### Status template (`context/.foundation.md`)

```markdown
# Foundation status
- [ ] Phase 1: Intake
- [ ] Phase 2: Map your business (the seven buckets)
- [ ] Phase 3: Evidence (ground the buyer)
- [ ] Phase 4: Buyer (/icp)
- [ ] Phase 5: Offer (/offer)
- [ ] Phase 6: Brand (/brand-guidelines, /brand-voice)
- [ ] Capstone: Proof
```

---

## Phase 1: Intake

Capture who they are and what they do. Builds the base of the Memory layer.

**The intake file.** `aios-intake.md` (repo root) is the source of truth. Read it. If it is missing, create it from the seed in `aios-intake.md`'s structure (seven questions, placeholder answers), then continue.

**Interview.** Walk the seven core questions, ONE AT A TIME, writing each answer into `aios-intake.md` the moment you get it. The seven are the spine, not a ceiling: when an answer is thin or high-value, ask one sharp follow-up before moving on (the depth standard applies). Do not bundle questions, and do not interrogate, probe only where it raises quality.

1. Who are you, what do you sell, who do you serve, and what is your website? One paragraph plus the URL. Name the offer and the buyer. If they have no site yet, accept "none yet" and move on. Capture the website first, it is the single highest-leverage input for the phases that follow.
2. Paste one or two writing samples, raw, from a real email or post you already sent. HARD RULE: if they type fresh prose instead of pasting, refuse. "Do not write me something new. Paste raw from something you already sent. The point is how you actually write, not how you write for an AI." Never accept fresh prose.
3. Top two or three priorities for the next 90 days. Push back on vague. Make each one carry a number or a deadline.
4. Where does revenue land and get tracked? Name the real tools.
5. Where do you talk to customers, your team, and the outside world?
6. Where do meeting recordings, notes, and docs live?
7. The one task that eats your week, and where you track work?

**Scaffold (one batch, back up any existing file to `archives/intake-{date}/` first):**
1. `context/about-me.md` from Q1 + Q7, plus their **why and point of view**. If it is not already clear, ask one short question: "In a line or two, why do you do this, and what do you believe about your space that most others get wrong?" Capture it verbatim. This is what makes later content sound like a person, not a brand.
2. `context/about-business.md` from Q1 + Q4, including the **website URL** on its own line. If they gave a website, **fetch it now with WebFetch, and not just the homepage**: pull the home, about, pricing, and product or services pages, plus their most prominent piece of content. From those, write into `context/about-business.md`: what they sell with the full offer or product list and prices, their positioning and proof, the exact words and phrases they use (for voice), and a one-line **business type** (services, ecommerce, creator, agency, local, or other, inferred from the site and Q1, confirmed with the operator). Business type tailors the ICP, the offer, and the proof piece, so set it now. This is the strongest grounding in the whole chain, so go deep. If the site is thin or missing, say so and capture the same facts by asking.
3. `context/priorities.md` from Q3 (numbered, keep numbers and dates).
4. `references/voice.md` from Q2, pasted verbatim, with a one-line header on how to use it.
5. `connections.md`, the seven-bucket table, each row tagged by engine per `references/the-architecture.md`. Leave the Tool column empty for now; Phase 2 fills it from the business map. Mechanism "not yet connected", auth "none".
6. `CLAUDE.md`, fill every `{{...}}` placeholder ({{business_name}}, {{your_name}}, {{primary_priority}}, knowledge base, voice summary, connections summary).

No `.env` writes. Reach gets wired later.

Mark Phase 1 done in `context/.foundation.md`.

---

## Phase 2: Map your business (the seven buckets)

The intake gave the broad strokes. Now map the business across the **seven buckets** every business runs on (`references/the-seven-buckets.md`): Revenue, Customer, Calendar, Comms, Tasks, Meetings, Knowledge. This is what makes the Memory layer operational. The OS learns the business by domain, and this map becomes the roadmap for the whole build that follows.

**Reuse the intake. Do not re-ask what you already know.** Pull tools straight from Phase 1: Q4 gives Revenue, Q5 gives Comms and Customer, Q6 gives Meetings and Knowledge, Q7 gives Tasks. Confirm those out loud, then ask only the genuine gaps. The intake never asks about the **Calendar** bucket and folds **Customer** into comms, so those two almost always need a real question.

**Walk the seven buckets, ONE AT A TIME.** For each bucket, capture four things in plain words:
1. **The tool** that holds it. The real app or place.
2. **The one task that eats your time** in this bucket.
3. **What you wish the OS did here.** The dream hand-off.
4. **Priority**: high, medium, or low, set from how big that time-sink is.

Keep it fast. Most buckets are one short exchange because the tool is already known from the intake. Spend the real time on the time-sink and the want, because those two become the build queue.

**Write `context/business-map.md`** (back up any existing one to `archives/business-map-{date}/` first). Fill every bucket with all five fields: what lives in it, the tool, the time-sink, the want, the priority. Set each bucket's status to "mapped".

**Sync `connections.md`.** Copy each bucket's tool into the Tool column. Mechanism stays "not yet connected"; the wiring happens later in `/level-up`.

**Surface the roadmap.** Name the one or two highest-priority buckets back to the operator: "Your biggest time-sinks are [bucket] and [bucket]. That is where `/level-up` will point first." This is the moment the map proves its worth, so do not skip it.

Mark Phase 2 done in `context/.foundation.md`.

---

## Phase 3: Evidence (ground the buyer in reality)

The next phase, the ICP, is required, and an ICP built from memory alone is a guess. This phase grounds it in real data. No API key to set up: `/competitive-research` and `/customer-research` now run on built-in web search.

Offer the full pass: "Want the deep version? I run `/competitive-research` and `/customer-research` first. It adds time, but your ICP and offer come out grounded in real competitor moves and real customer language. Or I do a quick scan and we keep moving."

- **Deep**: run `/competitive-research`, then `/customer-research` (read and follow each skill's `SKILL.md`). They write research files the next phases read.
- **Quick (the minimum, never fully skip)**: do a short built-in web scan yourself with WebSearch. Capture the names of 2 to 3 real competitors and 3 to 5 verbatim phrases real customers use for this problem (pulled from reviews, forums, social). Save them to `research/quick-scan-{date}.md`. The ICP reads this.

Grounding is not optional, only its depth is. Never let the ICP run on memory alone.

Mark Phase 3 done.

---

## Phase 4 (required): Buyer (/icp)

This phase is required, not optional. The whole system serves one buyer, and every phase after it (offer, brand, the proof piece, and every Growth skill) reads `context/icp.md`. You cannot skip it or move past it. If the operator asks to skip, explain plainly that nothing downstream works without it, and stay on this phase until it is done. Pausing and resuming is fine; skipping is not.

Announce: "Now we build the one buyer this whole system serves. This one is not optional, everything else is built on it."

Run `/icp`: read and follow `.claude/skills/icp/SKILL.md`. Hand it the website findings already saved in `context/about-business.md` so the profile is grounded in real language, not guesses. It writes `context/icp.md`.

Confirm `context/icp.md` exists and is genuinely filled, not a placeholder or a thin sketch. Only then mark Phase 4 done.

---

## Phase 5: Offer (/offer)

Announce: "Now we build the offer they would feel stupid saying no to."

Run `/offer`: read and follow `.claude/skills/offer/SKILL.md`. It reads `context/icp.md`, scores the Value Equation, stacks the offer, and writes `context/offer.md`.

Confirm `context/offer.md` exists. Mark Phase 5 done.

---

## Phase 6: Brand

Announce: "Now we lock how the brand looks and sounds. This canon is what every piece of output obeys."

1. Run `/brand-guidelines` in build mode: read and follow `.claude/skills/brand-guidelines/SKILL.md`. It reads the buyer, offer, and voice, and writes `references/brand-guidelines.md`.
2. Run `/brand-voice`: read and follow `.claude/skills/brand-voice/SKILL.md` to lock the voice from `references/voice.md`.

Confirm `references/brand-guidelines.md` exists. Mark Phase 6 done.

---

## Capstone: prove it

Announce: "Your Memory is loaded. Let's prove it. I will make one real thing from everything we built, aimed at your number-one priority."

Pick the deliverable that serves their top priority in `context/priorities.md`, operator's choice from:
- a homepage hero section (run `/copy`), or
- a hero ad (run `/ads`), or
- a launch email (run `/email`).

Run the chosen skill. It reads `context/icp.md`, `context/offer.md`, `references/brand-guidelines.md`, and `references/voice.md`, and produces a real draft. Show it.

**Then run the teammate test.** This is the litmus test, lived. Ask the OS a real question only a teammate would know, like "what is our sharpest angle against [competitor]?" or "who exactly do we serve and what do they say their problem is?" Answer it from the Memory you just built, and cite the file. If the answer is sharp and sourced, the Foundation took. If it is thin, the Memory is thin, go back and deepen the weak file before you close.

Land it: "You gave me one line of intent and got a real draft, and I just answered a real question about your business from memory. That is the Foundation. Every skill works like this now."

Mark Capstone done.

---

## Close

- Update the Knowledge base section of `CLAUDE.md` to point at the canon: `context/icp.md` (buyer), `context/offer.md` (offer), `references/brand-guidelines.md` (brand), `references/voice.md` (voice).
- Run `/audit` so they see the Memory layer filled and the coverage grid.
- **Hand them their first week.** From `context/priorities.md` and the highest-priority buckets in `context/business-map.md`, write a short, concrete plan into `context/first-week.md`: day by day, what to run and which bucket it serves. Make day one a single winnable build, not a list. This turns "what do I do now?" into a clear next step.
- One line: "Foundation built, and your first week is in `context/first-week.md`. Run `/audit` weekly. Run `/level-up` to start building your Fulfillment Engine, the side this kit does not pre-load."

## Critical rules

- The chain is ordered. Never run a later phase before its inputs exist.
- Each phase invokes its skill by reading and following that skill's `SKILL.md`. Do not reimplement those skills here.
- Resumable. Always read `context/.foundation.md` first and resume from the first unchecked phase.
- Phase 1 intake: seven-question cap, voice paste cannot be faked, back up before overwriting.
- Confirm before each phase. The operator can pause and resume any time.
- The three framework files in `references/` (engine-model, the-brain, the-architecture) are read-only.
- No `.env` writes during onboarding. Reach gets wired later via `/level-up`.
