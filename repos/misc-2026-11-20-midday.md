# 2026-11-20 midday run

## Step 1 (our PRs)
- rclone #10391: mac_amd64/windows red from our test (os.Stat("report.txt") hits Report.TXT on case-insensitive FS). Signed fix d2384ba7 (composer-2.5, normal push) compares exact dir entry names. Fork CI run is action_required (maintainer approval).
- temporal #12872 (approved by stephanos) and #12886 (approved by chanric): Misc checks / Mixed brain red because the branch was behind main (protoc via mise). GitHub update-branch on both (heads eba7bf76, 4eb9a799).
- salt #70436: twangboy CHANGES_REQUESTED again 2026-11-19 asking for a rebase. Already flagged, waits for Yash OK (no force-push).
- rails #59567 and #58954 conflict with main (DIRTY). Rails wants rebases, so these wait for Yash OK. litellm #47276 DIRTY too.
- salt #70864 newly approved by twangboy (BEHIND, no action needed). partiql #1977/#1978/#1979 re-approved by xd1313113. oxc #27975 approved by Dunqing.

## Step 2
- PICKED nrwl/nx #37966 (SIGTERM + closed stdout pipe leaves continuous tasks orphaned). Claim: https://github.com/nrwl/nx/issues/37966#issuecomment-7032964919. PR https://github.com/nrwl/nx/pull/37970, head fcb8f36f (verified). Repro before/after: 5 orphaned tasks -> 0. Cursor auto-opened the PR again after the app token 403; body replaced via gh.
- Fork sync for cestercian/nx via `POST repos/cestercian/nx/merge-upstream` worked (token has workflow scope now).

## Rejections / new skip-list entries
- go-gitea/gitea: AI disclosure required (Assisted-by trailer). SKIP.
- marimo-team/marimo: AGENTS.md requires "authored by a coding agent" line. SKIP.
- pola-rs/polars: AI disclosure in PR template. SKIP.
- neovim/neovim: AI-assisted trailer required, no one-shot AI PRs. SKIP.
- renovatebot/renovate: AI disclosure section in PR template. SKIP.
- atuinsh/atuin: AGENTS.md requires an AI disclosure line. SKIP.
- meilisearch/meilisearch: bans generative AI in external contributions. SKIP.
- modelcontextprotocol/servers: maintainers-only PRs ("we accept issues, not pull requests"). SKIP.
- open-webui/open-webui: PR template requires a CLA checkbox (legal agreement for Yash). SKIP unless Yash OKs.
- zed-industries/zed and zellij-org/zellij: no LLM-written PR descriptions/replies. Risky, skip for agent runs.
- syncthing: still HARD SKIP (anti-AI).
- rails #59882 (perform_now leaves job in ExecutionContext): open PR #54663 (BlakeWilliams) covers it, byroot asked to split. Not taken.
- helm #32920 claimed (1122Louis). webdriverio #16076 has #15980. streamlit #17830 reporter sending PR, #17234 design-y. rclone #10224 fixed by Proton-API-Bridge#8. gradio #13976 claimed (Mrun25). bullmq #5160 claimed. browser-use #6476 already fixed in 0.12.1. Ghost #33178 reporter has a patch, waiting on #33030. trigger.dev (vouch) and keda (assignment) still skipped. pulumi #25788 fix lives in pulumi-dotnet / pulumi-java codegen.
