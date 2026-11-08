# Design review: <feature>

**Author:** <name> · **Audience:** <reviewers> · **Summary:** <one line>
**Preconditions:** A peer review is done. The doc is short (a few pages excluding the appendix). No code is shown as design.

## Review goals: questions to settle
1. <A specific question with a recommended answer. Example: "Separate container or inline? We recommend separate.">

## Outcome *(fill in after the review)*
- **Date:**
- **Disposition:** proceed / redesign
- **Action items:**

| Item | Owner | Date |
|---|---|---|
| | | |

## Problem
- **Who:** <user + intent certainty>
- **Problem:** 
- **Benefit:** 
- **How we know:** <evidence with source + level>

## Goals as user stories
- As a <user>, I want <action> so that <outcome>.

## Business justification
<Data, plus the cost of doing nothing.>

## Proposed design
<One option, mapped to each goal. Low fidelity until the goals pass review.>

## Assumptions
Tag each one Value, Usability, Feasibility, or Viability. Mark the riskiest.

## Non-goals
<Each with the reason it is out of scope.>

## Alternatives considered
| Option | Pros | Cons | Why rejected |
|---|---|---|---|
| | | | |

## Design detail
- **Components reused:** 
- **New components:** 
- **Data and API changes:** 
- **States:** empty, loading, error, overflow, first-run

## Principle check
`ux-evidence/reference/principles.md`. Mark each pass / fail / n/a:
- Module budget
- Certainty stack
- Provenance
- Destination and return
- Attention vs importance
- Balance

## Determining success
| Metric | Type | Target / fail threshold | Source |
|---|---|---|---|
| | success | | |
| | perception guardrail | | |
| | business guardrail | | |

- **Kill condition:** 
- **Rollback:** 

## Failure scenarios and degraded UX

## Risks
| Risk | Cause | Severity | Likelihood | Mitigation |
|---|---|---|---|---|

## Remaining considerations
<Accessibility, privacy, performance, localization, cost, operations.>
