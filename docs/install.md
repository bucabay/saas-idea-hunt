# Install

The skill is plain Markdown in the [Agent Skills format](https://agentskills.io/specification) —
the same files work in Claude Code, Codex, Gemini CLI, Cursor, Augment, and other runtimes. Four
ways to install, from easiest down.

## 1. With a prompt (recommended — any agent)

Paste into any AI agent with file access:

```
install the skill at https://github.com/bucabay/saas-idea-hunt
```

The agent reads [`INSTALL.md`](../INSTALL.md), copies the skill into that agent's skills
directory, and confirms. Then say:

```
help me find a saas idea
```

If your agent can't fetch URLs, clone the repo first and paste the local path instead:

```sh
git clone https://github.com/bucabay/saas-idea-hunt.git
```

then tell the agent `install the skill from /path/to/saas-idea-hunt`.

## 2. Claude Code plugin (updatable, version-pinnable)

Inside Claude Code:

```
/plugin marketplace add bucabay/saas-idea-hunt
/plugin install saas-idea-hunt@bucabay-skills
```

Or from a terminal:

```sh
claude plugin marketplace add bucabay/saas-idea-hunt
claude plugin install saas-idea-hunt@bucabay-skills
```

Pin to a tag if you want a fixed version:

```sh
claude plugin marketplace add bucabay/saas-idea-hunt@v0.1.0
```

## 3. Manual, per runtime

Clone once, then copy the skill directory to wherever your runtime looks for skills:

```sh
git clone https://github.com/bucabay/saas-idea-hunt.git
```

| Runtime | Copy to (all projects) | Copy to (one project) |
|---|---|---|
| Claude Code | `~/.claude/skills/` | `.claude/skills/` |
| Codex · Gemini CLI · Cursor · Augment · other Agent Skills runtimes | `~/.agents/skills/` | `.agents/skills/` |
| Client-specific alternates | `~/.codex/skills/` · `~/.gemini/skills/` · `~/.cursor/skills/` | `.codex/skills/` · `.gemini/skills/` · `.cursor/skills/` |

```sh
# Claude Code, all projects
cp -R saas-idea-hunt/skills/saas-idea-hunt ~/.claude/skills/

# Any Agent Skills runtime, all projects
cp -R saas-idea-hunt/skills/saas-idea-hunt ~/.agents/skills/

# One project only
mkdir -p .agents/skills && cp -R saas-idea-hunt/skills/saas-idea-hunt .agents/skills/
```

Updates: `git pull`, then copy over the old directory. (Or symlink instead of copying —
`ln -s "$PWD/saas-idea-hunt/skills/saas-idea-hunt" ~/.claude/skills/` — so `git pull` updates the
skill in place.)

## Verify

Start your agent and say "help me find a saas idea". If the skill loaded, it will ask you for
categories and a buyer job title before doing anything else.

## Using it without an agent

Everything here is plain Markdown. The method works read-by-a-human:

- [`docs/method.md`](method.md) — the workflow in narrative form
- [`skills/saas-idea-hunt/references/`](../skills/saas-idea-hunt/references/) — the playbooks
- [`skills/saas-idea-hunt/templates/`](../skills/saas-idea-hunt/templates/) — fill these in by hand

The templates are the actual deliverables. The skill just fills them in faster.
