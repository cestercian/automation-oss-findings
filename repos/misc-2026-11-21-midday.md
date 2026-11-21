# 2026-11-21 midday run

## Step 1 (our PRs)
- No new unanswered human reviews since the Nov 20 evening run. CHANGES_REQUESTED only on salt #70436 (waits on Yash, rebase) and hyperswitch #7659 (stale, leave open).
- Red CI, not ours: rclone #10391 linux_386 fails in backend/cache TestInternalMaxChunkSizeRespected (PR only touches cmd/bisync + docs, flaky cache test). salt #70633 Windows onedir/source package builds die in ~1m (packaging infra; PR is masterapi.py + unit test, already approved). pulumi #25810: Frassle ran /run-acceptance-tests. No pushes needed.
- Still waiting on Yash's rebase OK: rails #59567, rails #58954, litellm #47276, salt #70436. jellyfin #18713 decision pending.

## Step 2 picks
- twbs/bootstrap #43431 (confirmed v6 bug by julien-deramond: range track fill drifts from the thumb near min/max). Fill gradient stopped at fill*100% while the thumb center is at thumb/2 + fill*(100% - thumb); now both stops use the bubble's formula. Chromium measurement (320px track, 16px thumb): mismatch 7.84/7.52/0/7.52/7.84px at 1/3/50/97/99 before, 0px after. css-lint + css-test pass. Claim: https://github.com/twbs/bootstrap/issues/43431#issuecomment-7059177635. PR https://github.com/twbs/bootstrap/pull/43434, head b7d82151 (verified). Cursor auto-opened the PR after the app-token 403 again. composer-2.5 took ~10 min.

## Rejections / new skip-list entries
- oraios/serena: PR template has a per-PR CLA checkbox and CLA grants relicensing to proprietary terms. SKIP (was a good candidate: #2286 tsgo includeDeclaration, maintainer said they'd accept a PR).
- huggingface/smolagents: CONTRIBUTING now requires a maintainer-validated issue assigned to you before any PR (unassigned PRs closed with needs-assigned-issue). SKIP (#3230 base_url + model_id was a clean bug).
- mastodon/mastodon: AI policy bans autonomous agent PRs and requires Assisted-by trailer. HARD SKIP.
- AdguardTeam/AdGuardHome: outside PRs basically never merged (internal mirror). Skip.
- vuetify #23412 (VDataTable retained via useProxiedModel externalValue getter): could not reproduce the V8 accessor retention with @vue/reactivity + WeakRef/gc in node (closure getter and shared getter both collected), root cause unconfirmed. Not taken.
- Saturation note: almost every fresh bug in big repos (symfony #68299 -> #68306, vue #16369 -> #16372, undici #6236 -> #6237, react-router #15807 -> #15808, black #5721 -> #5722, etcd #22877 -> #22878, mongoose, prefect, litellm, supabase, appwrite, npm/cli, datasets...) gets a PR from the reporter or a bot within 1 to 3 hours. "PR welcome" issues (eslint #21526, loguru #1542, maplibre #9088, alacritty #9070, accelerate #4588, etcd #22747, pyodide #6569, haystack #13830/#13761) all already have PRs or claims.
- Possible future picks: supabase #53779 (inline SQL editor drops results on expand; EditorPanel.handleExpand creates a snippet without carrying results, needs Studio to verify), bootstrap #43428 (range bubble overlaps label, needs a design call: show on hover/drag).
