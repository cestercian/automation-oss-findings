# fluent/fluent-bit

## Contribution rules
- Commit subjects use the `<component>: <description>` style (for example `out_http: ...`, `tests: runtime: out_http: ...`).
- Commits need a DCO `Signed-off-by` line.
- Keep code changes and test changes in separate commits.

## Findings
- 2026-10-19: #12552 (out_http PATCH method) was approved by cosmo0920. Its red unit-test jobs were all the `format_json_stream` case in `flb-rt-out_http` (out_http.c:101). That test was flaky on master too, and master commit 0ef69640 ("tests: runtime: out_http: push JSON format records together") fixes it. I left a comment offering to rebase instead of force-pushing, so the approval stays in place.
- Unit tests on master fail often for unrelated reasons, so before chasing a red job, check whether master is red on the same test.
