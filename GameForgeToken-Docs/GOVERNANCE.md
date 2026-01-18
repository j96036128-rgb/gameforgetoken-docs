# GameForge Governance

This document specifies who holds authority in the GameForge system, how that authority is constrained, and how decisions can be challenged.

---

## 1. Scope

This governance framework applies to:

- Build Request creation and prioritisation
- Contribution review and acceptance
- Participation ledger entries
- Coordination artifacts (Codex, demos, documentation)

This is a coordination governance system. It is not a corporate governance model, a token governance model, or a legal entity structure. Authority here pertains only to how work enters the system and how credit is recorded.

---

## 2. Roles and Authority

### Founder / Initial Maintainer

**Name:** Jon McMahon

**Responsibilities:**
- Bootstrapping the system
- Publishing initial Build Requests
- Acting as CRG member by default until the group is expanded

**Constraints:**
- Founder authority is bounded by the rules in this document
- All decisions must be recorded publicly in the participation ledger
- No off-ledger decisions carry authority
- The Founder is subject to the same recusal and conflict-of-interest rules as any CRG member

### Core Review Group (CRG)

**Role:**
- Evaluate contributions against published acceptance criteria
- Accept or reject work with written reasoning
- Maintain the participation ledger

**Composition:**
- Initially 1 member (Founder)
- May expand as Trusted Contributors emerge and are nominated
- CRG membership requires demonstrated review quality, not just contribution count

---

## 3. Build Request Creation

### Who May Create Build Requests

- Founder
- Trusted Contributors (see Section 5)

### Requirements for a Valid Build Request

Every Build Request must include:

1. **Clear scope:** What is being built and what is explicitly out of scope
2. **Acceptance criteria:** Specific, verifiable conditions for acceptance
3. **Submission method:** How to submit work (e.g., pull request, issue reference)
4. **Review expectations:** Estimated review timeline and who will review

### Publication Requirement

All Build Requests must be published publicly in the participation ledger before work begins. Unpublished requests do not exist for the purposes of contribution credit.

---

## 4. Contribution Review and Acceptance

### Review Process

The CRG reviews all submissions against the acceptance criteria specified in the corresponding Build Request.

### Outcomes

Every review concludes with one of three outcomes:

- **Accepted:** Work meets acceptance criteria. Ledger is updated.
- **Revision Requested:** Work does not yet meet criteria. Specific changes are documented.
- **Rejected:** Work does not meet criteria and revision is not appropriate. Reasoning is documented.

### Documentation Requirements

- Every decision must include written reasoning
- Reasoning must be public and attributable to the reviewing CRG member
- Ledger updates are mechanical reflections of decisions, not editorial interpretations

---

## 5. Trusted Contributor Status

### Threshold

A contributor achieves Trusted Contributor status after **3 accepted contributions**.

Contributions include:
- Accepted build work
- Accepted review work (when review is logged as a ledger contribution)

### Privileges

Trusted Contributors may:
- Propose Build Requests
- Participate in reviews (subject to CRG approval and conflict-of-interest rules)
- Participate in governance discussions
- Challenge decisions (see Section 6)

### Scope of Trust

Trust is role-scoped, not absolute. A Trusted Contributor with 5 frontend contributions does not automatically have authority over protocol design. Build Request proposals and review assignments should respect domain boundaries.

---

## 6. Challenges and Disputes

### What May Be Challenged

Any Trusted Contributor may challenge:
- A Build Request's prioritisation or scope
- A rejection decision
- A perceived violation of governance rules

### Challenge Process

1. The challenger opens a public GitHub Issue
2. The issue must reference specific criteria, rules, or reasoning being disputed
3. The issue must state what resolution is being requested

### Resolution

- The CRG responds publicly within a reasonable timeframe
- The response must address the specific points raised
- The CRG's decision is final but fully documented
- If the challenge reveals a governance gap, an amendment may be proposed (see Section 9)

---

## 7. Conflicts of Interest and Recusal

### Recusal Requirement

CRG members must recuse themselves from reviewing:
- Work they contributed to
- Work submitted by someone with whom they have a direct personal or financial relationship
- Any submission where impartiality cannot be reasonably maintained

### Disclosure Requirement

Any potential conflict of interest must be disclosed publicly before review begins. When in doubt, disclose.

### Handling Recusals

When a CRG member recuses themselves:
- Another CRG member reviews the work
- If no other CRG member is available, the review is deferred until one is

---

## 8. Transparency Commitment

- All governance decisions are public
- No off-ledger decisions carry authority
- The participation ledger is the source of truth for contribution credit
- Private communications may occur, but no credit or authority flows from them
- If it is not in the ledger, it did not happen

---

## 9. Amendments

### Process

Governance rules may evolve. Any change requires:

1. A public commit to this document
2. A clear rationale in the commit message explaining what changed and why
3. Public notice before the change takes effect (minimum 7 days for substantive changes)

### Constraints

- Amendments do not apply retroactively
- Contributions accepted under prior rules retain their status
- Amendments cannot revoke Trusted Contributor status already earned

---

## Related Documents

- [GOOD-PROBLEMS.md](GOOD-PROBLEMS.md) — Open questions in coordination design (advisory, not authoritative)

---

## Document History

- **Initial version:** Authored by Jon McMahon during system bootstrap
- **Amendments:** Tracked via git commit history
