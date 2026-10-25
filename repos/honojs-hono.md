# honojs/hono

- Stars: 32.6k
- Evaluated: 2026-10-21 (batch34)
- Result: no PR possible; fix linked as a branch on #5572 (https://github.com/honojs/hono/issues/5572#issuecomment-6310622332)

## Contribution rules
docs/CONTRIBUTING.md: "Pull requests are limited to maintainers." The repo has `pull_request_creation_policy: collaborators_only`, so `gh pr create` fails with a CreatePullRequest permission error. Outsiders file issues and may link a fork branch; a maintainer may open a PR from it and keep your commits.

## AI / agent policy
AI allowed, but a maintainer may close and block any account that wastes their time.

## CLA / DCO
None.

## Claim norms
Not applicable (no outside PRs).

## Tests / CI
pnpm + Bun, needs Node 22+ (pnpm fails on node 20). Run root `pnpm run build` before the adapter tests in adapters/*. Lint via `vp check`.

## Decision
SKIP for PRs. Check `gh api repos/<r> --jq .pull_request_creation_policy` before claiming on any repo.

## Update 2026-10-25 (evening run)
- Recent bugs already have fork fixes by other people.
