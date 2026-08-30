# MVP scope — <opportunity name>

**Build window:** <start> → <end> (2 weeks max)
**Validated by:** <n> rung-4+ commitments, logged in `validation.md`

Do not start this document until the commitment ladder has cleared. A scope written before
validation is a wish list.

## The one thing

v1 does exactly this, for exactly this person:

> <Buyer> can <single outcome> in <time> without <the workaround>.

## Not building

Be specific and absolute. Each line is a thing you will be tempted by in week two.

- No dashboard
- No onboarding flow or product tour
- No admin panel or settings screen
- No team management, roles, or permissions
- No billing portal — Stripe payment link only
- No integrations beyond the single one the wedge requires
- No mobile app
- No <opportunity-specific temptation>

## Pricing, live from day one

`principles.md` § Charge from day one. No card-free trial.

- Price: $<X>/month, or $<Y> for a <n>-week paid pilot
- Card captured at signup: yes
- Payment mechanism: Stripe payment link / Checkout
- Who approves this spend at the customer: <title>

## Time-to-first-value

Charging early raises the onboarding bar. Write the path down before building.

- First value = <the specific moment the buyer sees the outcome>
- Target: under <n> minutes from signup, in one session
- What has to be true for that: <data import, one credential, one setting>
- Manual concierge steps you will personally do for the first 10 customers:

## Instrumentation

One activation event, one retention event. Nothing else yet.

- Activation event: <the action that means it worked>
- Weekly retention event: <the action that means they still need it>

## Kill criteria — written before code

| Checkpoint | Date | Target | If missed |
|---|---|---|---|
| Signups from the validated list | | <n> | |
| Activation rate (reached first value) | | <n>% | |
| Paid conversion | | <n> of <n> pilots | |
| Week-4 retention | | <n>% | |

Missing a target means stop and diagnose, not "push harder on marketing".

## Post-launch order of work

1. Fix activation for the users who did not reach first value.
2. Interview every churned account (`principles.md` § Retention before acquisition).
3. Only then, Phase 6 — one channel, thirty days.
