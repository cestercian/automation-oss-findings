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
