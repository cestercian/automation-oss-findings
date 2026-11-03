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

## Update 2026-11-02 (evening run)
- #4165 was closed earlier; #4163 still open (base dev). Maintainers now target `four-dev` for 4.x source PRs (e.g. #4177); PR template says run `npm run test`, no AI clause.
- #4173 and #4180 are assigned to 1cg; skip.
- PICKED #4182 (parseHTMLUnsafe(trusted, {}) throws in Chrome 124-145, fall back like #4085). Claim: https://github.com/bigskysoftware/htmx/issues/4182#issuecomment-6580488778 . Agent bc-f0391627, base four-dev.
- #4183 (lazy history stamp aborts hx-browser-indicator) and #4184 (morph drops typed text after blur) are free backups from tFo-DE, both 4.0.1 regressions.
- Opened #4186 (208f19ca, verified) with box gh because the agent's upstream create got "Resource not accessible by integration". CI passed: htmx_tests, website_tests, content. The agent's stray fork PR cestercian/htmx#2 is already closed.

## Update 2026-11-03 (midday run)
- PICKED #4183 (lazy history stamp from #4067 calls replaceState during hx-browser-indicator's pending navigation and aborts the request). Claim: https://github.com/bigskysoftware/htmx/issues/4183#issuecomment-6597481240 . Agent bc-49e5b410 (grok-4.7 high).
- Opened #4192 (13dd5672, verified, base four-dev) with box gh; agent create got "Resource not accessible by integration" again. npm test 1853 passed.
- We now have 3 open in htmx (#4163, #4186, #4192): hold new htmx PRs until one lands. #4184 (morph drops typed text after blur) is still a free backup.
