# swc-project/swc

- Stars: 34.2k
- Evaluated: 2026-10-18 (batch33)
- Result: picked

## Contribution rules
CONTRIBUTING.md: PRs against main. `.changeset/*.md` entry per change.

## AI / agent policy
AGENTS.md / CLAUDE.md agent rules. No ban, no disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
`cargo test -p swc_ts_fast_strip` (fixture tests; `UPDATE=1` writes new expected .js/.transform.js).

## Decision
PICKED #12568 (ASI hazard when fast strip erases a class member). Claim: https://github.com/swc-project/swc/issues/12568#issuecomment-6273015682. Also seen: #12528, #12564, #12566 (minifier).
