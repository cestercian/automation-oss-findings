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
