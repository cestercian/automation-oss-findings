# vitest-dev/vitest

- Stars: 17.3k
- Evaluated: 2026-10-18 (batch33)
- Result: picked

## Contribution rules
CONTRIBUTING.md: conventional commit titles, PR template with Description and `Fixes #`.

## AI / agent policy
AI_POLICY: write in your own voice, no disclosure required; fully automated PRs get closed.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
pnpm 12, `pnpm install --frozen-lockfile && pnpm build`, then `cd test/e2e && pnpm vitest run test/<file>`. Rebuild `packages/vitest` after source changes (e2e uses dist). oxlint + oxfmt.

## Decision
PICKED #11646 (`--exclude` not applied to inline projects; root config pushed into `configDefaults.exclude`). Claim: https://github.com/vitest-dev/vitest/issues/11646#issuecomment-6272675478. Also seen: #11636 (browser tester load waits out the 60 s timeout).
