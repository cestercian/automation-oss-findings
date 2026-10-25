# oxc-project/oxc

- Stars: 23.1k
- Evaluated: 2026-10-18 (batch33)
- Result: picked

## Contribution rules
CONTRIBUTING.md + many per-crate AGENTS.md. Conventional commit titles with crate scope, e.g. `fix(mangler): ...`.

## AI / agent policy
Agent guides only. No ban, no disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
`cargo test -p oxc_minifier --test mod` (mangler tests live in crates/oxc_minifier/tests/mangler). Note `SourceType::mjs().with_unambiguous(true)` without import/export counts as CommonJS. rustfmt edition 2024.

## Decision
PICKED #27964 (top-level `var exports` / `var require` renamed in CommonJS). Claim: https://github.com/oxc-project/oxc/issues/27964#issuecomment-6273014695.

## Update 2026-10-25 (evening run)
- CONTRIBUTING and AGENTS.md now require AI disclosure. That's a hard skip under our rules.
