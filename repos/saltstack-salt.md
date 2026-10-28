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
