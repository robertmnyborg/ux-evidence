# Design principles

Each principle has three parts:
- **Why:** the mechanism behind it, in line with widely published usability and perception research.
- **Apply:** how to use the principle on any UI.
- **Check:** a yes/no test to run against a design (where one fits).

Numbers marked *Starting assumption* are defaults to begin with, not benchmarks. Replace them with your own measurements as soon as you have any, and never quote them as findings.

## Layout and density

**1. People count clutter, not just the thing you labeled.**
- **Why:** Perceived amount of something (ads, promotions, AI suggestions) follows the total visual noise on a screen, not the true share. Even a screen with none of it is rarely perceived as zero.
- **Apply:** Budget the total number of modules, badges, and labels per screen, not only the commercial ones.
- **Check:** Can you name the user benefit of every block? Cut or merge the blocks you cannot.

**2. Small viewports punish volume.**
- **Why:** Each added module costs more on mobile, where it pushes everything else below the fold.
- **Apply:** Set a separate content budget per viewport. Never port a desktop stack to mobile unchanged.

**3. Stack the page by user certainty.**
- **Why:** Users who already know what they want expect to act without scrolling. Users who are researching accept a deep scroll. A starting order to test:
  1. decision essentials
  2. required companions
  3. facts
  4. social proof
  5. alternatives
  6. everything else
  7. a clear end
- **Apply:** Map each page zone to a certainty state. The first viewport holds glance-level decision data only. Test the order (method card 5) rather than assuming your team's intuition is right.

**4. Tolerance falls as intent gets specific.**
- **Why:** Inserted items are a detour for someone with an exact task and a discovery aid for someone browsing.
- **Apply:** Adapt density to intent signals: tight for navigational tasks, looser for exploration. *Starting assumption:* about 2 inserted items in the top row for exact tasks, about 4 for browsing. Find your own knee with a density ladder (method card 4).

**5. Redundant modules read as clutter.**
- **Why:** Near-identical modules make users do the deduplication work.
- **Apply:** Keep one module per distinct job, and give each a title that names its benefit ("Under $50 with free returns", not "Related").

**6. Put irrelevant content last.**
- **Why:** Acceptance falls as content moves from on-topic to off-topic to unrelated. Placed at the end, low-relevance content also signals that the page is over.

**7. Use progressive disclosure for heavy content.**
- **Why:** Long specification or review sections bury the summary most people want.
- **Apply:** Show a summary, one low and one high example, and the controls. Show counts, not only percentages. Expand on demand.

## Usefulness and trust

**8. Usefulness beats relevance.**
- **Why:** People like an element being present roughly to the degree they find it useful. "Relevant" tends to mean an exact match. "Useful" means relevant plus a visible reason (rating, price, history), or a substitute *with the trade-off explained*.
- **Apply:** When you show a non-exact result, state what it gives up and why it is still worth a look.

**9. Keep provenance-titled lists pure.**
- **Why:** A list titled by its source ("your history", "people like you") makes a promise. Foreign items in it feel like a trick. Lists titled editorially ("Under $X") absorb mixed sources with little damage.
- **Apply:** A list titled by its source ("your history", "your team's", "verified") contains only that source.

**10. Separation plus a stated benefit restores trust.**
- **Why:** Items in a separate, labeled container that says what is in it for the user read as honest. Disguised mid-list insertions read as deceptive and are often not recognized at all.
- **Apply:** Paid, AI-generated, or third-party items go in a labeled container with a reason. Insert them at predictable positions.

**11. Past a tipping point, the container changes identity.**
- **Why:** Once inserted items outnumber organic ones, users re-read the whole module as serving the business first.
- **Apply:** *Starting assumption:* cap inserted items below half of any container.

**12. Opaque badges read as paid.**
- **Why:** A badge with no visible eligibility rule gets assumed to be bought.
- **Apply:** Give every badge a one-tap "how this is decided".

**13. Labels in dense modules go unseen.**
- **Why:** Disclosure labels are easy to miss in a busy module. When users later learn what they missed, trust can drop sharply.
- **Apply:** Test whether a disclosure is noticed, not whether it is present (method card 7).

**14. Pushed items get more scrutiny.**
- **Why:** People check evidence harder on anything that looks promoted. Thin evidence amplifies doubt; strong evidence recovers trust.
- **Apply:** Show stronger evidence on anything you push, not weaker.

**15. All-positive curation looks like hiding.**
- **Why:** Praise-only blocks and best-score-only displays make users ask what was left out.
- **Apply:** Show the spread.

**16. Control beats explanation.**
- **Why:** An action ("hide this source", "customize") does more for trust than an explanation ("why am I seeing this"). Users expect an acknowledgment after giving feedback.
- **Apply:** Pair every disclosure with an action, and always confirm receipt.

## Navigation and labels

**17. A label names the object, the owner, and the destination.**
- **Why:** A bare label ("Store", "Hub") leaves users unsure whether they will leave the product or lose their place.
- **Apply:** Run an expectation test (method card 2) on any new entry point.

**18. Always show a way back.**
- **Why:** Without an explicit "back to X", a meaningful share of users struggle to return. Hidden menus on mobile often go unopened.
- **Apply:** Make the logo or name link home. Put a visible return on every detour.

**19. Consistent templates enable comparison.**
- **Why:** Users compare across tabs, and a shifting layout makes comparison a chore. Comparison views are valued even when sparse.
- **Apply:** Pin the current item and rotate the alternatives in a fixed grid.

## Attention and measurement

**20. Attention is not importance.**
- **Why:** The loudest element wins the first glance whether or not it helps the decision. A loud tag can win first clicks and still lower intent, while a decision-critical cue goes unnoticed.
- **Apply:** Measure first click and intent separately, and back emphasis with substance.

**21. High satisfaction can hide abandonment.**
- **Why:** Satisfaction is often asked only of the people who stayed. A surface can score high while few users both use it and prefer it.
- **Apply:** Report the usage × preference funnel next to CSAT (customer satisfaction score).

**22. Content type follows the risk of the decision.**
- **Why:** High-stakes decisions draw requests for richer media (video, zoom) and decision-specific data (unit price, fit, warranty, terms).
- **Apply:** List the information users need for each decision type before designing the screen.

**23. Effects accumulate quietly.**
- **Why:** A denser variant can show no immediate satisfaction drop and still become, months later, the thing users name as their reason for dissatisfaction.
- **Apply:** A flat short-term A/B test does not clear a change. Read long-run effects from a surveyed holdout.

## Inclusion
- Start by recognizing who is excluded. Design for the most complex needs first.
- Never personalize on sensitive identity attributes.
- Missing data is no excuse to skip inclusion work. Get direct input from the people affected, not from proxies.
- Accessibility means using the product with no added friction. Screen-reader and keyboard paths are part of the design, not of QA.
