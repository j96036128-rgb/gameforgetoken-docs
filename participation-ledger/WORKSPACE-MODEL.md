# GameForge Developer Workspace Model

This document describes how developers and contributors work during Build Requests.

## Overview

GameForge uses a GitHub-first, zero-infrastructure model. All coordination happens through public repositories with manual review.

## Where Code Lives

- **Builder's own repository**: Builders maintain their own GitHub repos for game code
- **No code transfer**: GameForge does not host, fork, or take custody of builder code
- **Links only**: Build Requests reference external repos via URL

## How Contributors Submit Work

### For Playtesters / Reviewers

1. Access the builder's prototype (link provided in Build Request)
2. Complete feedback using the provided template
3. Submit feedback via:
   - GitHub Issue on the Build Request thread, OR
   - Pull Request adding feedback to a designated feedback file

### For Technical Contributors

1. Review scope defined in the Build Request
2. Submit work via Pull Request to the builder's repository (if applicable)
3. Reference the Build Request ID in all submissions

## How Reviews Happen

1. **CRG Review**: Core Review Group reviews all submissions
2. **Acceptance Criteria**: Evaluated against published contribution criteria
3. **Public Documentation**: Accepted contributions are recorded in the Participation Ledger
4. **Rejection Handling**: Rejected submissions receive brief public explanation

## How Outputs Link to the Participation Ledger

```
Build Request #001
    ↓
Contributor submits feedback (GitHub Issue/PR)
    ↓
CRG reviews and accepts
    ↓
Entry added to ledger.csv:
build_request_id,contributor,role,contribution_summary,date,status
BR-001,@username,playtester,Submitted structured feedback on prototype,2026-01-15,accepted
```

## Tooling

| Function | Tool | Cost |
|----------|------|------|
| Code hosting | GitHub (builder's repo) | Free |
| Feedback submission | GitHub Issues/PRs | Free |
| Contribution tracking | ledger.csv in this repo | Free |
| Communication | GitHub Discussions or X | Free |

## Constraints

- No paid infrastructure
- No custom platforms
- No token-gated access (pre-token phase)
- All activity publicly auditable

## For Builders

To submit a Build Request:
1. Ensure your prototype is accessible (public repo or shared link)
2. Contact GameForge via X (@gameforgetoken) or GitHub Issue
3. CRG will create a Build Request file if approved

## For Contributors

To participate:
1. Review open Build Requests in `/participation-ledger/`
2. Follow submission instructions in the specific Build Request
3. Your contribution will be reviewed and recorded if accepted
