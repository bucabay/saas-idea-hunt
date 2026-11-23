# SaaS Idea Hunt

An **agent skill** for finding and validating SaaS opportunities from evidence rather than
brainstorming.

Mines complaints from review sites, industry communities, and the labour market. Scores them
against an eight-factor rubric. Then drives validation to a **paid commitment** before a line of
code gets written — and tells you to stop when the evidence doesn't support building.

Works in any agent that loads skills: Claude Code, Codex, Gemini CLI, Cursor, Augment, and others
following the [Agent Skills format](https://agentskills.io/specification).

## Install — one prompt

Paste into any AI agent with file access:

```
install the skill at https://github.com/bucabay/saas-idea-hunt
```

The agent reads [`INSTALL.md`](INSTALL.md) and drops the skill into that agent's skills directory.
That's the whole install — it's plain Markdown, the same files for every runtime.

Then just say:

```
help me find a saas idea
```

If your agent can't fetch URLs itself, clone the repo and give it the path — the instructions
cover that too.

### Prefer a command line?

Claude Code plugin (updatable, version-pinnable):

```
/plugin marketplace add bucabay/saas-idea-hunt
/plugin install saas-idea-hunt@bucabay-skills
```

Manual installs for every runtime, per-project installs, and using the method without an agent:
[`docs/install.md`](docs/install.md).

## The one rule

> Evidence must record what someone **did** — hired, paid, filed, churned, upvoted. Not what they
> said they might do.

| Admissible | Inadmissible |
|---|---|
| A company hired someone to do it manually | A survey says 68% are "interested" |
| A contract was awarded at $X | An analyst's TAM estimate |
| A freelancer was paid $Y to do it | A LinkedIn poll |
| A customer churned and said why | A model-generated persona's answer |

Almost every bad product decision traces back to treating the right column as though it were the
left.

## What it actually does

**Phases 0-3 — find it.** Pick boring, regulated B2B categories. Mine 150+ complaint rows from 1-2
star reviews. Confirm each in three independent source types — review site, community, and the
labour market. Communities are searched for the specific complaint, not the product; Hacker News is
queried through Algolia's API, which reaches the comments where the workarounds actually get
described. Score the clusters out of 40.

The labour-market signal is the one most people miss. Job postings for **roles that shouldn't
exist** — "reconciliation specialist", "data coordinator" at a 50-person company — are pain that's
already articulated, quantified, budgeted, and approved. The salary caps what the software is
worth, and the hiring manager is your warmest contact.

**Phase 4 — validate it.** Nine outreach channels ranked by yield (reply rates vary ~50x, and the
popular ones are the worst). Then a five-rung commitment ladder where "yes I'd pay for that" scores
approximately nothing and the bar is three people naming a budget line, from 60-100 approaches.

**Phases 5-7 — build the smallest thing.** One feature, two weeks, priced from day one, with kill
criteria written before the first line of code. Then one channel for thirty days, gated behind
knowing your churn.

Full narrative walkthrough: [`docs/method.md`](docs/method.md).

## Why not just read the Reddit post it came from

Because the post is a hypothesis, not a case study — its own top comment reads it as AI-generated
promotion for an idea-mining tool. It earns its place only where independent practitioners in the
thread confirmed specific parts from their own work.

Three of its central claims are deliberately overridden:

| The post says | This skill says |
|---|---|
| "3 out of 10 saying yes is enough" | That's stated preference. Bar is 3 people at rung 4+ (named budget and approver) |
| Cold DM 10 people | Contradicted in its own thread — a founder reported 0 replies from 100 DMs. DMs rank last of nine channels |
| Find the missing feature | A missing feature is a feature request. Every brief must answer *why hasn't the incumbent shipped this* and *why can't this be cloned in six weeks* |

Every departure is documented with reasons in
[`research/what-we-rejected.md`](research/what-we-rejected.md).

## Two variants

**Track B — fast iteration.** For an idea you already have and a buyer you can already reach.
Falsifiable hypothesis → conversations → landing page with a payment button → simplest possible
solution → read the behaviour. Same evidence bar, faster loop.

**Desk mode.** How far public data alone gets you: procurement awards and RFPs, feature-request
boards with vote counts, Census establishment counts, BLS occupation data, SEC filings, Wayback
pricing history. Two to four days produces a quantified dossier and 100 named reachable buyers.

It stops where Phase 4 begins — not out of caution, but because no public dataset records whether
a named buyer will move budget. **Desk mode never authorises building. It authorises
conversations.**

## Layout

```
skills/saas-idea-hunt/
  SKILL.md                      phases 0-7, operating rules, track selection
  references/
    principles.md               the doctrine — tiebreaker for ambiguous calls
    mining-playbook.md          exact queries and sources per phase
    scoring.md                  8-factor rubric, 40 points, verdict bands
    outreach.md                 getting the meeting — channels by yield, scripts, ladder
    interview-guide.md          running the call — Mom Test, question bank, stack ranking
    why-boring-b2b.md           category selection, anti-patterns, scale ceiling
    candidate-niches.md         tiered hypothesis list for a cold start
    desk-mode.md                how far public data gets you, and where it stops
    track-b-fast-iteration.md   the fast landing-page/interview loop
    sources.md                  every claim's origin, unverified parts flagged
  templates/
    evidence-ledger.md          every complaint, one row each
    opportunity-brief.md        scored cluster with why-now and cloneability
    mvp-scope.md                one feature, priced, with kill criteria
    desk-dossier.md             the public-data dossier + irreducible unknowns

INSTALL.md  instructions for the installing agent (the prompt install)
AGENTS.md   one pointer for agents that browse the repo
docs/       method.md (narrative walkthrough), install.md
research/   the audit trail — sources, findings, and what was rejected
```

Output lands in `research/<slug>/` inside whatever project you run it from.

## Provenance

Synthesised from [r/SaaS — "my saas hit $9k/month..."](https://www.reddit.com/r/SaaS/comments/1sai8o6/)
and its 260-comment thread, plus r/startups, r/ycombinator, r/microsaas, r/SEO_Marketing_Offers,
Rob Fitzpatrick's *The Mom Test*, and B2B research-recruitment literature.

The [`research/`](research/) directory is the audit trail: what was read, what was taken, what was
rejected, and what remains unverified. Reply-rate figures are explicitly flagged as directional —
the *ordering* of channels is the reliable part, the percentages are not.

Contributions welcome, especially: measured reply rates by channel for a defined ICP, procurement
and public-record sources outside the US, and vertical-specific mining queries. Same standard
applies to contributions as to the skill — evidence of what someone did, with a link and a date.

## License

MIT — see [LICENSE](LICENSE).
