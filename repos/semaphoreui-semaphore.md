# semaphoreui/semaphore

- Stars: 14.3k
- Evaluated: 2026-10-18 (batch31)
- Result: picked

## Contribution rules
CONTRIBUTING.md + a large AGENTS/ tree. PRs go to `develop`. Conventional-ish commit titles (`fix(db): ...`).

## AI / agent policy
AGENTS.md is written for agents; no ban and no disclosure requirement.

## CLA / DCO
No CLA, no DCO found.

## Claim norms
Comment on the issue.

## Tests / CI
`go test ./db/... ./services/tasks/...`. Note `./api` tests fail on a clean checkout without built web assets (`public/*` missing), pre-existing.

## Decision
PICKED #4286 (template params nested under `params`/`ansible` ignored by FillParams). Claim: https://github.com/semaphoreui/semaphore/issues/4286#issuecomment-6245644203. Also seen: #4310 claimed by its author.
