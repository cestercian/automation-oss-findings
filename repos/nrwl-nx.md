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

## Batch35 update (2026-10-22)
Earlier PR #37471 (fix for #37468) MERGED 2026-10-18. PICKED #37427 (`nx release` pushes before commit/tag when `git.push` is true without `createRelease`; release.ts didn't pass `gitPush: false` to releaseVersion and only pushed later when a remote release was configured). Claim: https://github.com/nrwl/nx/issues/37427#issuecomment-6344102163. PR: https://github.com/nrwl/nx/pull/37568 (adds `--git-push` to the combined command and a new release.spec.ts).
Test notes: release tests now run with vitest (`pnpm exec vitest run src/command-line/release/release.spec.ts` in packages/nx). `utils/shared.spec.ts` fails without the native binding (`locateTouchedProjects is not a function`) when installed with `--ignore-scripts`; unrelated. Typecheck: `pnpm exec tsgo -p packages/nx/tsconfig.lib.json --noEmit` (`nx run nx:typecheck` needs dotnet for the project graph). Formatter: oxfmt.
Skipped #37506 (run exits 130 when tasks are skipped): reporter carries a local patch and offered to open a PR.
Upstream PR creation from the cloud agent app token 403s ("Resource not accessible by integration"); Cursor still auto-opened the PR, but with its own body, so fix the body to the template + `Fixes #N` afterwards.
