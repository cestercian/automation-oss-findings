# Rejections 2026-11-01 (midday run)

- docker/compose #14429: CONTRIBUTING requires AI disclosure under the Moby AI policy (AI_POLICY.md). SKIP repo (queued pick dropped).
- rolldown/rolldown #11395, #11399: claimed by another contributor with a branch ready. #11348/#11349 covered by #11358. #11264 has PR #11265.
- BerriAI/litellm #49551 (reporter has a fix), #49479 (claimed), #49359 (someone has a branch), #49253 (others tracing).
- mrdoob/three.js #35293 (PR #35294), #35297 (reporter offered a PR).
- stanfordnlp/dspy #10732: PR #10733 exists.
- langflow-ai/langflow #16084: reporter opened #16085.
- robotframework/robotframework #5840: Pekka fixing it himself (2a5f984).
- Significant-Gravitas/AutoGPT #16414/#16080: PRs exist.
- esphome/esphome #21607: needs an upstream MideaUART change first.
- ollama/ollama #19403 (claimed), #19424 (not a bug per maintainer).
- apache/superset ai-candidate issues: #45885/#45475 need design, #45802 already fixed on master, #45429 py3.13 canary. Maintainers wary of drive-by AI PRs.
- jdx/mise: Windows-only candidates plus a ban on AI replies.
- apify/crawlee #4315: design question.
- meilisearch/meilisearch: generative AI banned in external contributions (PR template certification, no-agents AGENTS.md). SKIP repo.
- Textualize/textual: AI PRs must self-identify (agent name) and link a maintainer-approved issue. SKIP repo.
- celery/celery: anti AI spam guideline, must ask before AI-based PRs. SKIP repo.
- streamlit/streamlit: outside PRs paused. SKIP repo.
- gradio-app/gradio: outside PRs paused, AI disclosure mandatory. SKIP repo.
- tauri-apps/tauri: AI tool policy forbids AI-written review replies, closes with ai-slop. Treat as risky/skip.

## Picks
- rolldown/rolldown #11330 (getModuleInfo / this.resolve report moduleSideEffects null instead of the effective value). Claim: https://github.com/rolldown/rolldown/issues/11330#issuecomment-6554773767
- dagster-io/dagster #34376 (get_paginated_partition_keys skips the is_valid_key_format filter, yields malformed keys for dynamic keys with `|`). Claim: https://github.com/dagster-io/dagster/issues/34376#issuecomment-6554774351
