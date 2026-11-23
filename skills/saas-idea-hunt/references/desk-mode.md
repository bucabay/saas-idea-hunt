# Desk mode — how far online data alone gets you

Question this file answers: can problem investigation and discovery be run entirely off online
data, with no human contact?

**Discovery: yes, and further than most people attempt.** Phases 0-3 are already desk research.
This file deepens them from "read reviews and Reddit" to a full public-record dossier that
quantifies the buyer population, the money already moving, and the incumbent's inability to close
the gap.

**Validation: no.** Not as a matter of rigour, but of availability. Phase 4 asks whether a
*specific named person* will move budget. No public dataset contains that. Desk mode ends with a
falsifiable, quantified, priced hypothesis and a list of 100 reachable humans — which is maybe 80%
of the work — and then hands you the 20% that only exists in a conversation.

Never report a desk-mode dossier as validation. Report it as what it is: the strongest possible
hypothesis, with the irreducible unknowns named.

---

## The rule that decides whether a source counts

**Revealed behaviour is admissible. Stated preference is not.**

| Admissible — records what someone did | Inadmissible — records what someone said or might do |
|---|---|
| A company hired a person to do it manually | A survey says 68% are "interested" |
| A contract was awarded at $X | A trend report says the category is growing |
| A freelancer was paid $Y to do it | A LinkedIn poll |
| A customer churned and said why | An analyst's TAM estimate |
| 400 people upvoted a feature request | A synthetic persona's answer |
| An incumbent's pricing page charges $Z | A VC thesis |

Every row in the ledger must be the left column. If a source only produces the right column, it can
inform a hypothesis but cannot score in `scoring.md`.

---

## Source catalogue

Phases 1-2 cover review sites, communities, Upwork, and job boards. These go beyond that. Check
what each actually exposes before relying on it — availability and pricing change.

### Tier 1 — money that provably moved

**Public procurement records.** The most underused source in this entire playbook. Governments
publish what they bought, from whom, for how much, on what terms.
- `USASpending.gov` — US federal contract awards, searchable by NAICS and PSC codes. You can read
  the actual dollar amount an agency paid for a category of software.
- `SAM.gov` — federal solicitations and RFPs. A buyer writing an RFP has written your requirements
  document for you, unprompted, in their own vocabulary.
- `TED` (Tenders Electronic Daily) — EU public procurement.
- State, county, municipal, and school-district procurement portals — enormously varied, mostly
  free, and where the boring verticals live. GovSpend and GovWin aggregate this commercially.

Why it is Tier 1: an awarded contract is a completed purchase with a price attached. An RFP is a
budgeted intention with published requirements. Both beat any interview.

**Feature request boards with vote counts.** Canny, UserVoice, ProductBoard public boards,
Salesforce IdeaExchange, Atlassian's Jira issue tracker, GitHub issues on the incumbent's repos,
public Trello roadmaps. These are ranked, dated, vote-counted demand — a queue of things customers
asked for and did not get. Read the ones open for 3+ years with high vote counts and an official
"not planned" or silence: that is a gap the incumbent has decided not to close.

**Freelance and BPO pricing.** Upwork completed jobs, Fiverr gig pricing, and the service pages of
offshore BPOs and bookkeeping/RCM/compliance agencies. An agency with a landing page for "we handle
your X reconciliation" has productised the pain and published the price.

**Incumbent pricing pages, past and present.** Current pricing sets the willingness-to-pay anchor.
Then run them through the **Wayback Machine**: five years of a pricing page and a feature list
shows you exactly what an incumbent has *not* shipped despite time and revenue. That is your
"why hasn't the incumbent shipped it" answer, with dates.

### Tier 2 — sizing the population and the spend

**Census County Business Patterns.** Establishment counts by NAICS industry code crossed with
employment size band. This turns "50-200 person P&C carriers" from a hand-wave into a number, which
turns the scale ceiling in the opportunity brief from a guess into arithmetic.

**BLS Occupational Employment and Wage Statistics.** How many people hold a job title nationally
and what they are paid, by metro. If 41,000 people work as <the glue-work role> at a median $58k,
the labour spend on your problem is a defensible number.

**O\*NET.** Task-level breakdowns of occupations — literally a list of the discrete tasks a job
consists of. Read the task list for the role your product would displace; it is a free, structured,
government-maintained description of the workflow you are trying to automate.

**Industry association member directories and conference materials.** Member directories are your
buyer list. Conference agendas tell you what the industry is anxious about this year — a session
titled "Surviving the 2026 reporting change" is a dated, industry-endorsed pain signal. Sponsor
lists tell you who already sells to these people, i.e. your partner and competitive landscape.

**Search demand.** Google Keyword Planner, Google Trends, Ahrefs/Semrush. The queries that matter
are not "<category> software" — they are `how to <task> manually`, `<system A> <system B> sync`,
`<incumbent> alternative`, `<incumbent> export to excel`. Volume on a how-to-do-it-by-hand query is
people looking for a workaround because no product exists.

### Tier 3 — the incumbent's own disclosures

**SEC filings and earnings calls** for public incumbents. 10-K risk factors, segment revenue,
retention language, and the "we intend to invest in" section of an earnings call are the closest
thing to a public roadmap. If the incumbent tells investors they are focusing elsewhere, your
factor-7 score improves and you can cite the date.

**The incumbent's own job postings.** What they are hiring for is what they are building. If they
just hired six engineers for the exact thing you found, stop.

**Changelogs, release notes, status pages, and public roadmaps.** Cadence tells you how fast they
ship. Status page incident history tells you whether reliability is itself the wedge.

**Support and community forums** — Salesforce Trailblazer, QuickBooks Community, Zendesk and
Atlassian communities, vendor subreddits. High-volume, dated, searchable, and far more specific
than review sites because people are describing a broken thing in the moment.

### Tier 4 — ecosystem tells

**Marketplace listings and review counts.** Salesforce AppExchange, QuickBooks Apps, Shopify,
Chrome Web Store, Zapier and Make template galleries. A thriving ecosystem of point solutions,
connectors, and templates around one workflow means the workflow is broken and unbuilt. Chrome
extensions publish install counts; other stores expose review counts as a rough proxy — check what
each actually shows rather than assuming.

**Template marketplaces.** Excel/Sheets template sellers, Notion template sales, Airtable
universe. People pay for a spreadsheet template because software does not exist. That is a product
brief with a revenue history.

**Glassdoor and Indeed reviews filtered to the job title** you would displace. People describing
the worst part of their day, in detail, unprompted, with no product in the frame.

**Funding data** (Crunchbase and similar) for adjacent startups — read as competitive density and
timing, not as validation. Heavy recent funding in your exact wedge is a warning, not a signal.

### The one community corpus with a real search API

Almost every community resists programmatic search. Reddit answers automated requests with `403`
and its search is not reachable from the agent's tools, so Reddit mining stays manual. Hacker News
is the exception and is worth knowing in detail, because the Algolia index covers every story
**and every comment**, full text, with second-level timestamps, points, and comment counts.

That matters because the best lines are in comments, not posts. A comment that a bookkeeper is
paid monthly to reconcile two systems is a spend record sitting at reply 14 of a three-year-old
thread. A `site:` search will not find it; the API will, and it will also show whether anyone
replied to agree.

Use it for:

- **Workaround admissions** — `manually`, `spreadsheet`, `had to hire`, `two systems`, `export to`.
- **Incumbent threads** — launches, outages, "we switched off X", each dated.
- **Who is hiring** — the monthly threads are a searchable labour sample, but a developer-heavy
  one: a supplement to Indeed and LinkedIn for tech-adjacent roles, weak evidence in regulated
  non-tech verticals.
- **Currency checks** — a date range settles whether the gap still exists, which a review site
  cannot do.

What it cannot do: points are attention, not budget. An 800-point rant is a hypothesis. Cite the
comment that describes a transaction and keep the popularity as context. Exact query patterns are
in `mining-playbook.md` § Triangulation; the API's parameters and limits are recorded in
`sources.md`.

---

## What synthetic personas are and are not for

You can have the agent role-play "an operations manager at a mid-size freight brokerage" and interview
it. Be clear about what that is.

**Legitimate uses — rehearsal and hypothesis generation:**
- Practising the interview so you do not burn a real conversation learning to ask cleanly.
- Pressure-testing your question set: does it survive a stubborn or defensive respondent?
- Red-teaming your own brief — "argue that this opportunity is worthless" produces better
  objections than you will generate alone.
- Generating a *list of things to go verify*, explicitly labelled as unverified.

**Illegitimate — and the failure mode is specific:** a language model asked to play a customer
produces the *statistically typical* answer, fluently and confidently. It will agree that your
problem is a problem, because posts and articles about that problem are what it learned from. It
cannot tell you what this buyer actually does, has no budget, and will never surprise you. Its
answers are the right-hand column of the admissibility table by construction.

**The firewall: no synthetic output ever enters `ledger.md`.** Keep it in a separate
`rehearsal.md`, marked as such, and never cite it in an opportunity brief.

---

## The desk-mode run

Phases 0-3, deepened. Output is `templates/desk-dossier.md`.

1. **Frame** (Phase 0, unchanged) — categories, buyer job title, size band.
2. **Mine** (Phase 1) — review sites and app stores, 150+ rows.
3. **Triangulate** (Phase 2) — communities, Upwork, job boards. Hacker News comments via Algolia
   are the one community corpus you can query directly, by date and thread (`mining-playbook.md`).
4. **Public record sweep** (new) — Tier 1 sources. Procurement, feature-request boards with vote
   counts, freelance/BPO pricing, incumbent pricing history via Wayback.
5. **Quantify** (new) — Tier 2. Establishment counts × price anchor = ceiling. Occupation counts ×
   wages = labour spend on the problem today. Write the arithmetic down so it can be attacked.
6. **Incumbent read** (new) — Tier 3. Filings, job postings, changelog cadence, forum volume.
   Produce a dated, evidenced answer to "why hasn't this been shipped".
7. **Score** (Phase 3) — the 8-factor rubric, now with real numbers behind factors 1, 3, 4, 7, 8.
8. **Assemble the buyer list** (new) — 100 named, reachable humans from job posters, review
   authors, RFP contacts, association directories, conference attendee and speaker lists. This is
   the deliverable that makes Phase 4 executable in a day rather than a week.
9. **Name the irreducible unknowns** (new, mandatory) — see below.

Realistic effort: two to four focused days. Every step is public data.

## Irreducible unknowns — the mandatory closing section

Desk mode must end by stating what it could not establish. At minimum:

- **Will this specific buyer pay?** No public record answers this. Only rung 4-5 does.
- **Is the pain top-two or seventh?** Complaints are visible; *relative* priority is not. Public
  data over-represents anything annoying enough to write about, which is not the same as important
  enough to buy. Customer Problem Stack Ranking in `interview-guide.md` is the fix, and it needs
  humans.
- **Who actually signs?** Job posts and reviews reveal the person in pain. In B2B that is rarely
  the person with budget.
- **What does the workaround really cost?** You can bound it from salaries and freelance rates. The
  true number, including the error rate and the downstream cleanup, lives in one screen share.
- **Is the complaint current?** Reviews and forum threads are dated; product state moves faster.
  Verify the gap still exists in the current version before building.
- **Survivorship in the sources.** You are reading people who bothered to post. Silent satisfied
  majorities and silently churned customers are both invisible.

## The honest ceiling

Two limits worth stating plainly.

**Public data is public.** Desk research is cheap now and everyone has the same tools. An
opportunity derived entirely from searchable sources is, by construction, one that many people can
derive this month — which is exactly the "gaps get filled within weeks" problem in
`principles.md`. The defensible edge from desk mode is *speed and synthesis depth*, not exclusivity.
The genuinely differentiated inputs remain the hard-to-search ones: procurement portals, private
communities, association directories, and conversations.

**Desk mode is the cheapest way to kill an idea, not to confirm one.** Its highest-value output is
a well-evidenced *no* delivered on day three instead of month four. Treat a strong dossier as
permission to go spend two weeks talking to people — never as permission to start building.
