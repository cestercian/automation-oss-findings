# Misc 2026-11-22 evening

Part 1: no unanswered human reviews or red CI caused by our changes. salt #70908 all green, video.js #9833 waiting for maintainer CI approval (Vercel fork failure only). Nothing merged or closed upstream since 06:30Z (only our own fork PR cestercian/video.js#1, closed at midday).

Picks: video.js #9759, dagster #34468 (see repo files).

Skip-list additions:
- gradio-app/gradio: CONTRIBUTING says PRs from outside the maintainer team are paused, and the PR template has an AI disclosure checkbox. Hard skip.
- huggingface/transformers: only issues labeled `triaged` (own) / `contributions-welcome` / `New model` may be worked on, and "can I work on this" comments are banned. Claim workflow does not fit. Skip.
- pydantic/pydantic: must be assigned before a PR (PR template checkbox "I am assigned"). Skip.
- capricorn86/happy-dom: AI tool disclosure required in PR. Skip.
- langchain-ai/langchain: assignment gating (already noted). #42021 skipped.

Looked at, not taken:
- rclone #10424 (RemoteStats race): already fixed on master by #10330. #10418/#10420/#10422 have PRs #10419/#10421/#10423 by the reporter zhengdaodeguL (no closing keyword, so cross-ref scans miss them; search the reporter's PRs).
- zigbee2mqtt #33767 (timers from the old controller after watchdog restart): reporter Monofin is actively sending similar shutdown/cancel fixes (#33762, #33763), likely to fix it himself. Fix would be in lib/extension/receive.ts (zhc globalStore.clear() does not cancel timers).
- bootstrap #43437 (.menu-item.selected colors): needs-decision and the docs present bold + check as the intended selected style. #43436 by design (miken32).
- nginx/kubernetes-ingress #11488 (--watch-secret-namespace ignored in all-namespaces mode): maintainer spencerugbo has open PRs reworking namespaces/tenant installs (#11485-#11487 touch controller.go and a tenant-secret-namespace test). Repo allows AI ("Using AI tools" section). Revisit after those land.
- crush #4376 ($defs dropped from MCP tool schemas): open PRs #4253 and #3782 already.
- svelte #19243: dup of #19170, PR #19171 open. ray #68089: reporter has a branch. helm #32920: claimed by 1122Louis. tailwindcss #20741: filed by capy-ai bot with its own patch. docling #5510: already fixed by #5322. transformers #51093: reporter mid-bisect, plus policy above.
- Kysely: dozens of fresh typing bugs filed by maintainer igalklebanov himself (likely his own backlog).
- VictoriaMetrics #11989 etc: perfloop-agent reports with their own fix diffs.
