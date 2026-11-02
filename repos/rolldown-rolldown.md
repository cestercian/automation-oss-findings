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

## Update 2026-10-28 (evening run)
- #11325/#11330 untriaged, experimental area, possibly team-fixed. Not taken.

## Update 2026-10-31 (evening run)
- PICKED #11400 (preserveModules strips non-JS extensions like .vue/.css from [name]; should match Rollup's NON_ASSET_EXTENSIONS handling in getPreserveModulesChunkNameFromModule). Claim: https://github.com/rolldown/rolldown/issues/11400#issuecomment-6545100474
- Opened rolldown/rolldown#11410 (863e8c28, verified) via box gh after the agent integration 403d.
- AGENTS.md suggests draft PRs unless told otherwise; no AI ban/disclosure.

## Update 2026-11-01 (midday + evening runs)
- #11410 (fixes #11400) MERGED ~12:04 AM IST Nov 1.
- PICKED #11330 (getModuleInfo / this.resolve report moduleSideEffects null instead of the effective value). Agent PR create 403d again; opened https://github.com/rolldown/rolldown/pull/11422 via box gh (8fd1bd8e, verified).
- By the evening #11422 conflicted with main (packages/rolldown/src/plugin/plugin-context-data.ts, branch 60+ behind) and only the Socket checks ran. Rolldown CI does not run on conflicting PRs, so rebase promptly when main moves fast. A rebase agent was launched.

## Update 2026-11-02 (evening run)
- #11295: hyfdev asked for wording that covers every external ctx.resolve result plus an import('node:fs') test with platform 'node'. Pushed 19fbb69 (verified) and replied.
- #11417 and #11397 are assigned to IWANABETHATGUY with PRs. #11447 was filed by sxzzbot (maintainer side), so leave it. Holding new rolldown PRs while #11295 and #11422 are open.
