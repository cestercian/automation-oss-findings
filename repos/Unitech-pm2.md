# Unitech/pm2

- Stars: 43.3k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
CONTRIBUTING.md.

## AI / agent policy
No ban found.

## CLA / DCO
-

## Claim norms
-

## Tests / CI
npm test.

## Decision
SKIPPED: #6148 has PR #6149.

## Batch32 update (2026-10-18)
Batch32: #6171 is a complex watch-restart race ("Callback was already called").

## Update 2026-10-24 (batch38)
- #6173 (pidusage) already fixed on master: package.json pins pidusage 4.1.0. Nothing to do.

## Update 2026-10-25 (evening run)
- Midday run opened #6177 (fixes #6176). CLA check passed, verified, CI green.

## Update 2026-10-29 (evening run)
- #6173 (Windows memory null, bump pidusage) is already fixed on master (pidusage 4.1.0). #6175 is just Docker base image CVE bumps. Nothing taken.

## Update 2026-11-03 (evening run)
- #6179 (fixes #6178) got a full Unitech review: fix confirmed (reproduced, Docker suite 184/184). Asks: base `development` (not master), guard the whole vizion/finalizeProcedure block when stopping, fixture handlers before 'booted', assert restart cb count, fork-mode case, a test that fails if the handleExit change is reverted, wire into test/unit.sh after cluster_log_lifecycle, `# Excluded:` comment in test/windows.sh. Maintainers add CHANGELOG lines themselves.
- Retargeted #6179 to development (gh pr edit) and posted a short ack. All changes are done and tested on the box (6/6 passing x3, cluster_log_lifecycle/reload-locker/graceful/cluster green; mutation checks: original God.js fails 4/6, reverted handleExit fails 4/6, readyCb-without-cb fails the restart cases). NOT pushed: Cloud Agent launches blocked (Cursor usage used up) and the box has no GPG key, so no signed commit possible. Patch: /workspace/pm2-6179-patch/0001-*.patch on top of the rebased branch (/workspace/pm2-work, branch fix/late-ready-during-stop rebased onto upstream/development, original commit needs re-signing too). Next: Cloud Agent applies patch, signs both commits, force-pushes.
- Repo rule: PR base is `development`, not the default `master`.
