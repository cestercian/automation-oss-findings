# homebridge/homebridge

- Stars: 25.5k
- Evaluated: 2026-10-18 (batch31)
- Result: picked

## Contribution rules
No CONTRIBUTING; CLAUDE.md + .github/copilot-instructions.md describe a label-driven beta branch strategy (bug fixes target the lowest open `beta-x.y.z` branch, currently `beta-2.4.1`). Outside PRs do get merged, but nothing has merged since 2026-08-30.

## AI / agent policy
No AI ban; CLAUDE.md present. No disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
Node 22+ required (eslint config breaks on Node 20). `npm test` (vitest, 1328 tests), `npm run lint`, `npm run build`.

## Decision
PICKED #4022 (Matter ColorControl commands fail when optional handlers are missing). Claim: https://github.com/homebridge/homebridge/issues/4022#issuecomment-6245865969. Skipped #4013-#4016 (design questions / API proposals).
