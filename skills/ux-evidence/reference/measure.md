# Measuring experience

## Question bank
Replace `[X]` with the thing under study: promotions, AI suggestions, notifications, modules. Rotate the order of grid items for each respondent.

| Construct | Wording | Scale |
|---|---|---|
| Perceived amount | "About how much of this screen is [X]?" | Slider 0-100% |
| Recognition | "How do you know something here is [X]?" | Open text; code the answers into label / position / design / mismatch |
| Noticing | "Click everything you think is [X]." | Hotspot |
| Affect | "Pick up to 5 words that describe how you feel about this element." | Balanced list of about 50 words: helpful, clear, relevant, gets in the way, distracting, sneaky, untrustworthy, and so on |
| Presence | "How do you feel about this element being here?" | 1-10 (1 dislike, 5 indifferent, 10 like). Bucket the answers 1-3 / 4-6 / 7-10 |
| Usefulness | "How useful is this element to you?" | 1-10 |
| Expectation | "Is the amount of [X] more than, about, or less than you expect?" | 5-point |
| Satisfaction grid | Amount, relevance, usefulness, clarity of labeling, visual appeal | 5-point |
| Trust (single proxy) | "[Product] has my best interests at heart." | 5-point agree |
| Confidence | "I'm confident [product] is showing me what best suits my needs." | 5-point agree. Ask before and after revealing a label |
| Mental model | "How do you think items get into this list?" | Forced choice plus "other" |
| Perceived change | "Has the amount of [X] changed in the last 6 months?" → "Where?" | 5-point plus open text |
| Ease | "How easy was it to [task]?" | 0-10 |
| Intent certainty (slicer) | "Which best describes why you came today?" | 5 levels: repeat a known action / know exactly / know roughly / comparing / just browsing |
| Behavior self-type | "Which best describes how you treat [X]?" | ignore / rarely notice / use if useful / seek out / block. **Treat as attitude, not behavior** |

## Tracker blueprint (small team)
- **Cadence:** quarterly. *Starting assumption:* 150-300 recent users each wave (active in the last 7-14 days), weighted to the user base, split by device and segment.
- **Order:** screens → frequency → device → intent certainty → overall satisfaction → rotated attribute grid with the trust proxy → follow-up for the dissatisfied (which screen, plus "describe it") → page-specific grid → perceived amount → expected vs actual → perceived change.
- **Slice by intent certainty first.** Satisfaction and trust often differ more between certain and browsing users than between demographic groups. Check this on your own data.
- **Pick drivers by regression.**
  1. After 2 waves, regress overall satisfaction (or trust) on the attribute items.
  2. Keep the top 2-3 drivers.
  3. Stop tracking the rest.
  4. Re-derive the drivers once a year.
- **Report both scores.** Report top-2-box and top-box. Top-box often moves first while top-2-box holds flat.
- **Mark significance.** Test at 95% between waves and between segments, and mark changes with arrows.
- **Open every wave with a changelog** of launches, experiments, and outside events during the field window. Readers otherwise blame the wrong cause.
- **Comparability:** any change in wording, panel, or market marks that wave "within-wave only, not trackable". Skip waves fielded in abnormal conditions.
- **Zero baseline:** run the perceived-amount question once on a screen with none of `[X]`. The floor is never 0.
- **Validate once against behavior.** Join one wave's respondent IDs to product analytics under a privacy-approved pseudonymous ID. Where stated behavior diverges from logged behavior, use the survey only for attitude.
- **Holdout:** send the same 4-6 question pulse to the long-run holdout and to the treatment in the same week.

## Metric hierarchy
```
Trust (one proxy item)
  └─ Satisfaction with the experience (amount, relevance, usefulness)
       └─ Drivers, re-derived by regression, often different per screen
Behavior (clicks, conversion, retention) runs alongside as the business outcome. It is never a stand-in for satisfaction.
```

## Experiment guardrails
- **Hypothesis:** "As we ship [mechanism], we believe [metric] rises ≥X%, because [construct]." Write it before the build.
- **Name the anticipated costs** (for example, fewer impressions, a slower page), and state the goal as a balance rather than a maximization.
- **Tier the metrics:** required / recommended / nice-to-have. Show control as the baseline, with absolute and % deltas for each arm.
- **Default launch bar:**
  - No negative effect on latency or the core business metric.
  - For customer-facing changes, a probability-of-improvement threshold (for example P(metric > 0)) that you state before launch.
  - The perception guardrail stays above its fail threshold.
- **Duration and timing:** run at least 7 days, typically 14-28. Do not ramp up on a Friday or before a holiday.
- **Pre-register what each outcome triggers:** success → ship; null → a named diagnostic; failure → a named diagnostic plus a rollback.
- **Coverage precondition:** the result counts only if the treatment reached a stated share of traffic or items.
- **Offline quality set:**
  - Label a fixed set of pairs (*starting assumption:* 100-200) with 2 blind raters.
  - Phrase the judge question in user language ("would this annoy you?").
  - Reuse the set unchanged across versions.
- **Read comparisons with `causal-claim`.** Observational log comparisons ("relevant vs irrelevant impressions from logs") carry selection bias. They are not experiments.

## Metric criteria (before a metric goes on a dashboard)
1. **Purpose:** state whether the metric drives a decision, needs pairing with another metric, or serves as an audit.
2. **Definition:** define the metric, its computation, and its time direction (looking back or forecasting forward).
3. **Call-outs:** name the top 3 call-outs and the action each one triggers. Cut any statistic that would never prompt a call-out.
4. **Worked example:** walk one entity through the metric end to end.
5. **Goal line:** show a goal line on the chart, name an owner, and record the date of the last correctness review.
6. **Gaps:** state what you would show but cannot, and why.
