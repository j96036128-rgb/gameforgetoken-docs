# Design Note 001 — Why We Avoid Automation

## Context

GameForge coordinates contributions through a manual review process. Build Requests are submitted by humans, evaluated by humans, and recorded by humans. This is slow. It does not scale elegantly. It requires sustained attention from a small group (currently one person).

Automation is technically feasible at nearly every step. We have chosen not to automate.

This note explains why.

---

## The Temptation

Automation promises:

- **Speed:** Instant acknowledgment, faster queues, no waiting for human availability
- **Consistency:** Same rules applied the same way every time
- **Scale:** Handle 10x the volume without 10x the effort
- **Reduced burden:** Free maintainers to focus on "higher-value" work

These are real benefits. We are not dismissing them.

The temptation is strongest when the queue grows, when reviews pile up, when a contributor waits longer than they should. In those moments, a bot that auto-acknowledges, auto-labels, or auto-triages looks like the obvious solution.

---

## The Tradeoff

Automation encodes assumptions. Once encoded, assumptions become invisible.

A rule that seemed reasonable when written ("reject contributions under 200 words") becomes policy without review. Edge cases that a human would catch ("this 180-word contribution is exceptional") get rejected silently. The system optimizes for throughput, not judgment.

More critically: automation shifts accountability. When a human rejects a contribution, they can be asked why. When a bot rejects a contribution, the answer is "it didn't meet the criteria." The criteria become the authority. The human who wrote the criteria is no longer present in the decision.

GameForge is an experiment in whether human judgment can remain central to coordination at scale. Automating away judgment defeats the experiment.

---

## A Concrete Example

When we designed the Coordination Codex (BR-006), we faced a choice:

**Option A:** Automate contributor sequencing. When a Chain Contributor submits, a bot validates word count, posts the section to the next contributor's issue, and updates the status table.

**Option B:** Keep sequencing manual. A human (CRG member) reads the submission, validates it against acceptance criteria, posts it to the next contributor, and updates the status table.

We chose Option B.

**Why:**

- Word count is easy to automate. Quality is not.
- A bot cannot tell if a contribution "visibly connects to the previous section." A human can.
- If we automate validation, contributors will optimize for passing automated checks, not for genuine contribution.
- The manual step forces the CRG to actually read every submission. This is the point.

The cost is that sequencing takes hours or days instead of seconds. The benefit is that every accepted contribution has been read and judged by a human.

---

## What This Costs Us

1. **Speed:** Contributors wait longer for responses.
2. **Scalability:** CRG capacity is the bottleneck. More Build Requests require more human hours.
3. **Consistency:** Different CRG members may evaluate differently. Calibration is ongoing, not guaranteed.
4. **Contributor frustration:** Waiting is unpleasant. Some contributors will leave.
5. **Maintainer burden:** Every review is work. Burnout is a real risk.

These costs are not hypothetical. They are current and ongoing.

---

## What This Buys Us

1. **Legibility:** Every decision has a human who made it. Accountability is traceable.
2. **Adaptability:** Edge cases are handled as they arise, not pre-encoded.
3. **Trust signal:** Contributors know their work is seen by a person, not filtered by a script.
4. **Learning:** CRG members develop judgment through practice. This judgment is the product.
5. **Failure visibility:** When the system fails (slow reviews, missed contributions), the failure is visible and attributable. Automated failures are silent.

---

## Known Failure Modes

This approach fails when:

1. **CRG capacity is exceeded.** If submissions outpace review bandwidth, the queue grows indefinitely. Contributors abandon the process.

2. **CRG judgment diverges.** Without calibration, different reviewers apply different standards. Contributors experience inconsistency as unfairness.

3. **Maintainer burnout.** Manual review is labor. Sustained labor without support leads to abandonment.

4. **Quality theater.** Manual review becomes rubber-stamping. The form persists but the judgment disappears.

We do not have solutions to all of these. We have mitigations:

- Explicit acceptance criteria reduce judgment variance
- Public documentation of decisions enables calibration
- Rate-limiting Build Requests controls inflow
- Acknowledging burnout as a design constraint, not a personal failure

---

## Open Questions

1. **At what volume does manual review become unsustainable?** We do not know. We have not reached it.

2. **Can CRG judgment be preserved while delegating volume?** Possibly. But delegation introduces the same encoding problem as automation.

3. **Is "human in the loop" sufficient, or must humans be central?** A human who rubber-stamps automated recommendations is not exercising judgment. Where is the line?

4. **What if contributors prefer speed over judgment?** Some will. GameForge may not be for them. Is that acceptable?

5. **Does this approach select for patient contributors, or just exclude impatient ones?** We do not know if patience correlates with contribution quality.

---

This note documents a current design choice, not a permanent doctrine. The choice may be wrong. If it is, the failure will be visible and documented.

That visibility is the point.

---

## Disclosure

Some documentation and scaffolding commits are produced with AI assistance under explicit human direction. All coordination decisions, reviews, and ledger entries are human-made.
