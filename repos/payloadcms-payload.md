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

## Update 2026-10-28 (evening run)
- Opened https://github.com/payloadcms/payload/pull/19144 (fixes #19140, streamed CSV header only covered first batch; regression from the download rewrite #14782 dropping #13009 pre-scan). Int tests need Localstack/Mongo, so only unit tests ran in the VM. We now have 3 open payload PRs (#19011, #19113, #19144); hold off on more here.

## Update 2026-10-29 (midday run)
- #19144: handled CodeRabbit review with signed commit bada708 (raw columns captured before exportHooks.before, new test, shortDoc takes an object param). Declined CSV formula escaping in a reply because it's pre-existing behavior and would change import round trips; offered to do it separately. Main CI is still waiting on maintainer workflow approval.

## Update 2026-10-29 (evening run)
- #19144: replied to the CodeRabbit outside-diff Minor note (merge first-batch keys before padding) without a code change: the pre-scan vs stream race can hit any page and the CSV header can't widen later. Offered to change it if a maintainer prefers. https://github.com/payloadcms/payload/pull/19144#issuecomment-6500325501
