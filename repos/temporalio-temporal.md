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

## Update 2026-11-01 (evening run)
- PICKED #12837 (SQLite IsDupEntryError uses a bitmask `Code()&0xE13 != 0`, so BUSY/LOCKED/IOERR/NOT NULL etc. count as dup-key). No cross-referenced PRs. Claim: https://github.com/temporalio/temporal/issues/12837#issuecomment-6559740935
- CloudAgent must use the fork URL (https://github.com/cestercian/temporal); the upstream URL is "not accessible to the connected GitHub account". Has a CLA bot.

## Update 2026-11-02 (evening run)
- #12872 (for #12837) still open, CLA signed.
- #12874 and #12881 already have PRs. Skip.
- PICKED #12880 (child completion dropped after a parent reset once the old run is deleted by retention; resolve the current parent run on NotFound). Claim: https://github.com/temporalio/temporal/issues/12880#issuecomment-6580490058 . Agent bc-c34a5714.
