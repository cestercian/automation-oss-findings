# 2026-11-19 evening run

## Step 1 (our PRs)
- symfony #68261 review fixed (42b969e6), retarget to 7.4 waiting for Yash. rolldown #11422 merged.
- No other unanswered human reviews on PRs updated since Nov 16. Red CI seen is infra/gates: temporal #12886 (Misc checks/Mixed brain), dagster buildkite, mermaid e2e-required, vector CLA, rails #58954 buildkite, kata gatekeeper, omnigent Maintainer Approval.

## Step 2 rejections / new rules
- jellyfin: LLM policy forbids LLM output in PR bodies/comments and "vibe coding" (https://jellyfin.org/docs/general/contributing/llm-policies/). ADD TO SKIP LIST. Note our open jellyfin #18713.
- celery: PR template links "Anti AI spamming Guidelines" (discussion #10932) and says ask in the issue/discussion before opening an AI based PR. Skip unless a maintainer OKs first.
- psf/requests: PR creation is collaborator-only, AI policy requires human owner. Skip.
- sqlalchemy: evaluating AgentScan to flag automated PRs (#13804). Skip.
- pm2 #6182 has PR #6183 (not cross-referenced, it's in our pm2 notes). htmx on hold (3 open: #4163 #4192 #4228); #4212 fixed by maintainer, #4219 AI-filed and unconfirmed.
- symfony #68275 (#68277), #68273 (#68274); vuejs/core #16353 (#16354); fastify #7231 (#7232/#7233); mongoose #16698 (#16704); echarts #21843 (#21844) all had PRs.
- Ghost #32851 (newsletter name flashes in the sending dialog): CONTRIBUTING welcomes straightforward bug fixes, but the new React admin publish flow needs a running Ghost to reproduce. Possible future pick.
- vuetify #23416 (sortable header should nest a button) and #23415 (VoiceOver double read) are S: triage a11y/design, not picked.
- hermes-agent: flood of fresh bot-style issues, still tracked in-house (#134889). Not picked.
