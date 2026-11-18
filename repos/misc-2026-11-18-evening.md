# 2026-11-18 evening run

## Step 1 (our PRs)
- tsrx #1079: jonkwheeler review (merge main, import map_iterable_async, runtime tests, Fixes #863, README). Agent bc-5f4b07ac merging main (signed merge, no rebase).
- rolldown #11422: see rolldown notes, agent bc-2f7e702f.
- partiql #1978: approved but conflicting; agent bc-51d0c706 (composer-2.5) merging main.
- pm2 #6179 / temporal #12886: no new review since our last push; temporal approved, CI red from infra.
- mermaid #8609: filipsajdak comparison with #8694, no action asked (maintainers decide). mermaid #8549 e2e-required red is a gate, not our diff.
- salt #70633 functional zeromq failures, dagster buildkite blocked, mattermost CLA, kata gatekeeper: not caused by our diffs.

## Step 2 rejections (everything fresh already has a PR, often from the reporter)
- undici #6184/#6202/#6187/#6216/#6143/#6144/#6149/#6141/#6204 all have PRs.
- puppeteer #15750 (#15751 by reporter), #15828 (#15830).
- vuetify #23321 (#23322), #23401 (#23402), #23376, #23391; #23412 memory leak has no minimal repro (S: triage).
- anime #1205 (#1206), #1207 (#1208), both reporter PRs.
- dagster: every new issue (#34403 to #34446) has a PR.
- rails #59741/#59736/#59791/#59721/#59215/#59581/#59152 have PRs; #59792 claimed with PR #59632; #59733 is a design discussion.
- svelte #19307/#19256/#19251/#19264/#19275, axios #11446/#11448/#11450/#11460/#11463, caddy #8399/#8401/#8427, socket.io #5616-#5629, crewAI, smolagents, react-router bug-labeled ones, nx, three.js, excalidraw, zx #1554: all have PRs.
- hugo: still skip (AI disclosure); note cestercian hugo #15607 (for #15595) was closed today by bep ("needs a conclusion in the issue").
