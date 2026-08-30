# Source thread — r/SaaS, "my saas hit $9k/month..."

**URL:** https://www.reddit.com/r/SaaS/comments/1sai8o6/
**Author:** u/Emotional_Seat1092 · **322 points, 260 comments** (as of 2026-08-30)

## What the post claims

A founder at ~$9k MRR / ~700 paying users after 12 months describes the 30-day plan they would
follow if they started over:

| Days | Step |
|---|---|
| 1-3 | Skip brainstorming. Read 1-2 star reviews on G2 and Capterra in boring B2B categories. 200 reviews minimum before forming an opinion. |
| 4-7 | Cross-reference the top complaints on Reddit. Check Upwork for repetitive work companies pay freelancers to do. |
| 8-10 | DM 10 people who left those reviews or posts. 3 of 10 saying yes is enough. |
| 11-25 | Build the ugliest possible MVP. One feature. |
| 26-30 | Pick one channel and go hard. |

Stated anti-patterns: developer tools ("2 months, 4 paying users"), consumer apps, and going it
alone.

The organising claim, and the part that survives scrutiny best:

> "frustrated paying customers = validated demand"

## The thread's reception — read this before trusting the post

The **top comment (56 points)** calls it advertising:

> "Tired of this ad posted every single day ... Please no more ai advertisements disguised as
> reddit posts" — u/simon96

A reply (19 points) gives the specific tell:

> "It's like they used the prompt to keep all lowercase to seem genuine. There are paragraph
> breaks, all notations perfect, but not one uppercase char" — u/forsvinne

The post closes with two soft pitches — a consultant network and an unnamed tool that "scrapes
complaints from G2, capterra, reddit, and app stores." That is consistent with the criticism.

A dissenting commenter (6 points) makes the case for reading it anyway:

> "regardless of the product placement... the tips are kinda legit about how to start. Especially
> where to find ideas." — u/CaptainDivano

**Conclusion adopted:** treat the post as a hypothesis, not a case study. It earns its place only
because independent practitioners in the comments confirmed specific parts of it from their own
work. Where nobody confirmed it, it was either rewritten or dropped — see
[`what-we-rejected.md`](what-we-rejected.md).

## Comment-level findings that made it into the skill

### The job-posting signal — the single best addition

[Comment `ody10pc`](https://www.reddit.com/r/SaaS/comments/1sai8o6/comment/ody10pc/) —
u/Wise-Butterfly-6546, who reports running multiple B2B products across healthcare compliance,
infrastructure, and insurance, all originating from the same source: someone in a regulated
industry complaining their tool needed manual workarounds.

Two claims:

1. **The regulated-vertical pattern.** Per the commenter, the more boring and regulated the
   vertical, the higher the willingness to pay — nobody wants to build claims processing or
   HIPAA-compliant monitoring, which is why the margins hold.
2. **The hiring signal**, added explicitly as an improvement on the post's day 8-10 step:

   > "If a 50-person company is hiring a 'compliance data coordinator' to manually reconcile
   > reports between two systems, that's a six-figure SaaS waiting to be built."

**Why it's the strongest signal in the playbook:** a job posting for glue work is pain that has
been articulated, quantified, budgeted, and approved — and the hiring manager is a warm contact
who expects inbound about that post. The salary caps what the software is worth.

**Where it landed:** `references/mining-playbook.md` § Labor signals; the highest-weighted source
in Phase 2; scoring factor 3.

### Retention over acquisition

Comment `odvybe8` (9 points) — u/ToBeContinuedHermit:

> "at early stage, focus on learning velocity, not growth rate"

> "That's not a growth problem — it's a product problem wearing a growth costume."

Fix the leaky bucket before pouring water in. Talk to every user; understand every signup and
every churn.

**Where it landed:** Phase 7, which *gates* Phase 6 scale-up rather than following it.

### Cold DMs don't work at volume

Comment `odzc52v` (3 points) — u/Super-Young-8108, reporting an actual attempt:

> "I dmmed about 100 people on reddit to check out my new app and didn't get a single reply"

Follow-up from the same person: people get annoyed at even a slight product mention in a post.

This directly contradicts the post's day 8-10 step. It is a report of an event, so it outranks the
post's assertion.

**Where it landed:** cold Reddit DMs rank last of nine channels in `references/outreach.md`.

### Independent confirmation of Upwork

Comment `oe0y95y` (2 points) — u/Gullible_Leek_3467:

> "The upwork angle is underrated as hell... it's literally a live feed of 'I will pay money to
> solve this problem.'"

Two independent commenters confirming the labour-market signal is why Tier 1 of desk mode is built
around records of money that provably moved.

### The fast-iteration alternative

Comment `oe0r0h7` (2 points) — u/ClawPulse: validate quickly and iteratively — customer
conversations, surveys, landing page tests, simplest possible solution, then iterate on feedback.

Kept as a **separate track** rather than merged, because it answers a different question. Track A
finds an idea; Track B pressure-tests one you already have.

**Where it landed:** `references/track-b-fast-iteration.md`.

### Scale ceiling

Comment `old3pni` (3 points) — u/JabezTadesse: "Problem with B2B is scale."

Fair and under-discussed. A narrow vertical caps out. Forced into an explicit up-front choice
rather than left as a surprise.

**Where it landed:** `references/why-boring-b2b.md` § The scale caveat; § 3 of the desk dossier.

### Churn at the $10k wall

Comment `odyleu2` (2 points) — u/KindAssignment1034 notes that founders typically hit a wall around
$10k MRR where acquisition is solved but retention leaks, and you end up replacing churned users
instead of growing. Reinforces Phase 7.

## Secondary thread

r/SEO_Marketing_Offers, "What SaaS products are actually trending to build in 2026?" (11 points,
24 comments) supplied the niche list now in `references/candidate-niches.md`, along with the
distribution-as-moat and gaps-close-fast arguments in `references/principles.md`.

The niche list is deliberately framed as **hypotheses, tiered by fit** — not opportunities. Two
entries (AEO tooling, short-form video generators) are marked "treat with suspicion" because they
fail the skill's own scoring criteria before research starts.
