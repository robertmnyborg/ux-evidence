---
name: ux-evidence
description: Ground UI and UX work in evidence before pixels. Gate a new or changed user-facing flow or screen through six questions (customer evidence, one ranked pain, PR + hard FAQs, assumption map, cognitive walkthrough, success metric + perception guardrail + kill condition), pick the research method that answers a UX question, write perception and trust questions, design an experience tracker, and judge a design against research-backed principles (clutter budgets, usefulness over relevance, certainty-stacked layout, provenance-safe lists). Use when planning or changing a screen, flow, dashboard, or module; choosing between UI variants; setting a launch bar for a UI change; asking "will users find / trust / understand this"; or writing a research plan, design review, or findings report. Hands visual craft to a design skill such as `impeccable`.
version: 0.1.0
---

# UX evidence

Good UX is a claim about how people behave. Treat each design decision as a hypothesis and name the evidence that would overturn it before building. Craft (type, color, motion, polish) belongs to a design skill such as `impeccable`. This skill decides what to build and how you will know it works.

## Gates before UI code

Scale the gates to the stakes:
- **No gates:** a reversible tweak inside an established pattern (button copy, a label, spacing, color within tokens). Answer the question directly and briefly. Do not prescribe a test, a metric, or a process.
- **G1 + G6, two lines:** a new component inside an existing flow.
- **All six:** a new screen, flow, or module, or any change that inserts content into what users already rely on.

Run the gates in order, and write the answers at the top of the plan or spec.

**Thresholds are numbers.** Never leave "X%", "TBD", or "set from baseline". When no baseline exists, propose a starting number, label it provisional, and say which reading will revise it ("≥30% of alerts opened within 7 days; provisional; reset after 4 weeks of data").

| Gate | Question it answers | Minimum output |
|---|---|---|
| **G1 Customer + evidence** | Who arrives, in what state of certainty, and what says they have this problem? | One user and situation. Each claim carries a source and an evidence level (use the `job-card` ladder if you have it). Simulated users and team opinion are level 0. |
| **G2 One pain** | Which single pain does this solve, and why that one? | 3 candidate pains, ranked by frequency × severity. Pick one. |
| **G3 PR + hard FAQs** | Would the user care, and what will disappoint them? | A 3-sentence press-release paragraph plus 5 hard FAQs, including "what did we reject and why". Cut every element that does not serve the pain. |
| **G4 Assumptions** | What must be true? | A story map of activities → steps. Tag each assumption Value, Usability, Feasibility, or Viability. Name the riskiest one. |
| **G5 Walkthrough** | Can a newcomer predict each next step? | A cognitive walkthrough on low-fidelity scenarios (method card in `reference/methods.md`). An agent-run walkthrough is level 0. Say so. |
| **G6 Launch bar** | Which number moves, which must not get worse, and what kills it? | A success metric with a target, a perception guardrail with a fail threshold, a kill condition, and a rollback. Write them before the build. |

Keep visuals low-fidelity until G3 passes. High-fidelity mocks pull reviewers into pixel arguments and away from the experience.

## Pick the method

Choose by the question, not by habit. Full cards are in `reference/methods.md`. The sample sizes are starting assumptions for directional reads, not power calculations. Raise them when you need to size an effect.

| Question | Method | Starting n |
|---|---|---|
| Can a newcomer learn this flow? | Cognitive walkthrough | 3-4 proxies, 1 session |
| Does this label or link tell people where it leads? | Expectation test | 10 per variant |
| What do people notice, and how do they feel about each element? | Hotspot perception survey | 100+ per page |
| How much added content will people tolerate? | Monadic density ladder | 100+ per cell; 5 recorded sessions per cell for the why |
| What belongs on the page, and in what order? | Participatory "build the ideal page" | 2-3 groups of 4-6 |
| Is the prototype better than today? | Prototype usability with a baseline cell | 3 per cell, 5+ total |
| Do people notice a disclosure, and does it change trust? | Retrospective live-task walkthrough | 10-25 |
| What grabs attention vs what matters? | Importance ranking plus first-click | 100+ |
| Did the change hurt experience over months? | Holdout survey | Same pulse to both arms |
| How do we compare to rivals without brand bias? | Blind competitive panel | 1 product per respondent |

Run qualitative first to find the why, then quantitative to size it. Triangulate observation, self-report, and support or feedback channels. Never rest a decision on one channel.

## Judge a design

Before presenting any UI, check it against `reference/principles.md`. The six checks that catch most failures:
1. **Module budget.** Every block states the user benefit it delivers. Merge or cut near-duplicates.
2. **Certainty stack.** The first viewport carries glance-level decision data for the most certain user. Alternatives and exploration sit lower.
3. **Provenance.** A list titled by its source ("your history", "your team's") contains only that source. Paid, AI, or third-party items sit in a labeled container with a stated reason.
4. **Destination and return.** Each link label names the object, the owner, and where it lands. Each detour has a visible way back.
5. **Attention vs importance.** Loud emphasis needs substance behind it. Measure first click and intent separately.
6. **Balance.** Curated content shows its spread (counts, a low and a high example). All-positive content reads as hiding something.

## Input-request artifacts

A sheet, form, or doc that colleagues fill in or confirm is a UI, and its users skip anything that looks like work. The message that links it should open with who must act, what they must do, and by when.
1. **Exceptions only.** Show each person only the rows that need them. Confident rows ship without review.
2. **Default the answer.** The header states what silence means: "Ships [date] as shown unless you change it." No Y/N confirm column.
3. **Prefill the lookups.** Any field the reader would have to research (an address, an email) gets a default they override.
4. **One person, one place.** Each person's rows live on one tab or file. Work for another role (ops, a manager assigning owners) goes elsewhere.
5. **Input column first.** Column A is what they type. Reference columns are grouped or hidden.
6. **Instructions where the eye is.** One frozen line at the top of each tab. No Read me tab.
7. **Cold test.** A colleague seeing it for the first time finishes their part in 5 minutes without a question, or it is not ready.

The common failure: many tabs, a long Read me on the last tab, one person's rows split across tabs, and required fields left empty. A sheet like that sits untouched.

## Measure

Use `reference/measure.md` for question wording, tracker design, and metric criteria. Three rules carry most of the weight:
- **Measure perceived, not shipped.** Ask how much of the screen people think is X, and run the question once on a clean baseline.
- **Behavior is not satisfaction.** People keep using things they dislike. Pair every behavioral A/B test with a perception guardrail, and read long-run effects from a surveyed holdout.
- **Stated behavior measures attitude only.** "I never click those" predicts nothing about clicks.

## Write it up

Use the templates for any artifact another person reads:
- `templates/research-plan.md` for a study you will run.
- `templates/design-review.md` for a design decision you want settled.
- `templates/findings-report.md` for results.

Every finding follows claim headline → evidence (n, effect, a quote) → IMPLICATION for the decision owner. Every claim cites an observation ID or a number.

## Hand-offs
These skills are optional. Use them if installed; otherwise do the step inline.
- Visual craft, critique, polish → `impeccable` (`shape` after G1-G4, `critique` after the build).
- Coding qualitative data into themes → `trustworthy-insights`.
- Reading an A/B or holdout comparison → `causal-claim`.
- Naming the buyer or job → `job-card`.
- Picking between built variants → build them side by side and judge them against G6.
