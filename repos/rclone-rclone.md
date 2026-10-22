# rclone/rclone

- Stars: 60.4k
- Evaluated: 2026-10-18 (batch32)
- Result: skipped

## Contribution rules
-

## AI / agent policy
-

## CLA / DCO
-

## Claim norms
-

## Tests / CI
-

## Decision
SKIPPED: backend-specific bugs needing accounts (internxt, drive).

## Batch35 update (2026-10-22)
CONTRIBUTING has an "AI-assisted contributions" section: AI is welcome, no disclosure needed, but you must understand every line, `go build` + `make quicktest` must pass, backend changes should be tested against a real remote, and trim verbose AI comments (see AGENTS.md commenting style). Skipped #10162 (iclouddrive case-only rename deletes items; backend should declare `CaseInsensitive`) because it can't be verified without an iCloud account.
