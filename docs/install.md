# Install

Three ways, depending on how you want it to live.

## 1. Plugin (recommended — keeps it updatable)

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

## 2. Plain skill, available everywhere

```sh
git clone https://github.com/bucabay/saas-idea-hunt.git
ln -s "$PWD/saas-idea-hunt/skills/saas-idea-hunt" ~/.claude/skills/saas-idea-hunt
```

A symlink means `git pull` updates the skill in place. Copy it instead if you'd rather pin it:

```sh
cp -R saas-idea-hunt/skills/saas-idea-hunt ~/.claude/skills/
```

## 3. Single project only

```sh
mkdir -p .claude/skills
cp -R /path/to/saas-idea-hunt/skills/saas-idea-hunt .claude/skills/
```

Useful when you want the research workspace (`research/<slug>/`) to live inside one repo.

## Verify

Start Claude Code and run `/saas-idea-hunt`, or just say "help me find a saas idea". If the skill
loaded, it will ask you for categories and a buyer job title before doing anything else.

## Using it without Claude Code

Everything here is plain Markdown. The method works read-by-a-human:

- [`docs/method.md`](method.md) — the workflow in narrative form
- [`skills/saas-idea-hunt/references/`](../skills/saas-idea-hunt/references/) — the playbooks
- [`skills/saas-idea-hunt/templates/`](../skills/saas-idea-hunt/templates/) — fill these in by hand

The templates are the actual deliverables. The skill just fills them in faster.
