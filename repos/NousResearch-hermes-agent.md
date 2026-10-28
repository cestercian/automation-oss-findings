# NousResearch/hermes-agent

- Stars: 254k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
CONTRIBUTING.md + many AGENTS.md files.

## AI / agent policy
No ban found.

## CLA / DCO
-

## Claim norms
Per-author PR limit.

## Tests / CI
pytest.

## Decision
SKIPPED: PR creation reported restricted for outside accounts; per-author PR caps.

## Update 2026-10-25 (evening run)
- The earlier skip turned out wrong: outside PRs do go through (cestercian already has #133584, #123116, #123108 open). There's no AI disclosure rule, and AGENTS.md is agent-friendly.
- Picked #144518 (the TUI config health probe warns about every top-level null key, including `max_concurrent_sessions: null`, which is a documented default). Claim: https://github.com/NousResearch/hermes-agent/issues/144518#issuecomment-6399484903
- Gotchas: `python scripts/check` is a code-health ratchet that blocks in CI. It sets complexity/size caps per function and file, and files over 2000 lines can't grow, so put new tests in a new test file. CloudAgent can't launch on the upstream repo ("not accessible"), so launch on the cestercian fork and branch from upstream/main.

## Update 2026-10-27 (midday run)
- #145412 (standalone Telegram send ignores HERMES_TELEGRAM_HTTP_*) already has several older PRs (#63116, #77315, #125409). #145387 tracked by maintainer in #134889. Search PRs by keyword, not just issue number, since hermes PRs rarely link issues.

## Update 2026-10-27 (evening run)
- #145530 and #145564 are tracked in-house under #134889. Skipped.
## Update 2026-10-28 (evening run)
- Issue tracker swarmed; issues are tracked in-house under #134889. Nothing taken.
