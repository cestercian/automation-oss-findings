# twbs/bootstrap

- No AI policy in CONTRIBUTING; PR template has Description / Motivation / Type / Checklist / Related issues. dist/ and js/dist are tracked: never commit build output.
- v6 bugs get `confirmed` + `v6` labels; mdo fixes many himself in batch PRs, so pick confirmed issues nobody has touched.
- JS bundle is ESM: load `dist/js/bootstrap.bundle.js` with type=module over http (python -m http.server) for repros.

## Update 2026-11-20 (evening run)
- Opened #43426 (fixes #43423): input-group corner rules skip `input[type="hidden"]`, reset margin on first visible element after a leading hidden input. Signed head 2385b612 (verified). stylelint + css-test pass.

## Update 2026-11-21 (midday run)
- Opened #43434 (fixes #43431): range-track fill stops use the thumb-center calc like `.form-range-bubble`. Signed head b7d82151 (verified). css-lint + css-test pass; Chromium mismatch 7.8px -> 0 at the ends.
- pricop files many v6 bugs and often PRs them himself (#43430 for #43415); claim within hours.

## Update 2026-11-22 (midday run)
- #43434 merged by mdo (2026-11-21 21:40Z) after pricop confirmed the fix. #43428 claimed by nikhil-304, #43404 has pricop's #43406, #43436 is by design, #43437 needs-decision.
