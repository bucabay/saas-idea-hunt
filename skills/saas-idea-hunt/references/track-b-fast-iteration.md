# Track B — the fast iteration loop

An alternative to the six-phase evidence hunt (Track A), contributed by u/ClawPulse in the same
thread:

> "Validate ideas quickly and iteratively. Talk to potential customers, run surveys, and test
> landing pages before building anything. Identify a clear pain point and build the simplest
> possible solution. Then get it in front of users and iterate based on feedback. It's all about
> finding product-market fit as fast as possible."

Where Track A spends a week accumulating evidence before it will name an opportunity, Track B
spends that week putting a cheap artefact in front of people and reading the reaction. Both end in
the same place — a one-feature MVP and a single channel — but they buy information differently.

## When to run Track B instead

- You already have a specific idea and a hypothesis about who buys it. Track A is for finding an
  idea; Track B is for pressure-testing one.
- You already have access to the buyer — you worked in the industry, or you have a list.
- Speed matters more than confidence: a competitor is moving, or a window is closing.
- The build is genuinely a few days, so testing by building is cheaper than testing by research.

Run Track A instead when you have no idea, no access to the buyer, or when the build is expensive,
regulated, or integration-heavy — there, being wrong is costly and the research is cheaper than
the iteration.

Running both is legitimate and often best: Track A in the background to keep the ledger filling,
Track B in the foreground on your leading hypothesis.

## The loop

One turn of the loop is one week. Stop when a turn produces no new information.

**1. State the hypothesis (30 min).** One sentence, falsifiable:
> `<buyer title>` at `<company type>` will pay `$<price>/month` to stop `<specific pain>`, which
> they currently handle by `<workaround>`.

Write it down before testing. An unwritten hypothesis is unfalsifiable by construction.

**2. Talk to customers (5-10 conversations).** Use the scripts and the commitment ladder in
`outreach.md` — Track B does not lower the evidence bar, it just reaches it faster. Ask about the
workaround, never about the idea.

**3. Survey, carefully (optional).** Surveys measure recall and opinion, not behaviour, so use them
only to *size* something the interviews already established, never to discover it. Ask what people
did last month, not what they would do. Keep it under 6 questions. Never ask "would you pay?".

**4. Landing page test (2-4 days).** One page: the pain in the buyer's own words as the headline,
three bullets, one price, one button. The button goes to a Stripe payment link or a $1 pilot hold
— not an email capture. Drive traffic from the interview list and one community. Judge on
paid-intent clicks. Visits and email signups are vanity here.

**5. Simplest possible solution (≤2 weeks).** Whatever the smallest artefact is that delivers the
outcome. Often not software: a spreadsheet you run manually, a Zap, a form plus your own labour.
Concierge delivery is a legitimate v1 and teaches more than code does.

**6. Ship it to real users and read the behaviour.** Instrument the one action that means the tool
worked. Then iterate: change one thing per turn so you can attribute the result.

## The two failure modes

**Iterating without a falsifiable hypothesis** is just drifting with extra steps. If you cannot
say what result would make you stop, the loop cannot end.

**Mistaking the loop for validation.** Fast iteration on an unbudgeted pain produces a
well-polished product nobody buys, faster. Track B still has to clear rung 4 on the commitment
ladder before you scale the build.

## Kill criteria

- Three full turns with no movement up the commitment ladder → the hypothesis is wrong, not the
  execution. Rewrite the hypothesis or switch to Track A.
- Landing page: 200+ targeted visitors, zero paid-intent clicks → the headline is not the buyer's
  pain. Change the headline once; if that fails too, change the hypothesis.
- Concierge v1 delivered manually to 5 users, none renew → stop. Do not automate a service nobody
  wants faster.

## Artefacts

Track B writes into the same workspace, so evidence carries across if you switch tracks:

```
research/<slug>/
  hypothesis.md    # the falsifiable sentence, versioned per turn
  validation.md    # same results log as Track A (references/outreach.md)
  landing.md       # headline variants, traffic sources, paid-intent clicks per variant
  loop-log.md      # one entry per turn: what changed, what happened, what it ruled out
  mvp.md           # templates/mvp-scope.md
```

`loop-log.md` is the point of the track. One entry per turn, three lines: what you changed, what
happened, what it ruled out. A loop that rules nothing out is not a loop.
