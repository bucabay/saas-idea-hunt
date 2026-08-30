# Research — how do you actually talk to customers?

Every validation guide says "talk to customers" and almost none say *how you get a stranger in a
specific job to spend twenty minutes with you*. This is what the research turned up.

Two separate problems, usually conflated:

1. **Getting the meeting** → `skills/saas-idea-hunt/references/outreach.md`
2. **Not wasting it** → `skills/saas-idea-hunt/references/interview-guide.md`

## Getting the meeting

### Channels differ by roughly 50x, and the popular ones are the worst

The ranking in `outreach.md` puts warm intros, paid recruiting, and paid freelancer hours at the
top and cold Reddit DMs at the bottom. Two channels were surfaced by the research and are missing
from essentially every founder guide:

**Paid interview recruiting.** Platforms — User Interviews, Respondent, Wynter, Askable — let you
post screener criteria and buy scheduled conversations with a specific B2B role, typically within
a week. Roughly a $30-60 platform fee plus a $50-150 participant incentive for ordinary roles,
more for senior or hard-to-reach titles. *Verify current pricing; it moves.*

Ten interviews for $1-2k against two months of building the wrong thing is cheap. The caveat is
real, though: paid participants are professionally agreeable and some are serial respondents. They
teach you the workflow; they are not evidence of demand. The skill caps them at rung 3 of the
commitment ladder regardless of enthusiasm.

**Hiring the freelancer who already does the task by hand.** On Upwork or Fiverr, book an hour with
someone who does the exact manual work you want to automate and have them screen-share their
process. They're being paid so they show up and they're candid; they've done it for many clients so
they know what breaks; and they'll tell you their rate, which prices the pain. ~$50-100.

### Offer a trade — the most transferable tactic found

[r/microsaas — "The exact steps I took to validate my idea before building (now at $7,300/mo)"](https://www.reddit.com/r/microsaas/comments/1kvxsdb/)
(128 points). The founder posted in r/SaaS and r/indiehackers asking founders to answer a few
questions, offering feedback on whatever they were building in return. That produced 8-10
conversations. Their own note on why it worked:

> "The key part here was offering them something in return for their time."

Reciprocity beats persuasion. "Answer three questions and I'll send you what the other twenty
people said" costs nothing and converts far better than asking for a favour — and the follow-
through is what later turns a research list into a distribution channel.

### Go where they already are, and give before asking

[r/ycombinator — "YC Founders, How Did You Get Your First REAL Users?"](https://www.reddit.com/r/ycombinator/comments/1j4basa/)
(122 points). The top answer (58 points): find where target users already discuss the problem
(Reddit, Discord, niche forums, Slack groups) and **engage authentically before pitching**; do cold
outreach only with something useful attached; build in public. A reply adds the thing founders most
consistently skip — personal network and second-degree intros.

[r/SaaS — "I Spent Months Helping SaaS Founders Get Their First 10 Users"](https://www.reddit.com/r/SaaS/comments/1j8y7ao/)
(290 points, 120 comments): search for people already asking "how do I solve <pain point>", mine
Product Hunt and Indie Hackers comment sections for people engaging with similar products, and DM
*before* launching — if nobody wants it, don't build it.

[Talk to Users Before You Build](https://abiraja.substack.com/p/talk-to-users-before-you-build):
cold email offering to pay for time; LinkedIn search, connect with a short note, then message;
landing page + Calendly with a gift-card incentive. Also the point that even a slideshow v1 beats
approaching people at the "just an idea" stage.

### Respect for time is a recruiting tactic, not a courtesy

[Dovetail — recruiting hard-to-reach B2B participants](https://dovetail.com/customer-research/how-to-recruit-hard-to-reach-b2b-participants-for-user-interviews/):
asking a busy executive for 60 minutes is a non-starter, and you get better data in 30 minutes from
an engaged participant than 60 from a checked-out one. Hence "15 minutes, three questions" in the
scripts.

[User Interviews — The Six Cs of B2B recruitment](https://www.userinterviews.com/blog/better-b2b-research-recruitment)
and [User Interview Exchange](https://www.userinterviewexchange.com/blog/how-to-recruit-participants-for-b2b-user-interviews):
screen hard. Talking to the wrong people produces worthless data — define role, company type,
purchasing authority, and problem experience *before* recruiting.

### Users and buyers are different people

[Linden Innovation — customer discovery interviews in B2B](https://lindeninnovation.com/customer-discovery-interviews-b2b/):
interview them **separately**. In B2B the person experiencing the pain rarely controls budget, so
you need users confirming the problem and buyers confirming willingness to pay.

This is why the commitment ladder has a distinct rung 4 ("names a budget line and an approver")
rather than treating enthusiasm as a single axis. It also explains a common false positive: ten
delighted users and no sale.

## Not wasting the meeting

### The Mom Test

Rob Fitzpatrick's three rules, via
[Sachin Rekhi's primer](https://www.sachinrekhi.com/p/the-mom-test-rob-fitzpatrick),
[UXtweak](https://blog.uxtweak.com/the-mom-test/) and
[ReadingRaphics](https://readingraphics.com/book-summary-the-mom-test/):

1. Talk about their life, not your idea
2. Ask about specific past events, not future hypotheticals
3. Talk less — they should have ~80% of the airtime

The load-bearing mechanism: people cannot lie about what they actually did, only about what they
might do. "Would you buy a product that does X?" asks an optimistic person for an opinion about a
situation that does not exist. "Walk me through the last time this happened" asks for a fact.

The skill adds one rule the sources imply but don't state: **don't mention your idea for the first
15 minutes.** Once they know what you're building, every answer afterwards is shaded encouraging.

### Customer Problem Stack Ranking — the highest-leverage finding

[r/startups — "How Stripe validates ideas for new products"](https://www.reddit.com/r/startups/comments/mmwphz/)
(870 points, 95 comments). Written by a Techstars community leader and global facilitator who had
run 100+ customer discovery interviews. They describe a method attributed to Shreyas Doshi and used
at Stripe, and report the result of trying it on their own startup:

> "the value proposition that we spent 7 months of discovery reseach crafting came dead last"

and

> "We learned more in 2 hours using this stack ranking approach than we did in 100+ customer
> discovery interviews."

The method, in five steps:

1. Ask a **broad** question about the whole activity, not your problem: "what is the most
   frustrating part of <activity>?"
2. **Convert your idea into a problem statement** — the write-up cites The Mom Test on why rating
   an *idea* invites flattery, while ranking a *problem* against other problems does not.
3. Collect the field of problems people named, plus yours, phrased in the same voice.
4. Have a fresh set of target customers rank them by frustration.
5. Read the **position**, not the score. Seventh of eight is a mild inconvenience however many
   people agree it's annoying.

**Why this matters more than it first appears:** interviews establish that a pain is *real*.
Nothing in review mining, forum reading, or one-on-one interviews establishes that it is
*important relative to everything else on that buyer's plate*. This is the specific blind spot in
the entire complaint-mining approach the skill is built on, and stack ranking is the only cheap
fix found.

**Where it landed:** `references/interview-guide.md`, and named as an irreducible unknown in
`templates/desk-dossier.md` — public data shows visibility, never relative priority.

## Open questions

- Reply-rate figures are assembled from practitioner reports, not measured. Ordering is
  trustworthy; percentages are not. A real experiment across channels for one ICP would be worth
  more than all of the above.
- Nothing found quantifies how much paid-recruiting agreeableness inflates positive signal. The
  rung-3 cap is a judgement call, not a measured correction.
