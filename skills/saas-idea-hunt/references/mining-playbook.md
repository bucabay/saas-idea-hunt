# Mining playbook

Exact sources and queries. Run searches with WebSearch, read individual pages with WebFetch, and
query documented public APIs directly (Hacker News is the one that matters). Human pace, public
pages only. If a source blocks automated reads, hand the query to the user to run in their browser
and paste back — do not route around the block.

## Complaint-signal phrases

These are the ctrl+F strings that separate a real gap from a generic 1-star rant. Use them
verbatim inside site-scoped searches, and inside the page once you have it open.

**Missing capability**
`doesn't have` · `does not support` · `no way to` · `can't` · `wish it could` · `missing feature`
· `feature request` · `been asking for` · `still no`

**Workaround cost (the highest-value signal — quantifies the pain)**
`workaround` · `export to excel` · `copy and paste` · `manually` · `we built a script` ·
`had to hire` · `full time person` · `takes hours` · `every month we`

**Switching intent (buyer is in market right now)**
`switching to` · `moved to` · `evaluating` · `looking for alternatives` · `cancelled our`

**Integration gap (usually the cleanest wedge)**
`doesn't integrate` · `no API` · `no Zapier` · `two systems` · `re-enter` · `sync`

## § Review sites

Rotate through these. Each has different reviewer populations.

| Source | Notes |
|---|---|
| G2 | Best B2B coverage; filter to 1-2 stars, sort by most recent |
| Capterra / GetApp / Software Advice | Same Gartner data pool; SMB-skewed, more candid |
| TrustRadius | Longer-form, more enterprise, best workaround detail |
| Apple App Store / Google Play | Field-worker complaints for anything with a mobile app |
| Chrome Web Store | Reveals what people bolt onto the incumbent |
| Salesforce AppExchange / QuickBooks Apps / Shopify App Store | Marketplace reviews name the exact workflow gap |
| Trustpilot | Weaker for B2B, good for billing/support pain |

Search patterns:

```
site:g2.com "<category>" "doesn't have"
site:capterra.com "<incumbent tool>" review "workaround"
site:trustradius.com "<incumbent tool>" "dislike"
"<incumbent tool>" reviews "switching to" 2025
"<incumbent tool>" "export to excel" "every month"
```

Ecosystem marketplaces are the underrated ones. A 2-star review on an AppExchange connector names
the exact two systems that don't talk and the exact record type that breaks.

## § Triangulation

A complaint that only lives on a review site may be one angry admin. Confirm it in the wild.

**Reddit** — search the top Phase 1 complaint phrases, not the product name:
```
site:reddit.com "<workflow>" "manually"
site:reddit.com/r/<industry sub> "<incumbent>" alternative
```
Industry subs beat r/SaaS: r/msp, r/sysadmin, r/accounting, r/dentistry, r/CommercialRealEstate,
r/Construction, r/freight, r/nonprofit, r/humanresources, r/InsuranceAgent, r/legaladvice
practitioners' subs, r/talesfromtechsupport.

Signal to look for: 20+ comments, and commenters **agreeing with each other** rather than the
thread being one person venting. Disagreement threads are also useful — they mark a real tradeoff.

**Hacker News — query the Algolia API, not `site:` search.** A site-scoped web search mostly
returns story titles. The admissions worth logging — "we do this in a spreadsheet", "I pay a VA for
it" — are in comments. The public API indexes every story and comment, needs no key, and takes
exact date ranges. Two endpoints, same parameters:

```
https://hn.algolia.com/api/v1/search          # relevance, then points, then comment count
https://hn.algolia.com/api/v1/search_by_date  # newest first
```

| Parameter | Use |
|---|---|
| `query=` | terms; ranked, **not** phrase-matched — a hit may contain only one of them |
| `tags=story` · `comment` · `ask_hn` · `show_hn` | what to search |
| `tags=author_whoishiring` | the monthly "Who is hiring" threads |
| `tags=comment,story_<id>` | every comment in one thread |
| `numericFilters=created_at_i>...` | Unix timestamp — the recency gate |
| `numericFilters=points>50,num_comments>20` | **stories only**; comments have neither field |
| `hitsPerPage=50&page=1` | paging; 10,000 requests/hour per IP |

Encode `>` as `%3E` in a URL, as below. Queries to start from, with `<workflow>`, `<incumbent>`,
and `<task>` substituted:

```
# the workaround admission, last 12 months
.../search?query=<workflow>+manually&tags=comment&numericFilters=created_at_i%3E1767225600&hitsPerPage=50

# threads worth reading end to end
.../search?query=<incumbent>+alternative&tags=story&numericFilters=num_comments%3E20

# "what do you use for X" — the genre is pre-qualified demand
.../search?query=what+do+you+use+for+<task>&tags=ask_hn

# then every comment in the best thread, paging with &page=1,2,…
.../search?tags=comment,story_<id>&hitsPerPage=100
```

`1767225600` is 2026-01-01; compute your own cutoff rather than reusing it. `author_whoishiring`
returns the job-seeker threads as well as the hiring ones, so filter on the title. Quote from
`comment_text`, link the item as `news.ycombinator.com/item?id=<objectID>`, and keep the ≤25-word
limit. Because multi-word matching is lenient, confirm the phrase is actually present before
quoting — a hit for "reconcile spreadsheet" may contain both words pages apart.

Two limits. Points and comment counts are attention, not spend: they corroborate a complaint and
never substitute for the labour signal. And HN skews developer, infra, and startup — a null result
there is not proof the pain is absent, only that it lives in another community. For regulated
non-tech verticals, go to the trade forum.

**Industry forums and Slack/Discord:** every vertical has one (Bogleheads for advisors,
DentalTown, TruckersReport, Spiceworks for IT). These are where the specific, unsearchable
complaints live.

**Facebook Groups and LinkedIn:** search the incumbent's name plus "frustrated" or "alternative".

A complaint repeated on Reddit and HN is still **one** source type. Three independent types means
review site + community + labour market, not three communities.

## § Labor signals

The strongest evidence tier: someone is already paying money — not opinion — to solve this.

**Upwork / Fiverr / Freelancer**
Filter to completed jobs in the category. Look for the same job posted repeatedly by different
companies, or on a recurring schedule by one company.
```
site:upwork.com "<workflow>" data entry
site:upwork.com "<system A>" "<system B>" sync
```
Record: fee, hours, recurrence. That is the annual spend the software displaces.

**Job boards — roles that should not exist**
Search Indeed / LinkedIn / Wellfound for titles that describe glue work:
`data coordinator` · `reconciliation specialist` · `reporting analyst` · `operations associate` ·
`billing coordinator` · `compliance coordinator` · `intake specialist`

Then read the JD for the tell: "reconcile reports between X and Y", "manually enter", "maintain
the master spreadsheet", "prepare weekly reports from multiple systems".

```
site:linkedin.com/jobs "reconcile" "spreadsheet" "<industry>"
site:indeed.com "data coordinator" "<industry>" "two systems"
```

A 50-person company paying $65k for someone to move rows between two systems has already approved
the budget and already named the problem. Log the salary — it caps what the software is worth, and
it names the buyer (the hiring manager on that post is your Phase 4 contact).

**Ancillary labor signals:** BPO/offshore agency service pages ("we handle your X reconciliation"),
Zapier/Make template galleries with high install counts, and Excel/Sheets template marketplaces.
Anything with a thriving template ecosystem is an unbuilt product.

## Ledger discipline

Every find becomes one row, immediately, in `ledger.md`. Rows added later from memory are
worthless — the URL and date are the whole point. Assign each row a stable ID (`L001`, `L002`) so
opportunity briefs can cite them.
