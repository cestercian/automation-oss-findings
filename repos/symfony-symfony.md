# symfony/symfony

- Stars: 31.2k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
CONTRIBUTING.md.

## AI / agent policy
No ban found.

## CLA / DCO
-

## Claim norms
-

## Tests / CI
phpunit.

## Decision
SKIPPED: #67040 has PRs; remaining good-first-issues are translations.

## Batch36 update (2026-10-23)
Skipped: no open Bug-labeled issues except old #40705; only translation good-first-issues left (hu/uz/uk/sk/ro), need native speakers. #67310 has PR #67320.

## Batch37 update (2026-10-23 evening)
- Looked at #67369 (cache checkpoint time=now / index -1 when state missing). Cold start behaves the same, labeled Needs Review, design debatable. Skipped.

## Update 2026-10-25 (midday run)
- #67448 (Intl 3-letter locales) Needs Review, needs big Intl data regen; #67369 needs reproducer. 'Missing translations' good-first-issues skipped (need native speakers, not a fit).

## Update 2026-10-25 (evening run)
- carsonbot's "Missing translations" issues (#67416-#67435) say a native speaker must do them. Skip unless it's a language Yash actually speaks natively.
- #67487 is a design question, not a scoped fix.

## Update 2026-11-18 (evening run)
- No AI clause in CONTRIBUTING, PR template or symfony.com patches doc; repo now ships .agents/skills (pr-authoring etc). PR template table required; bug fixes target lowest maintained branch (6.4 / 7.4 / 8.1).
- Bugs get PRs within a day (#68225 has #68258, #68219 has #68232).
- PICKED #68259 (ReflectionExtractor::getWriteInfo returns adder/remover for singular `network` when `networks` has addNetwork/removeNetwork; findAdderAndRemover runs before setter lookup). Claim: https://github.com/symfony/symfony/issues/68259#issuecomment-6982550041 . Agent bc-44eadc3b (grok-4.7 high).
