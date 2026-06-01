# How It Works

Build a polished, on-site /how-it-works page that explains a codebase's micro-systems in the site's own visual style. Use when the user wants an architecture explainer, a HN-shareable writeup, a build-journal page, or to "explain how X works" as a standalone artifact. Produces prose with real code excerpts (pinned to a SHA), hand-authored SVG diagrams in the site's palette, a sticky TOC, and de-slopified writing. Falls back to a single self-contained HTML file when no static site is detected.

## Skill

This repository packages one portable agent skill:

- `how-it-works` - Build a polished, on-site /how-it-works page that explains a codebase's micro-systems in the site's own visual style. Use when the user wants an architecture explainer, a HN-shareable writeup, a build-journal page, or to "explain how X works" as a standalone artifact. Produces prose with real code excerpts (pinned to a SHA), hand-authored SVG diagrams in the site's palette, a sticky TOC, and de-slopified writing. Falls back to a single self-contained HTML file when no static site is detected.

The canonical skill body lives at `skills/how-it-works/SKILL.md`. Keep behavior changes there; keep this README focused on installation and packaging.

## Install

Clone the repository, then run the installer:

```bash
git clone https://github.com/cbzehner/skill-how-it-works.git
cd skill-how-it-works
./install.sh all
```

Install targets:

- `./install.sh claude` -> `~/.claude/skills/how-it-works`
- `./install.sh codex` -> `~/.codex/skills/how-it-works`
- `./install.sh agents` -> `~/.agents/skills/how-it-works` for generic agent harnesses such as Pi/Hermes-style setups
- `./install.sh opencode` -> `~/.config/opencode/skills/how-it-works`
- `./install.sh all --copy` copies files instead of symlinking

Manual installation is just a symlink or copy from `skills/how-it-works` into your agent's skills directory.

## Compatibility

This repo uses the common `skills/<name>/SKILL.md` layout so agents that understand file-based skills can load it directly. Host-specific metadata is included where useful:

- Claude Code: `.claude-plugin/plugin.json` and direct `~/.claude/skills` install
- Codex CLI: `.codex-plugin/plugin.json` with `skills: "./skills/"` and direct `~/.codex/skills` install
- Other agents: direct install to the agent's skills directory; unsupported frontmatter fields can be ignored

Some skills mention optional host tools such as `Task`, `Agent`, `Skill`, MCP tools, or browser automation CLIs. On hosts that do not provide those tools, adapt to equivalent local capabilities and keep the same workflow intent.

## Public Safety

These repositories are public. Do not commit organization-specific instructions, private repository names, secrets, tokens, cookies, raw session logs, customer data, or machine-local paths. Use environment variables and generic paths in examples.

## Repository Layout

```text
.claude-plugin/plugin.json   # Claude plugin metadata
.codex-plugin/plugin.json    # Codex plugin metadata
install.sh                   # Symlink/copy installer for common agent skill dirs
skills/how-it-works/SKILL.md
README.md
LICENSE
```

## License

MIT
