# vuetifyjs/vuetify

- Stars: 41k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
AGENTS.md/CLAUDE.md.

## AI / agent policy
AI tooling guidance only.

## CLA / DCO
-

## Claim norms
-

## Tests / CI
pnpm test.

## Decision
SKIPPED: #21503 fixed, #23045 PR closed, #23153 needs design, #23248 disputed by maintainer.

## Batch32 update (2026-10-18)
Batch32: #23268 a11y contrast not examined; #23248 disputed.

## Update 2026-10-27 (midday run)
- #23321 (good first issue, VBtn flash) has PR #23322. J-Sek: they don't assign outside core, just open PRs. Older T: bug issues mostly have PRs or are by-design (#22348).

## Update 2026-10-28 (midday run)
- AI policy: CONTRIBUTING says AI assistants pick up AGENTS.md / .claude rules; just review what they produce. No ban, no disclosure.
- PICKED #21452 (v-virtual-scroll jumps when items change; `help wanted`, root cause from KaelWD). Claim: https://github.com/vuetifyjs/vuetify/issues/21452#issuecomment-6462920900. PR: https://github.com/vuetifyjs/vuetify/pull/23326 (keep measured sizes by item key across item changes, 3 new browser specs). CI green.
- Quirks: cestercian fork master is stale and can't be synced via API (workflow scope), so branch from upstream/master; an agent PR against the fork's own master pulled in 600+ files (cestercian/vuetify#1, closed). `pnpm --filter vuetify tsc` fails on an existing downlevelIteration deprecation; use `pnpm --filter vuetify lint` (tsgo + eslint) instead. PR body follows the template (Description + full Playground.vue markup); commit msg format `fix(Component): ...`.

## Update 2026-10-28 (evening run)
- #23326: J-Sek asked if the move could be eliminated; our follow-up b0e753ef broke VSelect.spec.browser "no-auto-scroll on click" (expected 48 to be 0). Fixed in 6e7b1d8a (only shift scroll when rows land above the anchor), CI green. Lesson: run the VSelect browser specs too when touching VVirtualScroll.
