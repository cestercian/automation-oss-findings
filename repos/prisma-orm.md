# prisma/orm (prisma/prisma)

- Stars: 40k+
- Evaluated: 2026-11-24 (midday run)
- Result: picked

## Contribution rules
Repo was renamed prisma/orm. `main` is Prisma 8 (new packages layout: `packages/1-framework`, `2-sql-family`, ...). Prisma 7 lives on the `v7` branch, which still has `packages/adapter-pg` etc. Target `main` for 8, `v7` for 7. Conventional-commit PR titles with a scope.

## AI / agent policy
CONTRIBUTING says they do not ask whether a PR was AI-assisted and ship a `contrib-pr` skill for agents. Fine to contribute.

## CLA / DCO
DCO: every commit needs `Signed-off-by` (DCO bot checks). PR template has Linked issue / Summary / Testing / Skill update / Checklist.

## Tests / CI
Needs Node >= 22.13 and pnpm 11. `pnpm install --frozen-lockfile --ignore-scripts --filter @prisma/adapter-pg...`, build `packages/debug` and `packages/driver-adapter-utils`, then `npx vitest run --project @prisma/adapter-pg <file>` from the repo root.

## Decision
PICKED #31196 (adapter-pg `connectToShadowDb` connected to the main DB when built from a connection string). Claim comment posted. Fix on `v7`: `withDatabase` helper rewrites the URL path. PR #31199. Only adapter-pg builds the shadow pool from a pool config.
Also seen: #31144 (rollback timeout, maintainers investigating, skip), #31182 (migration lock wait, not examined).
