# The method

The short version: **stop guessing what people want, and make the ones who already pay for a bad
solution prove it with money.**

Longer version below. This is the narrative form of
[`skills/saas-idea-hunt/SKILL.md`](../skills/saas-idea-hunt/SKILL.md), for reading rather than
executing.

## The one rule everything else hangs off

> A piece of evidence must record what someone **did** — hired, paid, filed, churned, upvoted.
> Not what they said they might do.

| Admissible | Inadmissible |
|---|---|
| A company hired someone to do it manually | A survey says 68% are "interested" |
| A contract was awarded at $X | An analyst's TAM estimate |
| A freelancer was paid $Y to do it | A LinkedIn poll |
| A customer churned and said why | A trend report |
| 400 people upvoted a feature request | A model-generated persona's answer |

Almost every bad product decision traces back to treating something in the right column as though
it were in the left.

## Phase 0 — Frame

Pick 3-5 **boring, regulated, unglamorous B2B** categories. Field service, claims processing,
compliance reporting, freight, practice management, municipal permitting, lab systems, trucking.

Refuse: developer tools (they build their own before paying), consumer apps (they churn in weeks),
and anything whose buyer is another founder (small market, no budget, everyone's selling to
everyone).

Weight heavily toward categories where you have firsthand experience or direct buyer access. It is
worth more than fifty reviews.

You must be able to name the job title of the person who suffers. If you can't, drop the category.

## Phase 1 — Mine complaints

150+ rows minimum before forming an opinion. 1-2 star reviews on G2, Capterra, TrustRadius, app
stores — and ecosystem marketplaces (Salesforce AppExchange, QuickBooks Apps, Shopify), which are
the underrated source because a 2-star connector review names the exact two systems that don't
talk.

Hunt the workaround language specifically: `workaround`, `export to excel`, `manually`,
`had to hire`, `every month we`. Those quantify the pain. `doesn't have` only locates it.

Every row: URL, date, reviewer role, company size, incumbent tool, a short verbatim quote, and any
spend signal.

**Kill: under 40 rows in 90 minutes → the category is too thin or too well served.**

## Phase 2 — Triangulate, and price the pain

A complaint on a review site might be one angry admin. It becomes a candidate at **three
independent source types**:

1. **Review sites** — the gap, in buyers' words
2. **Communities** — industry subreddits, trade forums, vertical Slacks. Not r/SaaS. Hacker News
   is the one community searchable in full through its Algolia API, comments included, which is
   where the workarounds are described. Look for 20+ comment threads where people agree with each
   other
3. **The labour market** — the strongest of the three

The labour signal deserves its own paragraph. Search job boards for **roles that shouldn't exist**:
"data coordinator", "reconciliation specialist", "reporting analyst" at 20-200 person companies,
where the description is *move data between two systems by hand*.

> "If a 50-person company is hiring a 'compliance data coordinator' to manually reconcile reports
> between two systems, that's a six-figure SaaS waiting to be built."
> — [u/Wise-Butterfly-6546](https://www.reddit.com/r/SaaS/comments/1sai8o6/comment/ody10pc/)

A salaried human doing integration work is pain that is articulated, quantified, budgeted, and
approved. The salary caps what the software is worth. The hiring manager is your warmest contact.
Same logic applies to recurring Upwork jobs and to BPO service pages.

## Phase 3 — Score, honestly

Eight factors, 0-5 each: frequency, triangulation, payment evidence, workaround cost, wedge
narrowness, buyer reachability, incumbent-response risk, regulatory moat.

Two questions every brief must answer in writing:

- **Why hasn't the incumbent shipped this?** "They're lazy" scores zero. Acceptable: it conflicts
  with their data model, cannibalises a revenue line, breaks a partner agreement, serves a
  different buyer, or they publicly declined it.
- **Why can't this be cloned in six weeks?** If the honest answer is "it can be", that's a park.

**Under 24/40 → the evidence doesn't support building. Say so.**

## Phase 4 — Validation

The part everyone skips, and the part that decides everything.

**Getting the meeting.** Nine channels, ranked by yield — warm intros, paid interview recruiting,
hiring the freelancer who does the task by hand, job posters, review authors, public community
participation, LinkedIn by title, cold email, and cold DMs *last*. Reply rates vary by roughly 50x
across that list.

**Not wasting it.** Talk about their life, not your idea. Ask about specific past events, not
hypotheticals. Talk less. Don't mention what you're building for the first fifteen minutes.

**The commitment ladder** — the only scoring that matters:

| Rung | Signal | Worth |
|---|---|---|
| 1 | "Yes I'd pay $X/mo" | ~nothing |
| 2 | Attends a 20-min call | weak |
| 3 | Sends their actual workaround file | real |
| 4 | Names a budget line and approver | strong |
| 5 | Pre-pays or puts a card on file | proof |

**Three people at rung 4+, from 60-100 approaches.** In B2B, interview users and buyers
separately — the person in pain rarely controls budget, which is exactly what rung 4 tests.

**Kill: 60 approaches, zero rung 4 → the pain is real but unbudgeted. That's a finding.**

## Phase 5 — One feature, priced

Two weeks. One feature. Write the *not building* list explicitly — no dashboard, no onboarding
flow, no admin panel, no settings, no billing portal.

Ugly is fine. Charge from day one; a card-free trial measures curiosity. But charging early raises
the onboarding bar, so write down time-to-first-value and the concierge steps you'll do by hand for
the first ten customers — otherwise you'll read your own onboarding failure as a market rejection.

Kill criteria go in writing *before* the first line of code.

## Phase 6 — One channel, thirty days

Six channels at once teaches nothing about any of them. Default to the community where you found
the complaints, because you arrive with research to share rather than a pitch. No product name and
no link in a first public reply.

## Phase 7 — Retention gates growth

Don't scale a channel into a leaky bucket. Before increasing acquisition: know your churn, interview
**every** churned account, and fix activation.

> "That's not a growth problem — it's a product problem wearing a growth costume."
> — u/ToBeContinuedHermit

At early stage, optimise for learning velocity, not growth rate.

## Two variants

**Track B — fast iteration.** For an idea you already have and a buyer you can already reach.
Falsifiable hypothesis → 5-10 conversations → landing page with a payment button → simplest
possible solution (often not software) → read the behaviour → change one thing. Same evidence bar,
faster loop. [Details](../skills/saas-idea-hunt/references/track-b-fast-iteration.md).

**Desk mode.** How far public data alone gets you: procurement awards and RFPs, feature-request
boards with vote counts, Census establishment counts, BLS occupation data, incumbent SEC filings,
Wayback pricing history. Two to four days produces a quantified dossier and 100 named reachable
buyers. It ends where Phase 4 begins — **desk mode never authorises building, it authorises
conversations**. [Details](../skills/saas-idea-hunt/references/desk-mode.md).

## The honest caveats

- **Public gaps close fast.** Desk research is cheap and everyone has the same tools. An
  opportunity derived entirely from searchable sources is one many people can derive this month.
  The edge is speed and synthesis depth, not exclusivity — and the hard-to-search sources
  (procurement portals, private communities, association directories, conversations) are where
  the real advantage lives.
- **AI compresses the build, not the understanding.** Cheaper building means more competitors at
  feature parity, faster. Spend the time it gave you back on customers.
- **Complaint volume ≠ priority.** Every source here shows you that a pain is *visible*. None shows
  whether it's top-two or seventh on that buyer's list. Customer Problem Stack Ranking is the fix,
  and it needs humans.
- **The best output is a fast no.** Treat a strong dossier as permission to spend two weeks talking
  to people. Never as permission to start building.
