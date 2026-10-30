# Koenkk/zigbee2mqtt

- Stars: 15.7k
- Evaluated: 2026-10-18 (batch31)
- Result: picked

## Contribution rules
CONTRIBUTING.md: PRs always against `dev`. 100% coverage enforced (`pnpm test:coverage`), biome lint/format (`pnpm run check`).

## AI / agent policy
AI-driven PRs are allowed but anything over 500 lines will not be considered. No disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
pnpm 11 (corepack), `pnpm test:coverage`, `npx tsc --noEmit`, `npx biome check lib test`.

## Decision
PICKED #33399 (device `throttle` ignored because messageNonEmitted lastSeenChanged events publish full state directly). Claim: https://github.com/Koenkk/zigbee2mqtt/issues/33399#issuecomment-6245900977. Most other open issues are device support that belongs in zigbee-herdsman-converters.

## Outcome
PR #33423 (fix for #33399, base dev) merged by Koenkk on 2026-10-18, about 20 minutes after opening. Small focused fixes with tests land fast here.

## Batch35 update (2026-10-22)
PICKED #33464 (HA extension republishes `light_type` select as `{"light": ...}` on `<device>/type`, because `onPublishEntityState` matched object ids by `light_`/`cover_` prefix). Fix: only for discovery component `light`/`cover`. Claim: https://github.com/Koenkk/zigbee2mqtt/issues/33464#issuecomment-6344104640. PR: https://github.com/Koenkk/zigbee2mqtt/pull/33472 (base dev, 857 tests, 100% coverage, full CI matrix green). PRs to `dev` don't auto-link "Fixes #N" as closing references (non-default branch).

## Update 2026-10-30 (midday run)
- Rules: PRs target the dev branch; AI-assisted PRs must stay under 500 lines; 100% test coverage required; run pnpm run check.
- Opened #33530 (fixes #33515, frontend WebSocket server sends 30s pings and terminates dead clients). Verified commit 55922ec4. CI all green (11 checks). Opened via gh from box (agent token can't create upstream PRs).
