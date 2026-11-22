# saltstack/salt

- Stars: 15.7k
- Evaluated: 2026-10-18 (batch32)
- Result: picked

## Contribution rules
CONTRIBUTING.rst: target the oldest supported branch where the bug exists (3006.x, 3007.x, 3008.x are active, fixes merge forward). Changelog file `changelog/<issue>.<type>.md` required (towncrier). PR template asks about tests, changelog, GPG.

## AI / agent policy
agents_CLAUDE.md: never add AI attribution lines. No ban, no disclosure requirement.

## CLA / DCO
No CLA, no DCO.

## Claim norms
Comment on the issue.

## Tests / CI
Python 3.11 venv with `requirements/static/ci/py3.11/linux.lock`, then `pytest -p no:system-statistics tests/pytests/unit/test_minion.py` (the sysstats plugin crashes/hangs locally otherwise). `test_resolve_dns_retry_aborts_on_shutdown_request_69466` fails on a clean checkout here. black 24.2.0 / isort 5.13.2.

## Decision
PICKED #70393 (after a zmq_monitor reconnect, __master_alive runs every second and the disconnect deletes the wrong job name). Based on 3007.x (3006.x defaults zmq_monitor off). Claim: https://github.com/saltstack/salt/issues/70393#issuecomment-6252757653. Most merges come from staff (dwoz, twangboy) but outside PRs do land. Also seen: #70396 (behavior change, not picked).

## Update 2026-10-28 (midday run)
- CI quirk: the Pre-Commit job runs black 24.2.0 (pinned in .pre-commit-config.yaml) and fails the whole CI on formatting in test files. Run `black==24.2.0` on changed files before pushing.
- #70436: pushed c6556a04 "Run black on the master_alive minion tests" (verified; black 24.2.0 --check passes locally). CI did not auto-start on the new head; salt CI on fork PRs seems to start only after maintainer action (dwoz's force-push/label kicked off the last run).

## Update 2026-10-29 (midday run)
- #70436: rebased onto 3008.x (base 3be18797ec) with one trivial EOF conflict in the test file. New head 77087bce is verified and the PR is mergeable again. The 5 master_alive tests pass locally, and full CI needs a maintainer.

## Update 2026-10-31 (midday run)
- #70619 (fixes #70616, opened in the Oct 30 evening run, head was d9b9fcac, twangboy approved) failed "Lint Salt's Test Suite": pylint W8470 resource-leakage on bare `open()` in tests/pytests/unit/utils/test_find.py. Fixed in 82fc6568 (verified) by using `salt.utils.files.fopen`. The push dismissed twangboy's approval, and fork CI is back to action_required until a maintainer approves the run.
- Lesson: salt tests must use `salt.utils.files.fopen`, not `open()`. Run `pylint --rcfile=.pylintrc --disable=I <changed test files>` before pushing.

## Update 2026-11-01 (evening run)
- PICKED #70622 (masterapi RemoteFuncs._mine: clear=True path never assigns `data`, so UnboundLocalError and stale mine data). Base 3008.x. Claim: https://github.com/saltstack/salt/issues/70622#issuecomment-6559741580
- CloudAgent must use the fork URL (https://github.com/cestercian/salt) and fetch upstream 3008.x itself.

## Update 2026-11-19 (evening run)
- PICKED #70792 (filed by maintainer dwoz with the fix shape: thread `options` through ssh.check_key_file for ssh_auth test=True). Claim: https://github.com/saltstack/salt/issues/70792#issuecomment-7013279875 . Agent bc-12540220 (grok-4.7 high). Opened #70864 (base 3008.x, 3bf74cce verified). Fork CI waits on maintainer approval. Recent merges all target 3008.x.
- #70830 (win_pdh for/else) had PR #70828 (closed); #70860/#70853/#70833 not looked at in depth.

## Update 2026-11-22 (midday run)
- #70864 merged by dwoz (2026-11-21 03:28Z). #70619 merged by dwoz (2026-11-20).
- PICKED #70742 (dup of #66022, assigned to dwoz since 2024 but idle; dwoz gave the fix shape on #70742 2026-11-13: `_parallel_map` threads lack `contextvars.copy_context()`). Claim: https://github.com/saltstack/salt/issues/70742#issuecomment-7075720275 . Agent bc-271cc4e7 (grok-4.7 high). PR #70908 (base 3008.x, f64ad729 verified): copy_context per worker + non-dict runner returns handled in saltmod (test.py untouched), unit tests + orchestrate integration test (--run-slow), changelog/66022.fixed.md. Upstream CI ran without approval this time; lint/pre-commit/docs green.
- #70891 (minion log level) has dwoz's own PR #70892. #70671 is not a bug (alternatives module moved to extensions).
