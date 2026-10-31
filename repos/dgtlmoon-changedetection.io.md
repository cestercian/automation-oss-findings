# dgtlmoon/changedetection.io

- Stars: ~31k
- Evaluated: 2026-10-31 (midday run)
- Result: picked

## Contribution rules
CONTRIBUTING.md: "Contributing is always welcome", PR into `master`, every new feature needs a test, run pytest (e.g. `pytest changedetectionio/tests/test_notification.py`), and dependencies must be permissively licensed. Commit titles look like "Area - description".

## AI / agent policy
None stated. No ban and no disclosure.

## CLA / DCO
None.

## Merge patterns
Mostly the maintainer's own PRs plus dependabot, but outside PRs do get merged (about 6 of the last 60).

## Decision
PICKED #4619 (Markdown to HTML breaks with more than one notification URL: the shared requested_output_format was overwritten and apobj.notify() was called once after the loop). Fix: format per URL plus one Apprise instance per URL, with a regression test in changedetectionio/tests/unit/test_notification_markdown_per_url.py.
- Claim: https://github.com/dgtlmoon/changedetection.io/issues/4619#issuecomment-6540368659
- Fork created this run: cestercian/changedetection.io. The CloudAgent opened its PR on the fork (closed), and the upstream PR was opened with gh.
- PR: https://github.com/dgtlmoon/changedetection.io/pull/4641 (c0af6e58, verified)
