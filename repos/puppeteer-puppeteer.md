# puppeteer/puppeteer

- Stars: 95.7k
- Evaluated: 2026-10-18 (batch31)
- Result: skipped

## Contribution rules
Contributing docs on site.

## AI / agent policy
No ban found.

## CLA / DCO
Google CLA.

## Claim norms
-

## Tests / CI
npm test.

## Decision
SKIPPED: #15497 previous PR closed stale; no other free bugs.

## Batch36 update (2026-10-23)
Skipped: #15630 has PR #15631, #15497 had two closed PRs, #14508 (license-checker swap) still 'we are considering' per OrKoN. Rest are old features. Google CLA (cestercian has merged google-gemini PRs, so CLA likely already signed).

## Update 2026-10-25 (evening run)
- Midday run opened #15664 (fixes #15661). Verified, CI green.

## Update 2026-10-26 (evening run)
- #15664: Lightning00Blade asked for structuredClone and for the feature flag test to be split. Done in ae177bd and replied.
- Some CI shards failed with ERR_MODULE_NOT_FOUND for node_modules/puppeteer/lib (build artifact missing, an infra issue unrelated to the diff).
