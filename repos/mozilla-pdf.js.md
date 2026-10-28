# mozilla/pdf.js

- Stars: ~50k
- Evaluated: 2026-10-28 (evening run)
- Result: PR opened https://github.com/mozilla/pdf.js/pull/22362 (fixes #22341). Older PR #22083 still open.
- Contribution rules: .github/CONTRIBUTING.md is about issue reporting; AGENTS.md lists commands only, no AI ban. pull_request_creation_policy is "all".
- AI/agent policy: no ban or disclosure requirement found.
- CLA/DCO: none.
- Claim norms: reporters often offer PRs and maintainers say go ahead (#22300 went to the reporter, PR #22347). Check comments before claiming.
- Tests/CI: `npx gulp lint` (needs NODE_OPTIONS=--max-old-space-size=4096 on small VMs), `npx gulp unittestcli`, integration via `TESTING=true` build then `INTEGRATION_FILTER=... INTEGRATION_SPECS=freetext_editor_spec.mjs node test/test.mjs --integration --noDownload --headless --noFirefox`.
- Commit/PR title style: plain imperative sentence, often with "(issue N)" suffix, no conventional prefix.
- Decision: good target for small, well-diagnosed editor bugs.
