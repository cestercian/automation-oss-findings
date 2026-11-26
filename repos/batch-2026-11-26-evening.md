# 2026-11-26 evening batch

- undici #6248 review fix pushed (7fc8d7f4), one reply.
- New: symfony #68446 -> #68448; reflex #7996 -> see reflex-dev-reflex.md.
- Skip list: eslint/eslint (PR template has an "AI acknowledgment" checkbox section).
- Skipped: apprise #1927 (reporter PR #1928), apprise #1918 (#1919), mongoose #16756 (#16758), vuetify #23436/#23437 (caret/tooltip, needs real mobile/browser repro, #23437 is more feature ask), videojs #9854 (mux-embed ambient types; fix means vendoring ~1k lines of mux-embed d.ts or a build copy hack, maintainers may prefer fixing mux-embed upstream), zod (skip list), pm2 #6185 (feature).
- Open PRs needing a rebase (conflicting), waiting for Yash's OK: rails #59567, rails #58954, salt #70633, partiql #1977/#1978/#1979, payload #19144, litellm #49407, goose #1118, hermes-agent #123108/#123116, omnigent #8312, OrcaRouter-Lite #166.
- Red CI seen on open PRs is infra/approval gated (buildkite unit-tests on dagster, argos/e2e on mermaid, rails docs-preview, salt windows builds, mattermost CLA, kata gatekeeper, rclone linux_386), not touched.
