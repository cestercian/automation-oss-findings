# vectordotdev/vector

- Stars: 22.7k
- Evaluated: 2026-10-18 (batch33)
- Result: picked

## Contribution rules
CONTRIBUTING.md: conventional titles with component scope (`fix(file source): ...`), changelog fragment in `changelog.d/<issue>_<name>.fix.md` ending with `authors: <gh user>`. PR template sections.

## AI / agent policy
AI_POLICY.md: AI use encouraged, you vouch for the PR, keep PRs scoped, human-written discussion. No disclosure requirement.

## CLA / DCO
CLA required (Datadog CLA bot).

## Claim norms
Comment on the issue.

## Tests / CI
`cargo test -p file-source` (13 tests, ~12 s once built). Full vector build is huge; keep tests in lib/file-source when possible.

## Decision
PICKED #26552 (`remove_after_secs` deletes files skipped by `ignore_older_secs` without reading them). Claim: https://github.com/vectordotdev/vector/issues/26552#issuecomment-6273181122. Also seen: #26644, #26565, #26564 (sink retry / disk buffer).

## Update 2026-10-25 (midday run)
- #26814 (IPv6 literal sent as TLS SNI) skipped: reporter says they fixed it downstream and can send PRs. Our #26739 still open.

## Update 2026-10-25 (evening run)
- AI_POLICY.md asks substantially agent-generated PRs to name the model in the commit or PR body. That counts as a disclosure requirement, so skip vector for new PRs. Existing #26739 stays open.

## Update 2026-10-28 (evening run)
- Re-checked: AI_POLICY requires naming the model/tool used in the PR, which amounts to AI disclosure. Skip.
