# psf/black

- Stars: 38k
- Evaluated: 2026-11-24 (midday run)
- Result: picked

## Contribution rules
PRs to `main`. PR template checklist (preview style, CHANGES.md entry with PR number, tests, docs). Changelog entry needs the PR number, so add it in a second commit after the PR exists. pre-commit.ci runs prettier on CHANGES.md: wrap entries at 88 cols.

## AI / agent policy
No AI/LLM wording found in docs/contributing, .github, CONTRIBUTING. Fine.

## CLA / DCO
None.

## Tests / CI
`pip install -e . pytest pytest-xdist`, `pytest tests -n 4 --ignore=tests/test_blackd.py`. Two `*_diff_with_color` tests in tests/test_black.py fail on clean main in a no-tty env (pre-existing). Line-range cases live in tests/data/cases/line_ranges_*.py with a `# flags: --line-ranges=N-M` header; the output section after `# output` repeats the flags line.

## Decision
PICKED #5736 (`--line-ranges` INTERNAL ERROR on fmt: off body before else/except). Cause: `_str_with_standalone_comments` in src/black/ranges.py. PR #5738.
