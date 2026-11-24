# ChromeDevTools/chrome-devtools-mcp

- Stars: 59k
- Evaluated: 2026-11-24 evening
- Result: picked #3601

## Contribution rules
PRs to `main`, conventional commit titles (release-please). AGENTS.md: use only package.json scripts, update BUILD.gn when adding files, never use any/as/!.

## AI / agent policy
None stated.

## CLA / DCO
Google CLA bot (tied to the commit email; our earlier Google PRs used yashafaid@gmail.com, so use that as the commit author, not the noreply address). No DCO.

## Tests / CI
Needs Node >= 22.18 (node 20 and 22.14 cannot run scripts/*.ts). Setup: `npm ci && git submodule update --init --depth 1 && node scripts/gclient-sync.ts` (about 5 GB, ~6 minutes), then `npm run build` and `node scripts/test.js tests/<file>.test.ts`. Lint: `npx eslint <files> && npx prettier --check <files>`. Node 22.21.1 is at /workspace/node-v22.21.1-linux-x64.

## Notes
Reporter amirkhakshour files audit-style bugs (#3601, #3604, #3606, #3607), all labelled confirmed,p3 and with no PRs yet. Picked #3601 only (one per repo). #3606 (heapsnapshot sortBy never applied) is a good follow-up for another day.
