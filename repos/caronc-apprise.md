# caronc/apprise

- Stars: 17.6k
- Evaluated: 2026-10-18 (batch31)
- Result: picked

## Contribution rules
CONTRIBUTING.md: tests required for every plugin change, ruff for lint/format, PRs against `master`.

## AI / agent policy
No AI ban and no disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
`pytest` (full suite), `ruff check` and `ruff format --check`.

## Decision
PICKED #1803 (custom `from=` address lost in email URL round trips). Claim: https://github.com/caronc/apprise/issues/1803#issuecomment-6245522269. Full suite 3602 passed, ruff clean.

## Batch36 update (2026-10-23)
Skipped: only fresh bug #1828 (Pushover empty HTML) already has PR #1829 (theluckystrike). Nothing else free.

## Update 2026-10-28 (evening run)
- #1840 (AppriseTag hash/eq mismatch, filed today) looks design-ambiguous; reserve candidate, not taken.

## Update 2026-10-29 (evening run)
- #1841 already has PR #1842.

## Update 2026-11-18 (midday run)
- PICKED #1897 (MarkdownV2 spoiler ||x|| escaped when body_format is MARKDOWN). Claim: https://github.com/caronc/apprise/issues/1897#issuecomment-6971595288 . Agent bc-ebc4711e (grok-4.7 high).
- Opened #1899 (152d0103, verified). Full suite 4017 passed, tox -e lint clean. Agent upstream create got 'Resource not accessible by integration' but the PR still ended up opened as cestercian.
