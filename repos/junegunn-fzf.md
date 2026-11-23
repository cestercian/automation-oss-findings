# junegunn/fzf

- Stars: ~78k
- Evaluated: 2026-11-23 (midday run)
- Result: picked

## Contribution rules
No CONTRIBUTING, no PR template. junegunn fixes most core bugs himself; outside PRs that land are mostly shell integration (bitraid fish, sim590 nushell, LangLangBart zsh tests). Contributors add a CHANGELOG.md line.

## AI / agent policy
None found.

## CLA / DCO
None.

## Tests / CI
Integration tests are Ruby + tmux: `go build -o bin/fzf .`, `bundle install` (racc needs make/gcc), then
`dir=$(mktemp -d); env -u TMUX TMUX_TMPDIR=$dir sh -c 'tmux -f /dev/null new-session -d && bundle exec ruby test/test_shell_integration.rb -n "/TestBash#test_ctrl_r/"; s=$?; tmux kill-server; exit $s'` (or `make itest`). `history -c; history -s` doesn't work inside the test shell; send real commands.

## Decision
PICKED #4962 (bash CTRL-R Perl branch: the oldest history entry keeps a trailing "\n" because `$/ = "\n\t"` never chomps the last record, so it gets an empty continuation line and escapes de-dup). One-line fix `s/\n\z//` in shell/key-bindings.bash; new TestBash test fails on master (2 vs 1) and passes with the fix; all 5 bash ctrl_r tests pass. Claim: https://github.com/junegunn/fzf/issues/4962#issuecomment-7094366361 . Brief: /workspace/batch-2026-11-23-midday/fzf-4962.md.
