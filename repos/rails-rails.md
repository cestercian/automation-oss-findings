# rails/rails

- Stars: 58.8k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
CONTRIBUTING.md + AGENTS.md.

## AI / agent policy
Agent guide only.

## CLA / DCO
-

## Claim norms
-

## Tests / CI
bin/test.

## Decision
SKIPPED: Ractor issues need Ruby 4.0; #58990 claimed by Kutomore.

## Batch32 update (2026-10-18)
Batch32: #59055 is about the website; #58990 claimed; #59153 Ractor related.

## Update 2026-10-24 (batch38)
- #59215 has PRs #59216 and #59314. Ractor issues (#59173, #59153, #59152, #59168) owned by Kutomore/mhenrixon with PRs.

## Update 2026-10-25 (midday run)
- #59215 (filtered_path ignores dotted filter_parameters) skipped: reporter dhruv-techdev already has a PR up asking for review.

## Update 2026-10-27 (midday run)
- #59359, #59146, #59136, #59193 all have PRs (reporters usually open their own).

## Update 2026-10-29 (midday run)
- Opened #59418 (fixes #59412): routing `format: :json` Symbol was silently ignored by `Mapping#normalize_format` (regressed in 4.0). Fix is `when String, Symbol` with `to_s`, so the default stays a String. Signed commit 3ad0df5. Claim comment posted first. Reporter asked if it was intentional and no maintainer has answered yet, so it might be closed as wontfix.
- The CloudAgent gh token can't create upstream PRs (Resource not accessible by integration). Opened it locally with gh as cestercian instead.

## Update 2026-11-02 (evening run)
- #59480, #59517, #59457, #59439 and #59419 all have cross-referenced PRs. Nothing picked.

## Update 2026-11-03 (midday run)
- PICKED #59540 (nested reconnect! -> SystemStackError when the server drops the first query during configure_connection, e.g. PgDog). Claim: https://github.com/rails/rails/issues/59540#issuecomment-6597480553 . Agent bc-8a4b8d75 (grok-4.7 high).
- Fix: attempt_configure_connection sets @configuring_connection, reconnect_can_restore_state? returns false while set, so the outer reconnect! keeps its own budget. Opened #59567 (9aa53a8e, verified) with box gh after agent 403. adapter_test passed on sqlite3, postgresql, mysql2, trilogy.
- #59545/#59546 are security-design reports (CSRF, signed cookies); not for drive-by PRs.
