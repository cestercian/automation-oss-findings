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

## Update 2026-10-27 (midday run)
- The fresh Triage batch (#8535-#8574, mostly one reporter) all got PRs from others within a day (#8576, #8577, #8559-#8564, #8578...). Nothing free.

## Update 2026-10-29 (evening run)
- PICKED #8608 (flowchart HTML labels only wrap when the measured width is exactly `wrappingWidth`; sub-pixel or overflowing widths stay nowrap). Claim: https://github.com/mermaid-js/mermaid/issues/8608#issuecomment-6500574474. PR: https://github.com/mermaid-js/mermaid/pull/8609 (0.5px tolerance in addHtmlSpan + 5 unit tests + changeset). Commit c852008c verified.
- #8574 already has PR #8577.
- Tooling: needs Node 22.12+ (box has 20; Node 24 tarball in /tmp/node24 with COREPACK_HOME=/tmp/corepack). Fork develop is stale and can't be synced (workflow scope), so the agent branches from upstream/develop. CloudAgent couldn't open the upstream PR; opened via gh from the box.
