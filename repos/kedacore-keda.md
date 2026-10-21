# kedacore/keda

- Stars: 10.6k
- Evaluated: 2026-10-21 (batch34)
- Result: skipped (looked at #8280, flaky Splunk Observability test hang)

## Contribution rules
CONTRIBUTING "Zero-spam & PR authorization policy": an issue must exist and be approved, and you must be ASSIGNED by a maintainer before starting work. Agents must ask the human to request assignment and wait. PR titles `Component: Description`; keep the full template checklist.

## AI / agent policy
Agents allowed but must follow AGENTS.md, which forbids --no-verify and requires make fmt/vet/golangci/test locally.

## CLA / DCO
DCO.

## Claim norms
Assignment required, not just a claim comment.

## Tests / CI
make test, golangci-lint.

## Decision
SKIP for batches unless an issue is already assigned to cestercian (assignment wait doesn't fit a batch).
