# Failure Log

Failure is logged deliberately, not hidden.

This log exists to make learning visible and prevent mythology. Systems that hide failures build false confidence. Systems that document failures build institutional memory.

---

## Entry Format

Each entry follows this structure:

- **Date:** When the failure was identified
- **What was attempted:** The goal or action taken
- **What failed or underperformed:** The specific outcome that didn't meet expectations
- **Why it failed:** Best understanding at the time of logging
- **What was learned:** Insight gained from the failure
- **What changed:** Concrete changes made as a result (if any)

---

## Entries

### 001 — Coordination Demo 001 Setup Friction

**Date:** January 2026

**What was attempted:** Run Coordination Demo 001 as a reference implementation to validate the end-to-end coordination loop.

**What failed or underperformed:** Initial setup was confusing. Contributors encountered tooling friction, unclear local environment requirements, and ambiguous setup instructions. Time was lost debugging environment issues rather than validating coordination.

**Why it failed:** Documentation assumed familiarity with the toolchain. Setup steps were written for the author, not for new contributors. The demo prioritised demonstrating coordination mechanics over ensuring the demo itself was easy to run.

**What was learned:** Coordination may be legible, but if tooling is fragile, contributors never reach the coordination layer. Tooling must be boring and robust. Setup friction is a filter that removes willing contributors before they can contribute.

**What changed:** Simplified demo expectations. Revised documentation to assume less prior knowledge. Accepted that reference implementations must prioritise ease of setup over feature completeness.

---

## Rules

- No blame. Entries describe what happened, not who is at fault.
- No spin. Entries are factual, not defensive or promotional.
- Anyone may propose an entry via GitHub Issue.
- CRG reviews and approves inclusion.
- Entries are permanent once logged.
