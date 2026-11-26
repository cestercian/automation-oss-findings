# reflex-dev/reflex

- Policy: CONTRIBUTING "AI-Assisted PRs" welcomes AI help, no disclosure checkbox. Requires human owner, passing pre-commit + tests, real assertions for every changed line, and addressing Greptile/Copilot bot feedback. No CLA seen. Issues get a Linear linkback bot comment (not an assignment).
- Layout: uv workspace, core code in packages/reflex-base/src/reflex_base. Changelog fragments in packages/reflex-base/news/+<issue>-<slug>.bugfix.md (towncrier).
- Commands: `uv sync`, `uv run ruff check .`, `uv run pyright <files>`, `uv run pytest tests/units -q`. On the box the full unit suite has 255 env failures on main (mostly tests/units/reflex_cli); compare against a main worktree.
- 2026-11-26 evening: PICKED #7996 (typing_extensions.TypedDict state vars untyped because `typing.is_typeddict` is False for them). Fix: import is_typeddict from typing_extensions in vars/object.py and utils/types.py. Tests in tests/units/vars/test_object.py and tests/units/utils/test_types.py.
- Busy repo: #7995 (generic TypedDict) had three competing PRs (#8019/#8021/#8022) within hours.
