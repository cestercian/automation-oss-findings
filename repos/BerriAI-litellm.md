# BerriAI/litellm

- Stars: 61.5k
- Evaluated: 2026-10-18 (batch32)
- Result: picked

## Contribution rules
CONTRIBUTING.md: sign the CLA first, Conventional Commits, PR template with TLDR / User Flow (written for humans) sections.

## AI / agent policy
AI coding agents told to follow AGENTS.md and run `make format`. No ban, no disclosure requirement.

## CLA / DCO
CLA required (cla-assistant.io/BerriAI/litellm).

## Claim norms
Comment on the issue.

## Tests / CI
`UV_PROJECT_ENVIRONMENT=... uv sync --extra proxy --extra proxy-runtime --group dev --group proxy-dev` (prisma lives in proxy-dev), then `pytest tests/unit/proxy/db/test_check_migration.py tests/unit/litellm_proxy_extras/`. Files are not ruff-format clean upstream, only check your own lines.

## Decision
PICKED #47273 (DATABASE_URL with password passed in prisma migrate diff argv). Claim: https://github.com/BerriAI/litellm/issues/47273#issuecomment-6253067814. Lots of fresh security-ish bugs (#46913-#46917) also open.

## Update 2026-10-31 (midday run)
- PICKED #49311 (parent_otel_span hashed into the exact cache key when enable_caching_on_provider_specific_optional_params is true). Fix: declare parent_otel_span litellm-owned in litellm/types/litellm_params.py so `is_litellm_owned_kwarg()` drops it. Tests are under tests/unit/caching and tests/unit/types/test_litellm_params.py.
- Claim: https://github.com/BerriAI/litellm/issues/49311#issuecomment-6540353568
- PR: https://github.com/BerriAI/litellm/pull/49407 (c57a5b0f, verified). The CloudAgent opened its PR on the fork (cestercian/litellm#4, closed), so the upstream PR was opened from the box with gh and the body cleaned. The tests dir is now tests/unit/ (not tests/test_litellm/). #47276 (Oct 18) is still open and unreviewed.
