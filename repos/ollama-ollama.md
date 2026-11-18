# ollama/ollama

- Stars: 184k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
CONTRIBUTING.md + AGENTS.md.

## AI / agent policy
No ban found.

## CLA / DCO
-

## Claim norms
-

## Tests / CI
go test ./...

## Decision
SKIPPED: #18995 is an API design discussion; #19040 disputed; rest are GPU/model specific.

## Update 2026-10-27 (midday run)
- #19303/#19296 fixed by #19310 (merged). #19326 reporter wants discussion before a PR. #19313 is a library template blob, not repo code.

## Update 2026-10-27 (evening run)
- #19326 is still waiting on design discussion, no PR yet. Skipped.
## Update 2026-10-28 (evening run)
- #19342 already claimed by A-RYAN-1.

## Update 2026-11-02 (evening run)
- #19446 has PR #19447. #19457 (llama.cpp rope shift) is upstream in llama.cpp, and #19463 (hybrid-model VRAM prediction) is large. Skipped.

## Update 2026-11-18 (midday run)
- #18841 is superseded by upstream #18874 (531946e9, hide duplicate and downgrade guards from list, closed #18830). Not rebased. Left open per standing rule.
- PICKED #19751 (thinking box clips 10+ list markers: prose-sm ol padding 22px vs 22.6px marker, overflow-hidden wrapper). Claim: https://github.com/ollama/ollama/issues/19751#issuecomment-6971595581 . Agent bc-9d967412 (grok-4.7 high).
- Opened #19755 (947da2d9, verified) with box gh after agent create 403. Fix [&_ol]:ps-[5ch] in Thinking.tsx plus a vitest browser test. npm run lint has 112 pre-existing no-explicit-any errors and prettier:check fails on 6 existing files, not ours. App UI uses vitest --mode browser for *.browser.test.tsx.
