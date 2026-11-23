# Misc 2026-11-23 midday

Picks: semaphore #4456, fzf #4962, socket.io #5642 (see repo files).

Skip-list additions:
- jdx/mise: not accepting external PRs at all (GitHub blocks creation). Hard skip.
- hatchet-dev/hatchet: vouch request required before PRs. Skip.

Looked at, not taken:
- Saturation continues: undici (#6216, #6184, #6135, #6123, #6112, #6110, #6082, #6236, #6141 all have PRs), puppeteer (#15848, #15838, #15828, #15862, #15855, #15853, #15655 all have PRs), storybook #37648/#37639 (rome-xi PRs), vuetify #23401/#23321/#23391/#23418 have PRs, ollama #19827/#19834/#19841 have PRs, #19836 claimed by visy-ani, #19829 reporter posted a full patch.
- rclone #10426/#10422/#10420/#10418/#10415: reporter zhengdaodeguL has PRs #10427/#10423/#10421/#10419/#10416. #10264 (webdav PROPFIND Korean) too vague, onedrive-only. Same reporter does this in huggingface/datasets (#9130 -> #9131, #9128 -> #9129).
- litellm: TechyMT files issues and opens his own PRs within minutes (#53735/#53734/#53733/#53732); #53092 points at existing PR #48698.
- bootstrap #43044 already fixed in #43418 (mdo). #43051 Safari-only drawer position.
- loki #26553 (pattern ingester shutdown flush): design-heavy (ordering + multi-ingester stream conflicts), reporter lists three possible designs.
- rails #59792 has PR #59632 by reporter; #59153 (herb in non-main Ractor) needs Ruby 4 ractors, heavy.
- storybook #37463 (actions trigger story store deprecation): action.ts doesn't touch storyStore; caller not found without a sandbox.
- Chart.js #12430: filed by maintainer kurkle, says a behaviour change "needs deciding"; wozhenbang2004 owns the numeric counterpart (#12414).
- jq #3746: nicowilliams turned it into the binary-data-in-JSON design discussion.
- sveltejs/kit #17827: API request (move/insert/remove on array fields), not a scoped fix.
- tiptap #8787 reporter has a fix and asked to be assigned. haystack #13863 claimed by reporter. syncthing anti-AI (already noted).
- hatchet #5425/#5416/#5390: good first issue + accepted, but vouch gate and multiple claimants.
