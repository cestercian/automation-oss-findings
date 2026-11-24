# fluent/fluentd

- Stars: 13.6k
- Evaluated: 2026-11-24 evening
- Result: picked #5676

## Contribution rules
PRs to `master`. Tests required (`bundle exec rake test`, or a single file with `bundle exec ruby -Itest test/plugin/test_x.rb`). PR template: "Which issue(s) this PR fixes / What this PR does / Docs Changes / Release Note".

## AI / agent policy
Nothing in CONTRIBUTING or the template.

## CLA / DCO
DCO bot: every commit needs `Signed-off-by` (git commit -s).

## Tests / CI
Ruby 3.3+. `bundle config set --local path vendor/bundle && bundle install` works with system ruby 3.3 (bundler lives in ~/.local/share/gem/ruby/3.3.0/bin). Rubocop is not in the bundle. out_exec_filter tests take ~10s each.

## Notes
#5676 (in_exec/out_exec_filter stop reading after one ParserError): JSON parse_io and msgpack parse_io/parse_partial_data now skip only the bad record, line mode rescues per line. #5677 (same reporter, Watson1978, maintainer) is the buffer chunk key change bug, left for later.
