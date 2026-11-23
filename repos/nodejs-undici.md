# nodejs/undici

- Stars: 7.7k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
CONTRIBUTING.md, DCO-style certificate.

## AI / agent policy
No ban found.

## CLA / DCO
DCO.

## Claim norms
-

## Tests / CI
npm test.

## Decision
SKIPPED: under 10k stars; #5963 has PR #5964.

## Update 2026-10-24 (batch38)
- #6075 has mcollina's backport PR #6076; #6064 has PR #6065. No free issues.

## Update 2026-10-26 (evening run)
- Opened #6094 (fixes #6092): extractBody re-enqueued string/byte bodies on every pull before the deferred queueMicrotask close. Fix is a once-only flag plus test/fetch/issue-6092.js. DCO sign-off included.
- test/fetch/cookies.js (HTTP/2 TLS) fails locally on main too, so ignore it.
- Skipped #6082, #6060, #6054: they already have PRs.

## Update 2026-11-02 (evening run)
- Every fresh issue already has a PR: #6123, #6135, #6112, #6115, #6110, #6106. Nothing picked.

## Update 2026-11-21 (evening run)
- Every fresh bug (#6184, #6144, #6082, #6202 and others) already has open PRs. Nothing picked.

## Update 2026-11-23 (evening run)
- Claimed #6246 (WebSocket messages in one chunk dispatched in same task) and opened #6248 (Fixes #6246). Fix: first message immediate, later buffered ones via setImmediate; close frame applied after message tasks (chained setImmediate turns clean close into 1006). Test: test/websocket/issue-6246.js. Lint: npm run lint. Tests: npm run test:websocket (borp). DCO sign-off required (-s).
- Fork main was 129 commits behind: branch from upstream/main. Local HTTP/2 handshake tests fail with timeouts, ignore.
