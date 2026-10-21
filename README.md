# Network Fix Review

AI recommendations for network operations that an operator can question, correct and teach.

**Live prototype:** https://elizabethhannan.github.io/network-fix-review/

A self-initiated concept by [Elizabeth Hannan](https://elizabethhannan.github.io). The network, the model and every number are simulated so the interaction can be tested end to end. No real systems are changed, and nothing you do leaves your browser.

## What it shows

**Review.** A queue of AI-recommended fixes. Each one shows:

- **Why:** the evidence, charted against what is typical for that site
- **How sure:** the confidence, with that confidence level's track record (how often operators accepted and rolled back fixes like it)
- **What would change my mind:** the signal that would make the AI withdraw the recommendation
- **What changes:** the setting before and after, who is affected, and how to undo it

The operator can accept, edit or reject with a reason. Low-confidence, high-impact fixes default to investigating first. When nothing explains the data, the AI says it doesn't know and asks for more evidence. After a fix, the metric is watched and a one-step rollback stays open.

**What the model learns.** A model-feedback dashboard: decisions, accept/edit/reject and rollback rates, time to decide, a trailing 7-day trend against the previous period, rejection reasons, edited settings, results by fix type and by confidence band. Model-training requirements are written from those patterns, and your own decisions in the demo appear as training examples and telemetry events.

**Telemetry spec.** Operator goals mapped to what is measured and what it tells the model team, the event schema, and the patterns used on the page.

## Run it

Open `index.html` in a browser. It is one self-contained file: no build step, no dependencies beyond Google Fonts.

## Notes

- Every dashboard number is computed from one seeded set of simulated decisions plus your own, so the tiles, chart, lists and requirements always agree.
- Keyboard: tabs move with the arrow keys; charts take focus and step with the arrow keys; Escape closes an open panel.
- Light and dark themes follow the system setting.

Built with HXO. HXO (Human Experience Optimization) is a design methodology that starts from human outcomes, not features, technology or business requirements, and tests every system with one question: does it help or hurt the full spectrum of human experience?
