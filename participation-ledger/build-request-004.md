# Build Request #004 — External Contributor Onboarding

**Status:** Open
**Type:** UI/UX Improvement
**Date Opened:** 2026-01-16
**Builder:** GameForge Core (Reference Build)

---

## Summary

Validate that an external (non-maintainer) contributor can successfully participate in the GameForge coordination protocol by completing a small, well-defined improvement to Coordination Demo 001.

---

## Purpose

This Build Request is designed specifically for first-time external contributors. Its primary goal is to validate that:

1. The contribution process is understandable to newcomers
2. Submission and evaluation workflows function correctly
3. External contributors can be successfully onboarded and attributed

The improvement itself is secondary to validating the coordination process.

---

## Context

Coordination Demo 001 is a minimal click-to-collect game used as a reference implementation for the GameForge protocol.

**Demo Repository:** https://github.com/j96036128-rgb/coordination-demo-001

**How to Play:** Open `game/index.html` in a browser. Click falling objects to collect them before time runs out.

---

## Request

We are seeking a small UI improvement to the demo. Choose one of the following:

### Option A: Visual Feedback Enhancement

Add a brief visual indicator when an object is successfully collected (e.g., a small "+1" that fades out, or a subtle screen flash).

### Option B: Instructions Clarity

Improve the start screen instructions to make the objective clearer for first-time players.

### Option C: End Screen Enhancement

Add the player's collection rate (objects collected / objects spawned) to the end screen.

---

## Acceptance Criteria

A valid contribution must:

1. Address one of the three options above
2. Be submitted as a working code change (HTML/CSS/JS)
3. Not break existing functionality
4. Be minimal and focused (no scope creep)
5. Include a brief description of what was changed and why

---

## How to Submit

1. Fork the [coordination-demo-001](https://github.com/j96036128-rgb/coordination-demo-001) repository
2. Implement your chosen improvement
3. Test that the game still works correctly
4. Open a GitHub Issue in [gameforgetoken-docs](https://github.com/j96036128-rgb/gameforgetoken-docs/issues) with:
   - Title: `[BR-004] Contribution Submission — @your-github-handle`
   - Link to your forked repository with the changes
   - Description of what you changed
   - Which option (A, B, or C) you addressed

---

## Constraints

- No financial reward
- No guaranteed token allocation
- Contribution must be original work
- Attribution recorded in participation ledger if accepted

---

## Evaluation

Contributions will be evaluated on:

1. **Relevance**: Does it address the stated scope?
2. **Completeness**: Does it work as intended?
3. **Quality**: Is the code clean and maintainable?
4. **Clarity**: Is the change well-documented?

See: [Evaluation Criteria](../protocol/EVALUATION-CRITERIA.md) (if available)

---

## Success Criteria

This Build Request is successful if:

- At least one external contributor submits a valid contribution
- The contribution is evaluated and recorded in the ledger
- The contributor confirms the process was understandable

---

## Contribution Log

| ID | Contributor | Role | Summary | Date | Status |
|----|-------------|------|---------|------|--------|
| — | — | — | — | — | — |

---

*This Build Request validates external contributor onboarding, not the demo itself.*
