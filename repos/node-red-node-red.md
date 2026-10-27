# node-red/node-red

- Stars: 23.7k
- Evaluated: 2026-10-18 (batch31)
- Result: picked

## Contribution rules
CONTRIBUTING.md: bug fixes go to `main`; features should be discussed on the forum first. PR template asks for a checklist and linked issue.

## AI / agent policy
No AI ban and no disclosure requirement.

## CLA / DCO
OpenJS Foundation CLA (bot prompts on the first PR).

## Claim norms
Comment on the issue; no formal assignment flow.

## Tests / CI
`npx mocha test/unit/@node-red/registry/lib/registry_spec.js` (full: `npm test` via grunt).

## Decision
PICKED #6010 (removeModule compared an array to 0, so modules used by others got removed). Claim: https://github.com/node-red/node-red/issues/6010#issuecomment-6245405638. Patch adds two registry tests, 150 passing.

## Outcome
PR #6017 opened 2026-10-18; EasyCLA check passed (CLA signed). Awaiting maintainer review.

## Update 2026-10-24 evening (batch39)
- #6014 (diff3 markers) is an AI-fished report; knolleary pushed back hard on AI-generated issues there. Avoid that reporter's issues. #6036 untriaged. Skipped.

## Update 2026-10-27 (midday run)
- #6031, #6007, #6013/#6012, #6008 all have outside PRs already. #6036 (projects history refresh) free but UI/git heavy and hard to test.
