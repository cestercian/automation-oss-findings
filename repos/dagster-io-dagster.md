# dagster-io/dagster

- Stars: 16.3k
- Evaluated: 2026-10-18 (batch31)
- Result: picked (batch36)

## Contribution rules
CLAUDE.md, libraries CONTRIBUTING.

## AI / agent policy
No ban found.

## CLA / DCO
No CLA.

## Claim norms
-

## Tests / CI
pytest.

## Decision
SKIPPED: #34312 author offered a PR, #34301 has PR #34303, #34080 needs a design decision.

## Batch32 update (2026-10-18)
Batch32: #34310 is Dagster+ specific; rest feature requests.

## Batch36 update (2026-10-23)
PICKED #27379 (dagster-user-deployments envSecrets optional: true dropped in includeConfigInLaunchedRuns: _helpers.tpl only forwards names into env_secrets). No CLA, no AI ban; contributing.md welcomes bugfixes. PR template: Summary & Motivation / Test Plan / Changelog. Must run `just ruff`; helm tests in helm/dagster/schema (pytest + helm binary). Claim: https://github.com/dagster-io/dagster/issues/27379#issuecomment-6359577836. Fork cestercian/dagster created this batch (CloudAgent needs the fork URL, upstream URL is not accessible).
PR: https://github.com/dagster-io/dagster/pull/34341 (commit 75abf3c, verified). CloudAgent createPullRequest upstream fails with "Resource not accessible by integration" (it opened a same-repo PR on the fork instead, closed); open upstream PR from box with gh. CI gotcha: buildkite/unit-tests shows FAILURE on every external fork PR because the build sits in "blocked" until a maintainer unblocks it. Not a real failure. Greptile auto-reviews.
