# Sources

Where the claims in this skill come from. Reddit threads are practitioner anecdote, not evidence —
weighted by upvotes, comment volume, and whether independent commenters confirmed the claim.

## Primary — the source thread

- r/SaaS, ["my saas hit $9k/month. if i had to start over..."](https://www.reddit.com/r/SaaS/comments/1sai8o6/)
  — 322 pts, 260 comments. The six-phase structure, the G2/Capterra 1-2 star filter, the Upwork
  angle, the ugly-MVP and one-channel rules.
  **Caveat:** the top comment (56 pts) reads the post as AI-generated promotion for an idea-mining
  tool, and a reply notes the uniform lowercase styling. The method survives because practitioners
  in the comments independently confirmed parts of it — but treat the post as a hypothesis, not
  a case study.
  - Comment [ody10pc](https://www.reddit.com/r/SaaS/comments/1sai8o6/comment/ody10pc/) —
    u/Wise-Butterfly-6546. The job-posting signal ("a 50-person company hiring a 'compliance data
    coordinator'... is a six-figure SaaS waiting to be built") and the regulated-vertical
    willingness-to-pay pattern. Now the highest-weighted source in Phase 2.
  - Comment odvybe8 — u/ToBeContinuedHermit. "Learning velocity, not growth rate";
    "a product problem wearing a growth costume". Basis of Phase 7.
  - Comment odzc52v — u/Super-Young-8108. Reported 0 replies from ~100 Reddit DMs. Why cold DMs
    rank last in `outreach.md`.
  - Comment oe0y95y — u/Gullible_Leek_3467. Independent confirmation of the Upwork signal.
  - Comment oe0r0h7 — u/ClawPulse. The fast iteration loop; basis of
    `track-b-fast-iteration.md`.

## Interview method

- Rob Fitzpatrick, *The Mom Test* — the three rules. Summaries:
  [Sachin Rekhi's primer](https://www.sachinrekhi.com/p/the-mom-test-rob-fitzpatrick),
  [UXtweak](https://blog.uxtweak.com/the-mom-test/),
  [ReadingRaphics](https://readingraphics.com/book-summary-the-mom-test/).
  The load-bearing idea: people cannot lie about what they actually did, only about what they
  might do. Anchor every question in a specific past event.
- r/startups, ["How Stripe validates ideas for new products"](https://www.reddit.com/r/startups/comments/mmwphz/)
  — 870 pts, 95 comments. Customer Problem Stack Ranking, attributed to Shreyas Doshi. Author is a
  Techstars facilitator who ran 100+ discovery interviews and reports learning more in two hours of
  stack ranking; his seven-month value proposition ranked last. Source for
  `interview-guide.md` § Customer Problem Stack Ranking.

## Recruiting participants

- [User Interviews — The Six Cs of Better B2B Research Recruitment](https://www.userinterviews.com/blog/better-b2b-research-recruitment)
- [Dovetail — How to recruit hard-to-reach B2B participants](https://dovetail.com/customer-research/how-to-recruit-hard-to-reach-b2b-participants-for-user-interviews/)
  — respect for time: better data in 30 minutes with an engaged participant than 60 with a
  disengaged one; a 60-minute ask of a busy executive is a non-starter.
- [Linden Innovation — Customer discovery interviews in B2B](https://lindeninnovation.com/customer-discovery-interviews-b2b/)
  — interview **users and buyers separately**. In B2B the person in pain rarely controls budget,
  so you need both: users confirming the problem, buyers confirming willingness to pay. This is
  why the commitment ladder has a distinct rung 4 (named budget + approver).
- [User Interview Exchange — How to recruit participants for B2B user interviews](https://www.userinterviewexchange.com/blog/how-to-recruit-participants-for-b2b-user-interviews)
- Screening: talking to the wrong people produces worthless data. Define role, company type,
  purchasing authority, and problem experience before you recruit.

## Reaching people — practitioner reports

- r/ycombinator, ["YC Founders, How Did You Get Your First REAL Users?"](https://www.reddit.com/r/ycombinator/comments/1j4basa/)
  — 122 pts. Top answer (58 pts): go where users already talk about the problem and engage before
  pitching; cold outreach only with something useful attached; build in public; and personal
  network / second-degree intros, which the thread notes founders consistently skip.
- r/microsaas, ["The exact steps I took to validate my idea before building (now at $7,300/mo)"](https://www.reddit.com/r/microsaas/comments/1kvxsdb/)
  — 128 pts. **Offer a trade.** Posted in r/SaaS and r/indiehackers asking founders to answer
  questions in exchange for feedback on what they were building; got 8-10 conversations. Source
  for `interview-guide.md` § Offer a trade.
- r/SaaS, ["I Spent Months Helping SaaS Founders Get Their First 10 Users"](https://www.reddit.com/r/SaaS/comments/1j8y7ao/)
  — 290 pts, 120 comments. Find people already complaining; search for "how do I solve <pain
  point>"; mine Product Hunt and Indie Hackers comment sections for people engaging with similar
  products; DM before launching.
- [Talk to Users Before You Build — abiraja.substack.com](https://abiraja.substack.com/p/talk-to-users-before-you-build)
  — cold email offering to pay for time; LinkedIn search + connect + short note; landing page with
  a Calendly link and a gift-card incentive; and the point that having even a slideshow v1 beats
  approaching people at the "just an idea" stage.

## Tooling

- Hacker News Search API (Algolia) — [API documentation](https://hn.algolia.com/api) and the
  [hn-search source](https://github.com/algolia/hn-search). Verified **2026-11-23**:
  `/api/v1/search` (relevance, then points, then comments) and `/api/v1/search_by_date` (newest
  first); tag filters `story`, `comment`, `poll`, `pollopt`, `show_hn`, `ask_hn`, `front_page`,
  `author_<user>`, `story_<id>`, with tags ANDed by default and ORed inside parentheses; numeric
  filters on `created_at_i`, `points`, `num_comments`; `page` and `hitsPerPage`; 10,000 requests
  per hour per IP. Two consequences worth carrying into the playbook: `points` and `num_comments`
  are story attributes, so combining them with `tags=comment` returns zero hits, and relevance is
  Algolia's lenient matching rather than phrase search, so a hit may match only one term.

## Not verified

Reply-rate figures in `outreach.md` are directional orders of magnitude assembled from practitioner
reports, not measured data. The *ordering* of channels is the reliable part; the percentages are
not. Paid-recruiting platform pricing changes — check current rates before budgeting.
