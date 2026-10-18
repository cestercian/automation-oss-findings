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
