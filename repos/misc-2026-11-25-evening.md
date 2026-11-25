# Misc notes, 2026-11-25 evening

Saturated again. Only one fresh issue was free.

- hermes-agent #160064 picked (see NousResearch-hermes-agent.md). #160062, #160067 also free at the time but one PR per repo.
- Already have PRs: temporal #12874 (#12875), undici #6202/#6187/#6184/#6144, ollama #18274, dagster #34405/#34301/#34440, payload #19917/#19867.
- payload #19920 (COMMIT error swallowed) is already fixed on main by #19159 (beginTransaction rethrows), so a PR would be tests only. Skip.
- puppeteer #15005: three earlier PRs closed, maintainer says Chrome behaviour changed. Skip.
- chrome-devtools-mcp #3605: depends on open #3612 (worker sort order), would conflict. Skip until #3612 lands.
- aider: effectively unmaintained, old bug issues only.
- vuetify #23436/#23437: still `S: triage`, no confirmation.
- Review fix: semaphore #4458 CodeRabbit race in TerraformApp_test fixed with a mutex (7c39cd95).
