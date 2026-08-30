# What was rejected, and why

The skill is not a faithful transcription of its sources. These are the deliberate departures.

## From the source post

### "3 out of 10 saying yes is enough"

> "message them directly... 'would you pay $30-50/month?' ... 3 out of 10 saying yes is enough."

**Rejected.** This is stated preference — the least predictive signal available, and the exact
failure mode The Mom Test is written about. A yes to a hypothetical costs the respondent nothing,
and politeness alone produces roughly that hit rate.

**Replaced with** the five-rung commitment ladder in `references/outreach.md`. The post's bar is
rung 1. The skill's bar is three people at rung 4+ (named budget line and approver, or an LOI),
from 60-100 approaches.

### Cold DMs as the primary validation channel

**Rejected as the primary channel.** Contradicted inside the same thread by a founder reporting 0
replies from ~100 Reddit DMs (comment `odzc52v`), and volume DMing gets accounts banned.

**Replaced with** nine channels ranked by yield, DMs last, weighted toward warm paths, paid
recruiting, and people who published something specific you can quote back.

### "Find the missing feature"

**Rejected as sufficient.** A missing feature is usually a feature request, not a company. If it is
easy and valuable, the incumbent ships it the quarter after you validate it for them.

**Replaced with** two mandatory written answers in every opportunity brief: *why hasn't the
incumbent shipped this* (with "they're lazy" scoring zero) and *why can't this be cloned in six
weeks*. Both are scored — factor 7 in `references/scoring.md`.

### The implied timeline

The post presents 30 days from zero to launched. **Softened.** The phases keep their time-boxes
but validation is 1-2 weeks of human-executed conversation that cannot be compressed by working
harder, and Phase 7 has no end date. What the skill kept is the *discipline* of time-boxing, and
it added kill criteria the post lacks — every phase can now end in "stop", which the original
never allows.

### The post's own framing as a case study

**Rejected.** Treated throughout as a hypothesis. The thread's top comment reads it as AI-generated
promotion for an idea-mining tool, and the post closes with two soft pitches. Its claims are used
only where an independent practitioner confirmed them. See [`source-thread.md`](source-thread.md).

## From the wider threads

### Surveys as a discovery tool

Several sources recommend surveys early. **Demoted.** Surveys measure recall and opinion, not
behaviour. In the skill they may only *size* something interviews already established — never
discover it — must ask what people did last month rather than what they would do, and may never
ask "would you pay".

Customer Problem Stack Ranking is the exception, and only because it ranks *problems against each
other* rather than rating an idea.

### Email-capture landing pages

**Rejected.** An email signup is rung 1 in a costume. Every landing-page test in the skill routes
the button to a Stripe payment link or a $1 pilot hold. Judge on paid-intent clicks; visits and
signups are vanity here.

### The trending-niche lists

Kept, but **demoted to hypotheses and tiered**, in `references/candidate-niches.md`. Two entries
are explicitly marked "treat with suspicion":

- **AEO / SEO tooling for SaaS** — the underlying insight (distribution is the moat) is sound and
  drives Phase 6, but as a product category it is saturated and its buyer is other founders, which
  is an anti-pattern in `references/why-boring-b2b.md`.
- **Short-form video generators** — the supporting argument was "I see a lot of ads for this",
  which is evidence of a crowded market, not an open one.

Anything on a public trend list is being read by everyone else the same day. The list gets you to
the starting line and confers no other advantage.

### Building for developers, and for founders

**Kept as an anti-pattern**, and extended. The post warns off developer tools from experience (2
months, 4 paying users). The skill generalises it: any product whose buyer is another builder or
founder inherits a small market, no budget, and high churn.

Noted without snark: the source thread is itself an instance — a post to an audience of founders,
pitching tools to founders.

## What was added that no source provided

- **The revealed-vs-stated admissibility rule** (operating rule 2) — a ledger row must record what
  someone *did*. This is the spine of the whole skill and is implicit in the sources at best.
- **Desk mode** — procurement records, feature-request boards with vote counts, Census
  establishment counts, BLS occupation data, incumbent filings and Wayback pricing history. No
  source mentioned public procurement or labour statistics; both are stronger evidence than
  anything the original threads used.
- **The synthetic-persona firewall** — LLM-simulated customers are useful for rehearsal and
  inadmissible as evidence, because a model asked to play a customer returns the statistically
  typical answer, confidently, and will never surprise you.
- **Kill criteria on every phase.** The sources describe what to do when things work. The most
  valuable output of this workflow is a well-evidenced *no* on day three.
