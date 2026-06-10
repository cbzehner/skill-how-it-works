> **Moved:** this skill now lives in [cbzehner/skills](https://github.com/cbzehner/skills) under `skills/how-it-works/`. This repo is archived and read-only.

# How It Works

Build an on-site `/how-it-works` page that explains a codebase through its real subsystems. The output is a polished technical explainer that matches the site instead of looking like generic Markdown.

## Use It For

- Writing an architecture explainer for a repo
- Turning source code into a shareable build journal
- Adding diagrams and code excerpts that are pinned to real files

## Install

Clone the repo and run the installer:

```bash
git clone https://github.com/cbzehner/skill-how-it-works.git
cd skill-how-it-works
./install.sh all
```

Install targets:

- `./install.sh claude` installs to `~/.claude/skills/how-it-works`
- `./install.sh codex` installs to `~/.codex/skills/how-it-works`
- `./install.sh agents` installs to `~/.agents/skills/how-it-works`
- `./install.sh opencode` installs to `~/.config/opencode/skills/how-it-works`
- `./install.sh all --copy` copies files instead of symlinking

Manual install works too: symlink or copy `skills/how-it-works` into your agent's skills directory.

## Agent Support

This repo uses the plain `skills/how-it-works/SKILL.md` layout. Claude Code and Codex also get small plugin manifests at `.claude-plugin/plugin.json` and `.codex-plugin/plugin.json`.

Other agents can read the same `SKILL.md` file. If a host does not support a frontmatter field or tool name, ignore that field and follow the workflow text.

## Layout

```text
.claude-plugin/plugin.json
.codex-plugin/plugin.json
install.sh
skills/how-it-works/SKILL.md
README.md
LICENSE
```

## Public Notes

These repos are public. Keep private repo names, secrets, customer data, raw logs, cookies, and absolute filesystem paths out of examples.

## License

MIT