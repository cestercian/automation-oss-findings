# mobile-dev-inc/Maestro

- Stars: 16.1k
- Evaluated: 2026-10-18 (batch32)
- Result: picked

## Contribution rules
CONTRIBUTING.md: simple fixes can go straight to a PR; squash merge so the PR title becomes the commit subject. Issues are mirrored to Linear (MAE-xxx).

## AI / agent policy
AGENTS.md: never add AI attribution trailers or Signed-off-by. No ban, no disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
JDK 17. `./gradlew :maestro-cli:test` (the build rewrites maestro-cli/mcp-viewer/package-lock.json, revert it before committing).

## Decision
PICKED #3682 (flow name over 255 bytes aborts the run when creating the artifact dir). Claim: https://github.com/mobile-dev-inc/Maestro/issues/3682#issuecomment-6252594017. 4 new tests in TestDebugReporterTest; full maestro-cli test suite green. Also seen: #3659 (U+0000 in stripInvalidXMLChars), left for later.

## Batch37 update (2026-10-23 evening)
- PR #3693: maintainer Fishbowler pushed a simplifying commit on our branch (2026-10-23 ~6:33 PM IST). Replied thanks. Good sign, maintainer engaged.
