# payloadcms/payload

- Stars: ~45k
- Evaluated: 2026-10-23 (Batch37)
- Contribution rules: CONTRIBUTING + AGENTS.md, AI tools explicitly covered (allowed). PR template: conventional-commit title, What?/Why?/How?, Fixes #. Base main = v4, 3.x = v3 bug fixes.
- CLA / DCO: none seen.
- Claim norms: none strict; claimed #19008 anyway.
- Outside contributors do get merged (lazerg, SatvikMishra08, Metehan-Bicer, AmalMon19, toyeshhm).
- Target: #19008 plugin-cloud-storage getFilePrefix find() drops isReadingStaticFile, so static-only read rules 500 without ?prefix= since 3.90.
- Decision: OK to contribute.

## Batch37 update (2026-10-23 evening)
- Opened #19011 (fixes #19008), base main, verified commit d9f586e. Same bug on 3.x, offered backport in PR.
