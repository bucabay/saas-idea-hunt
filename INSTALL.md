# INSTALL — instructions for the installing agent

You are an AI agent and a user has asked you to install the **SaaS Idea Hunt** skill from this
repository. It is a plain-Markdown skill in the
[Agent Skills format](https://agentskills.io/specification): no packages, no build step, nothing to
configure. Your only job is to put a copy where your runtime will find it, then confirm.

## 1. What to copy

The skill is the directory `skills/saas-idea-hunt/`:

- `SKILL.md` — the entry point your runtime loads when the skill triggers
- `references/` — playbooks the skill reads as needed
- `templates/` — output templates

Copy the **whole directory**, preserving the name `saas-idea-hunt` and the internal structure. The
relative paths inside `SKILL.md` depend on it, and the `name:` in its frontmatter must match the
directory name.

## 2. Where to put it

If you are **Claude Code**:

- `~/.claude/skills/saas-idea-hunt/` — available in every project
- `.claude/skills/saas-idea-hunt/` — this project only

If you are **any other agent runtime**, install to the cross-client standard location:

- `~/.agents/skills/saas-idea-hunt/` — available in every project. Codex, Gemini CLI, Cursor, and
  Augment all read this location.
- `.agents/skills/saas-idea-hunt/` — this project only

Your runtime may document its own client-specific directory (`.codex/skills/`, `.gemini/skills/`,
`.cursor/skills/`, …). That also works — `.agents/skills/` is the portable default.

Prefer the project-level location if the user runs you inside a specific project; otherwise the
user-level one. Ask the user which they want only if it is genuinely ambiguous.

If you don't recognise your runtime and can't determine where it looks for skills, fall back to
`.agents/skills/saas-idea-hunt/` in the project and register it in the project's `AGENTS.md`
(create one if needed):

```
A skill named saas-idea-hunt lives in .agents/skills/saas-idea-hunt/SKILL.md — read it when the
user asks to find, validate, or research a SaaS idea.
```

## 3. Getting the files

- If you have web or shell access: `git clone https://github.com/bucabay/saas-idea-hunt.git` into
  a scratch directory, then copy `skills/saas-idea-hunt/` out of it.
- If you cannot fetch the repository yourself, ask the user to clone it and give you the local
  path, then copy from there.

## 4. Verify and confirm

After copying, read the installed `SKILL.md` and check the frontmatter `name:` is `saas-idea-hunt`.
Then tell the user:

> Installed the `saas-idea-hunt` skill at <path>. Say "help me find a saas idea" to run it.

Do not run the skill's phases as part of the install unless the user asked you to.

## 5. Updates

The skill changes over time. To update, repeat this install (clone fresh and copy over the old
directory), or `git pull` an existing clone and copy again. Skills are not auto-updating by
design — the copy you made is yours to pin.
