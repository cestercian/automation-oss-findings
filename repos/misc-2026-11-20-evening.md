# 2026-11-20 evening run

## Step 1 (our PRs)
- CHANGES_REQUESTED: only salt #70436 (waits on Yash, rebase) and hyperswitch #7659 (stale, leave open).
- Red CI: dagster #34359 / #34341 are buildkite "failed and blocked" (external contributor gate, not our code). omnigent #8312 needs Maintainer Approval plus 24h CI freshness; no code fix needed. Others are known/old. No pushes done.

## Step 2 picks
- twbs/bootstrap #43423 (confirmed v6 bug: combobox first in .input-group loses start radius because Combobox inserts a hidden input before the toggle). Repro with built dist + Chrome: start radius 0 -> 8px, -1px margin overhang fixed. PR #43426, head 2385b612 (verified). Claim: issuecomment-7042956675. Bootstrap has no AI policy; dist/ is tracked, don't commit it.
- pulumi/pulumi #25798 (staff-filed R1: python docRefResolver used Get_serverArgs/Get_serverResult). PR #25810, head 4b130456 (verified), new TestDocRefResolverFunctionProperties + changie entry. Claim: issuecomment-7043113203. Cursor auto-opened both PRs after the app-token 403.

## Rejections / skip-list notes
- typescript-eslint: AI policy says avoid AI-generated PR descriptions/comments. Same bucket as zed/zellij, SKIP for agent runs.
- mlflow/mlflow: PRs auto-closed unless a maintainer applied the `ready` label; triage bot opens PRs itself. SKIP.
- python/mypy: discourages LLM use by new contributors, closes mostly-LLM PRs. SKIP.
- uutils/coreutils: AI allowed (no GNU code, human replies, short PR text), but every fresh issue gets claimed within hours (#16496, #16507, #16420, #16644, #16646, #16647, #16690 all claimed). Watch for new sylvestre issues early.
- symfony #68275 already fixed by #68277; #68298 is architectural. anime #1205/#1207 have reporter PRs. vuetify #23422/#23416 claimed. dagster #34405 has PR #34406; #34440/#34301 need maintainer direction. ollama #19792 overlaps open #18953. excalidraw #12656 has #12657. hoppscotch #6797 has #6798. plotly.js #8182 reporter waiting to open PR. echarts #21843 has #21844. undici #6075 backported (#6076), #5999 fixed in 6.29.1. rails #59792 has #59632. outline #14674 is Linear-tracked (team fixes). jupyterlab #20369 belongs in jupyter_server.
