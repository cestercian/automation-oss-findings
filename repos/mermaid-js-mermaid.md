# mermaid-js/mermaid

- Stars: 90.7k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
CONTRIBUTING.md, PRs to `develop`.

## AI / agent policy
No ban found.

## CLA / DCO
-

## Claim norms
-

## Tests / CI
pnpm test.

## Decision
SKIPPED: #7564 and #7047 already fixed; newer issues are triage/feature requests.

## Update 2026-10-24 (batch38)
- No AI policy, no approved-label gate; outsiders do get merged (Yun-seoung, jackroberts236, SwastikTripathi) but the open PR backlog is huge and our #8396 has had no review since Oct 6.
- Picked #8540/#8544/#8545 (entity placeholder leaking into pie/radar/venn error messages, same root cause). Claimed all three on 2026-10-24.
- Needs a .changeset entry. PRs target develop. Fork develop can't be synced from the box (token lacks workflow scope), branch from upstream/develop instead.
- PR: https://github.com/mermaid-js/mermaid/pull/8549 (opened 2026-10-24).

## Update 2026-10-24 evening (batch39)
- #8549: addressed CodeRabbit decode comment (placeholder-only decode was already in 3e50ce18e; added mixed-label tests in 39d5f59, verified). Replied on the thread. e2e-required still the 'run pr tests' label gate.
