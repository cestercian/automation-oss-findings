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
