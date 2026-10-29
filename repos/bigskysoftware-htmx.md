# bigskysoftware/htmx

- Stars: 49.6k
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
SKIPPED: #4147 soft-claimed; #4006 maintainer says invalid.

## Batch35 update (2026-10-22)
#4151 (expired hx-preload blocks re-preloading) got pushback from maintainer MichaelWest22 (single preload with timeout is by design). Skipped.

## Update 2026-10-24 (batch38)
- #4155 already has PR #4156 by the reporter.

## Update 2026-10-24 evening (batch39)
- #4161/#4160 are feature discussions, #4151 still pushback. Skipped.

## Update 2026-10-25 (evening run)
- Midday run opened #4163 (fixes #4162). Verified, CI green.

## Update 2026-10-26 (evening run)
- Opened #4165 (fixes #4164) against four-dev: swap() ran the history update before htmx:before:swap, so a cancelled swap still changed the URL. htmx 4 work targets four-dev, and the fork four-dev is stale, so branch from upstream.
- npm test (web-test-runner) passes: 1804 passed, 4 skipped.

## Update 2026-10-29 (midday run)
- #4164 and #4162 are covered by our own open PRs (#4163, #4165). Don't add more until those land.

## Update 2026-10-29 (evening run)
- #4173 skipped: still a design question and our notes say hold off until #4163/#4165 land.
