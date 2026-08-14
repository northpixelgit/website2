# Provenance

Vendored from [nextlevelbuilder/ui-ux-pro-max-skill](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill).

- Upstream commit: `a38d04c3d5c298c851dbe5e6ee1965ee3de42cb5` (2026-08-14)
- Plugin version: 2.13.0
- License: MIT (see `LICENSE`)
- Source path: `.claude/skills/ui-ux-pro-max/`

Only the `ui-ux-pro-max` skill was installed. The upstream repository also ships
`ui-styling`, `design`, `design-system`, `brand`, `slides`, and `banner-design`,
which are not vendored here.

## Local modification

Upstream ships this skill as part of a Claude Code *plugin*, so `SKILL.md` invoked
the search script through `${CLAUDE_PLUGIN_ROOT}`. It is installed here as a plain
project skill, where that variable is not set, so the 11 invocation examples were
rewritten to the project-root-relative path:

    ${CLAUDE_PLUGIN_ROOT}/.claude/skills/ui-ux-pro-max/scripts/search.py
    -> .claude/skills/ui-ux-pro-max/scripts/search.py

The sentence introducing those examples was reworded to match. Nothing else was
changed; `data/`, `scripts/`, and `references/` are byte-identical to upstream.

## Updating

Re-clone upstream, copy `.claude/skills/ui-ux-pro-max/` over this directory, then
reapply the path rewrite above.
