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

## Update 2026-11-23 (midday run)
- PICKED #4456 (remote runner never calls Kill() when GET /api/internal/runners reports a running task as `stopped`; `stopping` kills one poll late). Root cause: `checkNewJobs()` in services/runners/job_pool.go decides to kill from the OLD local status before `SetStatus(currJob.Status)`. Reproduced with an httptest unit test (LocalExecutor.IsKilled false for both statuses); fix = also kill when the server status is stopping/stopped and the local job isn't finished. `go test ./services/runners/` passes with it. Claim: https://github.com/semaphoreui/semaphore/issues/4456#issuecomment-7094366089 . Brief: /workspace/batch-2026-11-23-midday/semaphore-4456.md. Open related PR #3972 (app/cursor) touches the post-Run status path; keep clear of it.
- Our #4349 (params nested under params/ansible) still open since Oct; merges are mostly fiftin/souryogurt, outside merges rare.
- #4310 claimed by its author (has a branch). #4292 (secret survey var with remote runner) no repro detail. #4282 looks fixed in 2.20.23 per jpmens.
