# temporalio/temporal

- Stars: 23.8k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
CONTRIBUTING.md + AGENTS.md.

## AI / agent policy
No ban found.

## CLA / DCO
Temporal CLA.

## Claim norms
-

## Tests / CI
make test.

## Decision
SKIPPED: #11721 has PR #11727; remaining issues are deep replication bugs.

## Batch32 update (2026-10-18)
Batch32: #12300 is a deep shard-reload replication bug.

## Batch36 update (2026-10-23)
Skipped: #12652, #12647, #12611, #12625, #12506, #12493 all have PRs.

## Update 2026-10-26 (evening run)
- #12652: claimed, then withdrew. Open PR #12671 (A-RYAN-1) already covers it but is not formally linked, so a `-linked:pr` search misses it. Check the issue timeline for cross-referenced PRs before claiming.
- No temporal PR opened.

## Update 2026-10-27 (midday run)
- #12746 has PR #12749. #12722 (dynamic config callback ordering): maintainer dnr is still discussing the design (sharded queues vs generation counter); not a scoped fix yet.

## Update 2026-10-28 (evening run)
- #12783/#12784 belong to maintainer stephanos's internal lock-assertion work; #12784 claimed by BBtacker. Nothing taken.

## Update 2026-10-29 (evening run)
- #12792 (single-node ring after a DB outage) has a contributor asking to take it; #12782/#12784 are maintainer lock work. Nothing taken.
