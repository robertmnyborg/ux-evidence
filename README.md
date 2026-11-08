# ux-evidence

A Claude Code skill that makes an agent ground UI and UX work in evidence before it writes UI code: who the user is, which one pain the screen solves, what must be true, and which number will tell you it worked or should be killed.

## Install

```bash
git clone <this repo> ux-evidence
cp -R ux-evidence/skills/* ~/.claude/skills/
```

Requirements: Claude Code. No scripts or hooks.

## Failure it prevents

An agent asked for a new screen goes straight to polished mocks. Nobody named the user, the pain, or the launch bar, so the design gets judged on looks, ships on a flat A/B test, and quietly erodes trust over the following months.

## How

- **Six gates, scaled to the stakes.** Customer + evidence, one ranked pain, a press-release paragraph with hard FAQs, an assumption map, a cognitive walkthrough, and a launch bar (success metric, perception guardrail, kill condition, rollback). A copy tweak gets no gates; a new flow gets all six. Thresholds must be numbers, labeled provisional when no baseline exists.
- **Method picker.** Ten research method cards (expectation test, hotspot perception survey, density ladder, holdout survey, and others), each with setup, starting sample size, what to measure, when not to use it, and a solo version for one builder plus an agent.
- **Design principles.** 23 checks on density, trust, provenance, navigation, and attention vs importance. Numeric thresholds are labeled starting assumptions to replace with your own data.
- **Measurement.** A perception and trust question bank, a quarterly tracker blueprint, experiment guardrails, and criteria a metric must meet before it goes on a dashboard.
- **Templates.** Research plan, design review, and findings report.

## Hand-offs

Optional companion skills, used if installed: `impeccable` (visual craft and critique), `trustworthy-insights`, `causal-claim`, and `job-card` (the last three from the author's analyst-rigor-skills repo).

## Credits

Builds on publicly documented methods: the Working Backwards press release and FAQ, the cognitive walkthrough (Wharton, Rieman, Lewis, Polson), story mapping (Jeff Patton), assumption mapping (David Bland), the value / usability / feasibility / viability risks (Marty Cagan), and Nielsen Norman Group usability guidance. The gates and checks are my own synthesis.

## License

MIT. See `LICENSE`.
