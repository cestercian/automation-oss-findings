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

## Update 2026-10-25 (evening run)
- Recent issues already have PRs.

## Update 2026-10-27 (evening run)
- #10186: reporter already has a fix in progress. Skipped.
## Update 2026-11-19 (evening run)
- PICKED #10362 (bisync + --name-transform deletes/renames Path1 files on the second run). Reproduced on master with a local build before claiming. Claim proposed "refuse the flag" (docs only list copy/sync/move): https://github.com/rclone/rclone/issues/10362#issuecomment-7013280361 . Agent bc-47291eb7 (grok-4.7 high). Opened #10391 (5ae56ed2 verified): applyContext errors on transform.Transforming(ctx), docs note in bisync.md + docs.md, unit test. TestRcBackupDir flakes on master too.
- PR template checklist has an "If I used AI tools" ownership box (no disclosure ban). Bisync PRs from Aug/Sep are still unmerged, so expect a slow review. #10315 (vfs zero-size cache) has ihsandeniz asking ncw for approach: skip.

## Update 2026-11-20 (midday run)
- #10391: test used os.Stat on a lowercase name, which passes on macOS/Windows case-insensitive FS. Fixed in d2384ba7 by comparing exact ReadDir names. Fork PR CI needs maintainer approval (action_required).

## Update 2026-11-25 (midday run)
- #10424 (RemoteStats data race) is already fixed on master by #10330; skip.
- PICKED #10422 (crypt Object.Size returns 0 when the underlying size is -1). Claim: https://github.com/rclone/rclone/issues/10422#issuecomment-7155549120 . Agent bc-2425e5ee (grok-4.7 high). PR #10453, head c55243b3 (verified). Passes negative sizes through like ObjectInfo.Size; TestObjectSizeUnknown fails on master (actual 0).
- Agent's `gh pr create` got "Resource not accessible by integration", but the upstream PR still appeared (opened under cestercian at 07:18Z). Check for an existing PR before opening one manually.
- #10391 linux_386 red is TestInternalMaxChunkSizeRespected in backend/cache, unrelated to the bisync change.
- #10420 (track-renames ignores compare-dest) is still free as of this run.
