# mswjs/msw (~18k stars)

## AI policy
None in CONTRIBUTING.md, no AGENTS.md, no PR template AI checkbox.

## CLA / DCO
None.

## Claim norms
Comment on the issue. Outside PRs do get merged (Andarist, felmonon, AndyMJones etc. in 2026); kettanaito merges. Very few open PRs, so review load is low.

## Tests / CI
pnpm, vitest (unit), playwright (browser). Conventional commits.

## Decision
PICKED #2827 -> branch fix/worker-update-rejection, e64aa78f (verified). Upstream PR creation 403d for both the agent and box gh ("does not have the correct permissions to execute CreatePullRequest"), likely an interaction limit for new contributors. Compare: https://github.com/mswjs/msw/compare/main...cestercian:msw:fix/worker-update-rejection . Agent also opened a stray fork PR cestercian/msw#1. Original pick: #2827 (Firefox unhandled InvalidStateError from background existingRegistration.update() in src/browser/utils/get-worker-instance.ts). Claim: https://github.com/mswjs/msw/issues/2827#issuecomment-6545122847
