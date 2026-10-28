# storybookjs/storybook

- Stars: 91.3k
- Evaluated: 2026-10-18 (batch33)
- Result: picked

## Contribution rules
CONTRIBUTING: PRs target `next`. Title format `Area: Summary`. PR body needs a `#### Manual testing` section; maintainers add labels.

## AI / agent policy
AGENTS.md has workflow notes for agents. No ban, no disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
Node 22, `corepack yarn install --mode=skip-build --json` (the plain fancy output dies silently in the Fetch step here). Then `cd code && yarn vitest run <file>`. Manager tests that import `storybook/manager-api` need `vi.mock` for it unless the package is built. Formatter is oxfmt.

## Decision
PICKED #36858 (sidebar reads `state.disableWhatsNewNotifications` instead of `state.whatsNewData.disableWhatsNewNotifications`). Claim: https://github.com/storybookjs/storybook/issues/36858#issuecomment-6272686952. Also claimed #36873 (waitForAnimations on scroll timelines) first, then found it already fixed on `next` by #31900, so it was dropped; that claim comment is still up.

## Update 2026-10-24 evening (batch39)
- #36844 no reproduction yet; we already have #36899/#36858/#36848/#36855 open. Skipped.

## Update 2026-10-28 (evening run)
- Our open PR #36887 got the label agent-scan:automated (storybook runs an automated-account scanner). #36844 has no repro. Treat storybook as risky for new PRs.
