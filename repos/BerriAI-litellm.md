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
