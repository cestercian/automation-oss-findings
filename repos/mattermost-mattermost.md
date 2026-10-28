# mattermost/mattermost

- Stars: 39.4k
- Evaluated: 2026-10-21 (batch34)
- Result: PR for #39098 (RenderHTML panic on whitespace-only fenced code info)

## Contribution rules
PR template: Summary, Ticket Link (`Fixes: <url>`), Release Note block that must always be present (`NONE` if no user-facing change). AGENTS.md: remove template comments and drop sections that don't apply.

## AI / agent policy
No ban or disclosure requirement; AGENTS.md only gives formatting rules.

## CLA / DCO
Mattermost CLA required (bot comments on the PR). Yash may need to sign it.

## Claim norms
Claim comment first.

## Tests / CI
Huge monorepo; use a sparse clone of server/public for the shared/markdown package (`go test ./shared/markdown/`).

## Decision
OK TARGET for small server/public fixes, but expect the CLA step.

## Update 2026-10-28 (evening run)
- #39099 already claimed by tejaschavan724. Nothing else free and well scoped.
