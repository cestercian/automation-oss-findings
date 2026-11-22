# videojs/video.js (~40k stars, v10 monorepo)

- AI-friendly: CONTRIBUTING has a "Using AI" section, AGENTS.md/CLAUDE.md, no disclosure rule. No CLA (DCO text, no sign-off check). Claim unclaimed issues via a comment.
- Triage bot (github-actions) labels `confirmed` with a written analysis. `agent:pr` label (human-applied) triggers a Codex implementer, so skip issues carrying it.
- Mostly maintainers merge (luwes, cjpillsbury, spuppo-mux, decepulis, mihar-22); a few outside contributors merged.
- Fork PR CI needs maintainer approval (action_required). Vercel check fails on forks with "Authorization required to deploy" (not ours). A codesmith footer is auto-added to PR bodies by the repo.
- pnpm workspace: `pnpm lint`, `pnpm typecheck` (after `pnpm -F <pkg> build`), `pnpm test`; tests use vite-plus (`vp test`).

## Update 2026-11-22 (midday run)
- PICKED #9769 (react-native player/media dead after <Activity> hide/show; port of #9768). Claim: https://github.com/videojs/video.js/issues/9769#issuecomment-7075766083 . Agent bc-5bc7c8fa (grok-4.7 high). PR #9833 (786cca96 verified): useDestroy clears pendingRef + useInstance, provided media untouched, first vitest setup for packages/react-native. Agent also opened a fork PR (cestercian/video.js#1, closed) with Fixes in body; body scrubbed.
- #9796 has PR #9797; #9812 is a bigger coordinator lifecycle issue; #9708 not reproducible per orcnd.
