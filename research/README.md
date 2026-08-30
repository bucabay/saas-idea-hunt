# Research

The skill in `skills/saas-idea-hunt/` is a synthesis, not an invention. This directory is the
audit trail: what was read, what was taken, what was rejected, and what remains unverified.

The skill's own operating rule is "evidence or silence." That rule applies to the skill itself.

| File | Contents |
|---|---|
| [`source-thread.md`](source-thread.md) | The r/SaaS post the workflow is built on, its reception, and the comment-level findings |
| [`customer-conversations.md`](customer-conversations.md) | Research into the "how do you actually talk to customers" question |
| [`what-we-rejected.md`](what-we-rejected.md) | Advice from the sources that was deliberately not adopted, with reasons |

## How the research was gathered

Reddit blocks automated fetching (`403` on the JSON endpoints, and the search API is not reachable
from the web-search tool). Threads were read through a logged-in browser session and parsed from
Reddit's own JSON endpoints, same-origin. Scores and comment counts are as of **2026-08-30**, and
they move.

Web sources were found with ordinary search and fetched directly.

## Evidential standing

Reddit threads are practitioner anecdote. They were weighted by:

1. Whether an independent commenter confirmed the claim from their own experience
2. Upvotes and comment volume, as weak proxies for community agreement
3. Whether the claim is about **what someone did** rather than what they think works

Point 3 does most of the work. "I DM'd 100 people and got 0 replies" is worth more than a
1,000-upvote listicle, because it is a report of an event rather than a theory.

Nothing here is a controlled study. The skill's reply-rate figures in
`skills/saas-idea-hunt/references/outreach.md` are explicitly flagged as directional: the *ordering*
of channels is the reliable part, the percentages are not.
