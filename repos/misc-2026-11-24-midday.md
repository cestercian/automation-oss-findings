# Misc notes, 2026-11-24 midday

Issue backlog is saturated by drive-by PR farmers; almost every fresh bug on the big repos already has an open PR within hours. Check `repos/<r>/issues/<n>/timeline` cross-references (core API) instead of the search API, which hits the secondary rate limit fast.

- ollama/ollama: #19834, #19792, #19675, #19623, #19490, #19341, #19204 all have open PRs. #19767 is a design question.
- caddyserver/caddy: #8292, #8244, #8291 have PRs (some closed after maintainer pushback); no free bug issues.
- gin-gonic/gin: #4928, #4897, #4451 have PRs.
- temporalio/temporal: #12874, #13133, #12437, #12449 have PRs; #13174 and #13237 are deep / design level.
- saltstack/salt: #70771, #70832, #70760 have PRs; #70463 duplicate of #70354 (fix in #70380); #70671 not a bug (alternatives module removed in 3008).
- vuetifyjs/vuetify: nearly every bug has a PR; #22348 intended behavior.
- axios/axios, fastify/fastify, sveltejs/svelte: every fresh issue has a PR (axios issues are filed and fixed by the same bot-like accounts). svelte #19401: triage bot could not fix; area under heavy internal rework (batch-views-run-flatten), skip.
- prisma/orm: see prisma-orm.md.
- Search API: use sparingly, `gh api search/issues` hit secondary rate limits after ~10 calls.
