# Method cards

Each card gives the question the method answers, the setup, the minimum n, what to measure, when not to use it, and a solo version. The solo version is for one builder plus the agent, with no research team. Sample sizes are starting assumptions for directional reads, in line with common practitioner defaults. Raise them when you need to size an effect.

---

## 1. Cognitive walkthrough
- **Answers:** Can a newcomer learn this flow? Where does the interface fail to signal the next step?
- **Use when:** designs are low-fidelity (sketches, a click-through), the tasks are known, and the user is known.
- **Do not use for:** value or usefulness, severity, how often a problem happens, proof of zero issues, fine interaction nuance (double-click vs drag), or ideation.
- **Route elsewhere:**
  - A design expert's gut check is enough → heuristic critique (`impeccable critique`).
  - The change is a one-way door (it costs trust or cannot be reversed) → usability test with 5+ real users.
  - The users are unlike any available proxy → generative interviews.
- **Setup:**
  - 1 session of 60-90 minutes.
  - 3-4 proxy participants: mixed roles, unfamiliar with the feature, with baseline domain knowledge.
  - 1-3 scenarios. Each takes one deep slice of the flow, not the whole flow.
  - A persona for each scenario.
- **Roles:**
  - The facilitator leads the session.
  - Participants act as the persona.
  - The designer takes notes and stays silent.
  - Observers stay silent.
- **Loop at each step:**
  1. Before revealing the next screen, ask: "What would you do next?"
  2. After revealing it, ask: "Is this what you expected to see?"
- **Ground rules:** no redesigning in the room, no defending the design, no debating theory.
- **Output:** one row per step, logged as step | predicted action | expected? | issue ID.
- **Solo:** The agent plays the persona against the actual screens, one screen at a time. It must commit to a prediction before it sees the next screen. Label the output level 0. Confirm the top 3 issues with one real person.

## 2. Expectation test (labels, links, navigation)
- **Answers:** Does this label or entry point tell people where it leads? Will they know how to get back?
- **Setup:**
  - Show a static screenshot.
  - Ask in this order:
    1. "What matters to you on this page?"
    2. "Is anything confusing?"
    3. Circle one element and ask "Where would you land if you clicked this?" Ask it open-ended first. Then repeat it with rotated closed options.
    4. Show the real destination.
    5. Ask them to rate the match: Better / Matches / Different / Worse / Unsure.
    6. Ask "How would you get back?"
- **n:** 10 per variant. Run a 2×2 (for example, label A/B × with/without a cue) as 4 cells of 10.
- **Measure:** the distribution of predicted destinations, the match distribution, and the count who cannot find the way back.
- **Solo:** Run it unmoderated on a testing panel, with 10 people per variant, in about a day.

## 3. Hotspot perception survey
- **Answers:** Which elements do people notice or classify as X (an ad, AI-generated, paid, optional)? How do they feel about each one?
- **Setup:**
  - Use a full-page screenshot matched to the device the respondent uses.
  - Give a realistic scenario ("you want to do Y and arrived here").
  - Ask, in this order:
    1. Estimate what % of the page is X (slider, 0-100).
    2. "How do you know?" (open text, coded later).
    3. "Click everything you think is X."
    4. For one randomly assigned clicked element: pick up to 5 adjectives from a balanced list of about 50 positive and negative words.
    5. Rate its presence on a 1-10 like scale (5 = indifferent).
    6. Rate its usefulness on a 1-10 scale.
- **n:** 100+ per page variant for a direction; thousands only when sizing a population.
- **Measure:** % who flag each element, adjective clusters, and the correlation between "like presence" and "useful".
- **Do not use for:** behavior. This method measures perception only.

## 4. Monadic density ladder
- **Answers:** How much added content (modules, badges, promotions, AI suggestions) will people tolerate before satisfaction or trust drops?
- **Setup:**
  - Clone one base page into 4-6 levels: none, simplified, current, more, and saturated.
  - Each respondent sees exactly one level.
  - Hold relevance constant (relabel the same items) so that quantity is the only variable.
  - Cross the levels with intent: exact task vs browsing.
- **n:** 100+ per cell for the survey. Add 5 recorded sessions per cell to get the why.
- **Measure:**
  - Perceived % of the page that is X.
  - % rating the page "excellent" on quality, relevance, usefulness, and navigation.
  - "Which would you choose?" as a hotspot. This also tells you whether people choose above or below the fold.
  - Ease, on a 0-10 scale.
  - Trust.
- **Read:** Look for the knee in the curve, separately by device and by intent.

## 5. Participatory "build the ideal page"
- **Answers:** What belongs on the page, what order it goes in, and what is clutter.
- **Setup:**
  - Groups of 4-6, about 2 hours.
  - Split each group by device or by user certainty: "sure what I want" vs "researching".
  - Run three exercises:
    1. Card-sort every page element into importance piles.
    2. Build the ideal page on paper. Participants may omit elements and invent new ones.
    3. Introduce a new stimulus and ask them to place it.
  - Photograph each artifact.
  - Regroup: each half critiques the other half's page.
- **n:** 2-3 groups.
- **Measure:**
  - How often each element was omitted.
  - Where each element was placed: above the fold / middle / end.
  - The reason given for each element.
- **Write it as:** competing hypotheses to falsify, for example "users want X high" vs "users want X low".

## 6. Prototype usability with a baseline cell
- **Answers:** Is the new design better than how people do the task today?
- **Setup:**
  1. Have the participant do the task their current way first. This is the baseline.
  2. Then have them explore the prototype under a persona scenario.
  3. Run a sequential cell (A then B) to get a direct comparison.
- **n:** 3 per cell, 5+ total.
- **Measure:**
  - Rating vs current, on a 1-5 scale.
  - Attributes: easy to navigate, confident to decide, credible, worth returning to.
  - Each feature's expected behavior vs its actual behavior.
- **Solo:** Run it unmoderated with a clickable prototype and 5 sessions. Watch every recording before you summarize.

## 7. Retrospective live-task walkthrough
- **Answers:** Do people notice a disclosure or label? How do they define "relevant" vs "useful"? Does trust change once they understand?
- **Setup:**
  1. The participant does a real task on the live product.
  2. They walk back through the specific elements.
  3. They classify each element on the same rubric your own reviewers or policy team use. This yields the user-vs-reviewer disagreement rate.
- **Coding rule:** code "noticed the label" only when the participant mentions it unprompted.
- **Trust:** ask about trust twice, once before you point out the label and once after.
- **n:** 10-25.

## 8. Importance ranking plus first click
- **Answers:** What grabs attention vs what actually drives the decision?
- **Setup:**
  - Rank the elements, or select every element that is essential.
  - Ask "click what you look at first", then "click what you look at second".
  - Run a monadic A/B of 2 treatments, measuring intent (top-2-box).
- **Read:** A loud element can win first click and still lower intent. Report both.

## 9. Holdout survey
- **Answers:** Did a shipped change hurt the experience over weeks or months, when the A/B test looked flat?
- **Setup:**
  - Keep a small long-run holdout (*starting assumption:* 5-10% of traffic).
  - Send the same short pulse (4-6 questions) to the holdout and the treatment in the same week.
  - Regress with controls if the arms are imbalanced.
- **Why:** Behavior stays flat while attribution shifts. Over months, users name the specific element as their reason for dissatisfaction.

## 10. Blind competitive panel
- **Answers:** Does our owned survey flatter us? Where do we stand against rivals?
- **Setup:**
  - Use a third-party panel with no brand reveal.
  - Each respondent rates only the one product they used in the past week.
  - Ask no head-to-head questions.
  - Run it twice a year.
- **Solo:** A paid-panel survey rating you and 2 competitors on the same 6 questions.

---

## Running any study
1. **Brief:** goal, research questions, participant profile, method, timeline. Have stakeholders review it before you recruit.
2. **Recruit first,** because recruiting takes longest. Use a screener, a confirmation, and a reminder 1 day before.
3. **Rehearse:** run a pilot session to test the setup before session 1.
4. **Daily summary:** send one each day of fielding, with recording links.
5. **Top line:** send it within 48 hours of the last session.
6. **Report:** write a short narrative (a few pages). Label quotes by persona, not by name. Put the full discussion guide in the appendix so anyone can rerun it.
7. **Log:** give every observation an issue ID in a running frustration log, and cite the IDs in claims.

## Standing program for a product with users
The cadences and counts below are starting assumptions. Scale them to your team.
- **Monthly:** about 10-30 recorded real-task sessions, logged into the frustration log.
- **Quarterly:** a perception tracker (`measure.md`).
- **Twice a year:** a blind competitive panel.
- **For every major UI experiment:** pre-test qualitative input to narrow the concepts, then a post-test holdout survey.
