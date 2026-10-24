# pulumi/pulumi

- Stars: 25.8k
- Evaluated: 2026-10-18 (batch32)
- Result: picked

## Contribution rules
CONTRIBUTING.md + AGENTS.md (several per-package AGENTS.md). Changelog entry via `make changelog` (changie, `changelog/pending/*.yaml`). Squash merge, PR description becomes the commit message.

## AI / agent policy
AI-assisted contributions allowed; human must stay in the loop and include real test output. No disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
sdk/nodejs: Node 22, `npm ci --ignore-scripts`, then `npx mocha --timeout 300000 tests/provider/experimental/*.spec.ts` (the analyzer spec npm-links @pulumi/pulumi into testdata in a before hook, needs the long timeout; revert testdata/package.json after). `npx tsc --noEmit`, `npx biome check`.

## Decision
PICKED #25259 (single-member enums / `as const` objects in component args fail with Unsupported type). Claim: https://github.com/pulumi/pulumi/issues/25259#issuecomment-6252888419. Many recent issues are filed by staff from internal evals (policy CLI), mostly service-side.

## Batch35 update (2026-10-22)
Our #25273 (fix for #25259) MERGED 2026-10-18. Skipped #25235 (`policy group edit --add-stack` no-op) because staff have several open PRs rewriting policy pack/group commands (#25296 generated API types, #25297, #25333, #25334); the policy-CLI issues come from staff evals and are being handled in-house.

## Batch36 update (2026-10-23)
Skipped: staff-filed policy CLI issues (#25234-25237) handled in-house; #25215 reporter wants to fix it.

## Update 2026-10-24 evening (batch39)
- Opened #25381 (fixes #25358, Go programgen tuple of optional strings -> pulumi.Array, conformance test extended + snapshots regenerated, changie entry). Verified commit 77e0fca. CloudAgent could not create the upstream PR (Resource not accessible by integration); opened via gh from box. CI: maintainer-gated (/run-acceptance-tests), 3 checks pass.
- CloudAgents cannot launch on pulumi/pulumi directly (repo not accessible to integration); launch on cestercian/pulumi fork and branch from upstream/master. Fork sync via API fails (workflow scope).
