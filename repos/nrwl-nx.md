# nrwl/nx

- Stars: 29.4k
- Evaluated: 2026-10-18 (batch32)
- Result: picked

## Contribution rules
CONTRIBUTING.md: commit format `type(scope): subject` with scopes from scripts/commitizen.js (e.g. `angular-rspack`). PR template: Current Behavior / Expected Behavior / Fixes #.

## AI / agent policy
AGENTS.md / CLAUDE.md are workflow notes for agents. No ban, no disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
pnpm 12 (install with `npm i -g --prefix /tmp/pnpm12 pnpm@12.4.2`, corepack layout breaks), `pnpm install --frozen-lockfile --ignore-scripts --filter '@nx/angular-rspack...' --filter @nx/nx-source`. Then in packages/angular-rspack: `NODE_OPTIONS=--conditions=@nx/nx-source npx vitest run`. Formatter is oxfmt (not prettier).

## Decision
PICKED #37468 (angular-rspack SSR engine manifest import dropped when sideEffects is set). Claim: https://github.com/nrwl/nx/issues/37468#issuecomment-6253166383. Also seen: a run of cache-correctness reports #37459-#37467 by one reporter (bigger design questions).
