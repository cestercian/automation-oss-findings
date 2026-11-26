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

## Update 2026-11-19 (evening run)
- #68261: nicolas-grekas review (plural property instead of pluralize(), aircraft failed low-deps on symfony/string < 6.4.3, staff collection went to setter, retarget 6.4 -> 7.4, add [PropertyInfo]). Agent bc-87bb7de6 pushed 42b969e6 (verified, normal push): setter only wins when another declared property singularizes to the name; staff test added. Low-deps (8.2) CI now green. Title prefixed via gh. Replied.
- Retarget to 7.4 NOT done: waiting for Yash's OK (base-only `gh pr edit --base 7.4` may work without a push since 6.4 merges up into 7.4, but symfony usually wants the branch rebased onto 7.4 = force-push).

## Update 2026-11-21 (evening run)
- Fresh unclaimed bugs seen: #68299, #68298, #68275, #68259 (no PR yet at check time). Not picked: box has no php/composer, so no local phpunit repro. Bugs here get PRs within a day.

## Update 2026-11-22 (midday run)
- #68261 merged by nicolas-grekas (2026-11-19 16:36Z), so the 7.4 retarget question is moot. #68299 (#68306), #68298 (#68314), #68275 (#68277 merged) all taken.

## Update 2026-11-26 (evening run)
- PICKED #68446 ([Serializer] JSON int denormalized as float into `int|float`). PR #68448 to 7.4, head 498f4540 (Verified). Fix: skip the JSON int to float shortcut when the union also has int, in both validateAndDenormalize (TypeInfo) and validateAndDenormalizeLegacy. Two tests in ObjectNormalizerTest (TypeInfo + legacy getTypes-only extractor); both fail before, Serializer suite 1649 pass.
- Reproduces on 7.4 by default (TypeInfo and the 7.4 legacy path both sort union members, float before int). 6.4 only with `@var float|int` doc order, so 7.4 was chosen and the body offers a 6.4 version.
- Box now has PHP 8.4 + composer. Component testing recipe: `cd src/Symfony/Component/Serializer && COMPOSER_ROOT_VERSION=7.4.x-dev composer install`, then pin `--with symfony/property-info:7.4.* --with symfony/type-info:7.4.*` (composer picks 8.x otherwise and legacy anonymous extractors fatal), run phpunit 13 phar (`/tmp/phpunit13.phar`).
- Cloud Agent got 403 on upstream PR create but the PR showed up anyway (#68448); check before running gh pr create.
