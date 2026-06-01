---
name: onboard
description: Day-1 setup wizard for the Helion AIOS. Runs a 7-question interview, then scaffolds the Day-1 file set (context files, voice sample, connections table, and a filled CLAUDE.md). Idempotent and re-runnable. Triggers on "set me up", "onboard me", "/onboard", "fill in my AIOS", or a fresh clone of the starter kit.
---

# Onboard: Day-1 setup

This is the first thing the operator runs. It captures who they are and what they do, then builds the Memory layer (see `references/the-architecture.md`). Memory is non-skippable. Everything else sits on it.

One-time, but safe to re-run. Every run backs up before it writes.

## Step 1, Read the intake, find the gaps

`aios-intake.md` (repo root) is the source of truth. Read it.

If it does not exist, create it from the seed below, then continue. The seed has all seven questions with `[PLACEHOLDER]` answers.

Check each of Q1 through Q7. A question is **filled** if it has a real answer. It is **empty** if the answer is `[PLACEHOLDER]`, blank, or a stub.

- All seven filled: skip the interview. Go to Step 3 (scaffold).
- Some filled: list which are empty. Ask the operator which they want to fill now. Interview only those.
- None filled: run the full interview, Step 2.

### Intake seed (write this if `aios-intake.md` is missing)

```markdown
# AIOS Intake, source of truth for /onboard

Edit any answer and re-run /onboard to refresh your files. Keep this honest. The whole system is built on it.

## Q1, Who are you, what do you sell, who do you serve?
[PLACEHOLDER]

## Q2, Writing samples (paste 1-2 raw, do not retype)
[PLACEHOLDER]

## Q3, Top 2-3 priorities for the next 90 days (with a number or a deadline)
[PLACEHOLDER]

## Q4, Where does revenue land and get tracked?
[PLACEHOLDER]

## Q5, Where do you talk to customers, your team, and the outside world?
[PLACEHOLDER]

## Q6, Where do meeting recordings, notes, and docs live?
[PLACEHOLDER]

## Q7, The one task that eats your week, and where you track work?
[PLACEHOLDER]
```

## Step 2, The interview

Seven questions. ONE AT A TIME. Wait for the answer before asking the next. Write each answer into `aios-intake.md` (replace the `[PLACEHOLDER]`) the moment you get it, before moving on.

**Hard cap at seven. Do not invent a Q8. Do not bundle questions.**

**Q1.** Who are you, what do you sell, and who do you serve? One paragraph is enough. Name the offer and the buyer.

**Q2.** Paste one or two writing samples. Raw. Pulled straight from a real email you sent or a post you published.
> HARD RULE: if they type fresh prose into the chat instead of pasting, refuse it. Tell them: "Do not write me something new. Open a real email or post you already sent and paste it raw. The point is to capture how you actually write, not how you write when you know an AI is reading." Do not accept fresh prose as a voice sample.

**Q3.** What are your top two or three priorities for the next 90 days?
> Push back on vague answers. "Grow the business" is not a priority. Make them attach a number or a deadline to each one. "Close 3 clients by August 31" is a priority. Ask again until each one has a number or a date.

**Q4.** Where does revenue land and get tracked? Name the actual tools (Stripe, Shopify, QuickBooks, a spreadsheet, wherever the money shows up).

**Q5.** Where do you talk to customers, your team, and the outside world? Email, Slack, SMS, DMs, a CRM. List the real channels.

**Q6.** Where do your meeting recordings, notes, and docs live? Google Drive, Notion, Granola, Fathom, a folder on your desktop. Name it.

**Q7.** What is the one task that eats your week? And where do you track your work (the task list, the project board, the place you look to know what to do next)?

After Q7, stop asking. Move to scaffold.

## Step 3, Scaffold the Day-1 file set

Build all of the following in ONE batch. Before writing any file that already exists, back it up to `archives/intake-{YYYY-MM-DD}/` first. Then write.

1. **`context/about-me.md`**, from Q1 (identity and role) and Q7 (biggest time-suck). Who they are, what they do day to day, the task that drains them.

2. **`context/about-business.md`**, from Q1 (offer and who they serve) and Q4 (revenue model). What the business sells, to whom, and how it makes money.

3. **`context/priorities.md`**, from Q3. A numbered list. Each priority keeps its number or deadline.

4. **`references/voice.md`**, the Q2 samples, pasted verbatim, unedited. Add one header line at the top: "Voice reference. When writing anything external in my voice, match the register below. Show me a draft before sending." Then the raw samples.

5. **`connections.md`**, the seven-domain table, populated from Q4 through Q7. Tag each row with the engine it serves per the mapping in `references/engine-model.md` and `references/the-architecture.md`. Use this template:

```markdown
# Connections, every system your AIOS can reach

Tagged by engine. Mechanism is how the AIOS reaches it. Run /audit to see coverage and freshness.

| # | Domain | System | Engine | Mechanism | Auth |
|---|---|---|---|---|---|
| 1 | Revenue and financials | {from Q4} | Growth | not yet connected | none |
| 2 | Customer interactions | {from Q5} | Growth | not yet connected | none |
| 3 | Calendar | {if named, else blank} | Both | not yet connected | none |
| 4 | Communication | {from Q5} | Both | not yet connected | none |
| 5 | Project and task tracking | {from Q7} | Fulfillment | not yet connected | none |
| 6 | Meeting intelligence | {from Q6} | Fulfillment | not yet connected | none |
| 7 | Knowledge and files | {from Q6} | Both | not yet connected | none |
```

   Fill the System column from the operator's answers. Where a domain was not named, leave System blank but keep the row. Engine tags are fixed as above (the mapping comes from the architecture's seven-domain table). Every Mechanism on Day 1 is "not yet connected" and every Auth is "none". Reach gets wired later, one tool at a time.

6. **`CLAUDE.md`**, fill every `{{...}}` placeholder:
   - `{{business_name}}`, from Q1
   - `{{your_name}}`, from Q1
   - `{{primary_priority}}`, the top item from Q3
   - Knowledge base section, a short paragraph from Q1 and Q3: what they do, who they serve, what matters this quarter
   - Voice summary, one or two lines describing the register from Q2 (do not paste the full samples here, point to `references/voice.md`)
   - Connections summary, one line per wired-or-named domain from `connections.md`, tagged by engine

Do not write to `.env`. Do not wire any tool. Day 1 is Memory only.

## Step 4, The closing screen

Three lines. No more.

```
Day 1 done. Your Memory layer is built.
Today: ask me "what should I focus on this week?"
Tomorrow: wire one tool from connections.md. Day 7: run /audit.
```

When they run the closing prompt ("what should I focus on this week?"), answer ONLY from the new context files. Do not browse. Do not pad.

- Three bullets. A priority list, in their voice (match `references/voice.md`).
- Each bullet ties to one priority from `context/priorities.md` (Q3).
- The final line names the single thing to do Monday, then asks the Shift question: "To what extent could AI carry this?"

That last question is not filler. It plants the Brain's Shift habit (see `references/the-brain.md`) before `/level-up` ever teaches it formally.

## Critical rules

- Seven-question cap is non-negotiable. No Q8.
- The voice paste (Q2) cannot be skipped or faked. Refuse fresh prose.
- The scaffold is one shot. All six artifacts in one batch.
- Idempotent. Back up any existing file to `archives/intake-{date}/` before overwriting.
- The closing screen is three lines.
- Do not generate extra skills. The kit ships with three.
- The three `references/*.md` framework files (engine-model, the-brain, the-architecture) are read-only. They ship with the kit. Never edit them.
- No `.env` writes on Day 1.
