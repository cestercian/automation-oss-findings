# rolldown/rolldown

- Stars: 13.9k
- Evaluated: 2026-10-25 (evening run)
- Result: picked

## Contribution rules
AGENTS.md is agent-friendly and has internal-docs/ for context. It tells assistants to open PRs as drafts unless the user says otherwise.

## AI / agent policy
No ban and no disclosure requirement.

## CLA / DCO
None seen.

## Claim norms
Comment on the issue.

## Tests / CI
just + pnpm. Build the binding with `just build-rolldown`. Dev lazy tests are in packages/rolldown/tests/dev/dev-lazy-compile.test.ts, and Rust fixtures are in crates/rolldown/tests.

## Decision
PICKED #11273 (lazy dev mode wraps plugin-resolved externals in a `?rolldown-lazy=1` proxy). The cause is in crates/rolldown_plugin_lazy_compilation/src/lazy_compilation_plugin.rs: resolve_id never checks whether the `ctx.resolve` result is external. Claim: https://github.com/rolldown/rolldown/issues/11273#issuecomment-6399532449
