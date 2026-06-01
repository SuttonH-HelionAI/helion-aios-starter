# The Brain: Shift, Scope, Ship

> Helion's operator brain. How you think, decide, and build with AI. Read it once. The `/level-up` skill walks you through all three moves every week until they become your defaults.

Tools change every six months. The model you use today may be gone next year. What does not change is how you THINK about a task, how you DECIDE what to automate, and how you BUILD and run the thing once it exists. That is the brain. Three moves: Shift, Scope, Ship.

---

## SHIFT: how you think

Before you touch a tool, you change your default. The way you look at a task decides whether you spot the leverage or walk past it.

### Default to AI
Before doing any task the old way, ask one question: **"How could AI do this?"** If the answer is "it can't do all of it," ask the follow-up: **"How could AI do the first 30 percent?"**

It is never all-or-nothing. The real question is always **"to what extent can AI carry this?"** Maybe 80 percent. Maybe 10. You do not know until you ask. Ask every time, until asking is automatic.

### Break the function down
Your job is not one big thing. It is a tree of small tasks. You do not automate your job. You automate one branch, get it working, then chain it to the next.

"Automate my marketing" sounds impossible. Break it down: ideas, copy, visuals, scheduling, replies. Each branch is its own small build. One a week, and in six months you have automated most of the tree. Compounding is real.

### Stay curious
Never run something you cannot explain. Ask the AI why it chose an approach. Ask for three alternatives and which it would pick. Push back.

A system you do not understand is a liability, not an asset. When it breaks, and it will, you will have no idea where to start. Treat AI like a mentor, not a vending machine. The vending machine hands you output. The mentor hands you understanding.

### Run the filter
Every build passes your decision filter before it ships. If it does not fit who you are and what you stand for, it does not ship, no matter how clever it is.

### Expect the dip
You will be about 20 percent slower for the first week or two. New tools, new habits. That is normal. Push through it and your baseline doubles. Get to your first ten mistakes fast. The real learning lives there, not in your first ten wins.

---

## SCOPE: how you decide

Shift tells you to look for leverage. Scope turns "I should automate something" into "here is exactly what I am building and why."

### Find the constraint
Two questions surface everything:

- **"If demand 10x'd on Monday, what would break first?"** This finds the bottleneck. Onboarding? Support? Invoicing?
- **"What would give you 10x the demand?"** This finds the growth lever. Content you are not making? Follow-up you are not doing?

One finds what is broken. One finds what could scale. Start with the constraint.

### Eliminate, Automate, Delegate (in that order)
For every process, run EAD:

1. **Eliminate first.** "What happens if we just stop doing this?" Plenty of work exists only because it always has. If nobody would notice it gone, kill it. **Do not automate waste.**
2. **Automate second.** Use the 60/30/10 rule: about 60 percent fully automated, about 30 percent AI-assisted with a human review before it goes out, about 10 percent stays manual. Full automation is rarely the goal. Anyone promising 100 percent is selling you something.
3. **Delegate third.** Too complex, too variable, too much judgment? Hand it to a person. Not everything should be automated.

Nothing stays as-is. Every process gets killed, automated, or handed off.

### Map the process
Before you touch a tool, write every step on paper. Five parts:

- **Trigger**: what kicks it off
- **Sources**: where the information comes from
- **Transformations**: how the data changes shape
- **Decision points**: where it branches
- **Destination**: where the output goes

If you cannot explain it to a person, you cannot explain it to an AI.

### Set the autonomy level
Each step gets a level. Default to the **lowest level that works.**

| Level | Name | What happens |
|---|---|---|
| L0 | Manual | No AI. You do it. |
| L1 | Suggested | AI suggests, you decide every step. |
| L2 | Drafted | AI drafts, you review and edit. |
| L3 | Supervised | AI runs, you validate periodically. |
| L4 | Autonomous | AI handles it end to end. |

Most people jump to L4 and get burned. **Workflows beat agents.** If a decision does not have to be made by AI, do not let AI make it. Push autonomy up only after you have proven the level below works.

### Tie it to a number
Every build moves one of three: more customers, more value per customer, or lower cost. Plus a specific metric (response time, error rate, conversion, time saved). **No number, no build.**

---

## SHIP: how you build and run

You have the thinking and the decision. Now you build it and run it. Helion builds with **WAT: Workflows, Agents, Tools.**

### The WAT split
- **Workflows** are the instructions. Plain-language SOPs that say what to do, in what order, with what inputs and outputs. The reasoning lives here.
- **Agents** are the decision-makers. They read the workflow and orchestrate the steps. This is the probabilistic part. Use it where judgment is genuinely needed, and nowhere else.
- **Tools** are the execution. Scripts and API calls that do the actual work. Deterministic, testable, fast.

Keeping these separate is what makes a system reliable. When AI tries to do every step itself, accuracy drops fast. Offload execution to tools and let the agent just coordinate.

### Build rules
- **Smallest blocks first.** One input, one output per block. The output of block one is the input of block two.
- **Deterministic before AI.** Get the plain, rule-based pieces working first. Then add AI only where it is actually needed.
- **Validate each step.** Run block one, confirm the output, then build block two on top of real output. Do not build the whole pipe and test at the end. That is how you end up with "it does not work and I have no idea why."

### Operate rules
- **Roll out in phases.** Manual, then reviewed, then watched, then hands-off. Even at 90 percent confidence, start with 10 percent of the volume and watch for a week.
- **Treat the AI like a new hire on day one.** Its own accounts and keys, never yours. Read-only until write is proven. Scoped permissions, nothing more. It never signs as you. Full audit trail.
- **Keep a kill switch.** If a build needs constant patching, makes low-quality output, or costs more to maintain than it saves, tear it down. "I spent three weeks on it" is not a reason to keep something that does not work.

---

Shift, Scope, Ship. That is the loop. Run it every week with `/level-up`. After a few rounds the questions stop being a checklist and start being how you think.

> **Boring is beautiful.** The best automation is the one you barely notice. Eliminate what does not need to exist, then automate what is left with the least AI possible.
