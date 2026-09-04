---
name: capacity-economics
description: Work out what actually drives profit in a business that delivers service through finite capacity — sessions, seats, slots, appointments, installs. Separates the price lever from the utilisation lever, and finds the entitlement-versus-consumption gap. Use for any subscription or package business where a human or a slot delivers the value.
---

# Capacity economics

In a software business, one more customer costs almost nothing to serve. In a
business that delivers through people or slots, one more customer costs a real
amount, and **the profit lever is usually how full the slot is, not what you
charge for it.**

This skill exists because the obvious response to thin margins is to raise
price, and in capacity businesses that is often the third-best move.

## Establish the delivery unit first

Before any arithmetic, name the unit that costs money to deliver: a class, a
session, a visit, a route, an install. Then answer:

- What does one delivery unit cost, regardless of how many customers are in it?
- How many customers can it hold?
- How many are actually in it?

The third number is the one nobody has. Get it before continuing.

## The two levers, and why utilisation usually wins

If the delivery unit costs roughly the same whether it holds two customers or
five, then contribution per unit scales with occupancy while cost stays flat.
Moving occupancy from 2 to 4 can do more for margin than any tolerable price
increase, and **it does not risk conversion the way a price rise does.**

Compare them explicitly:

```
contribution per unit = (customers_in_unit × revenue_per_customer_per_unit)
                        − cost_to_deliver_unit
```

Run it at current occupancy and at target occupancy. Then run the price
increase that would produce the same result. Show both. In most capacity
businesses the occupancy path is smaller in percentage terms than the price path
— and that comparison is the whole point of the skill.

**This is not universal.** Where delivery cost scales per customer rather than
per unit — one-to-one coaching, per-seat licences with real per-seat cost — the
lever genuinely is price or cost, and this skill should say so rather than force
the occupancy story.

## The entitlement-versus-consumption gap

Customers on a package rarely consume all of it. If someone buys eight sessions
a month and attends five, your cost base reflects five while your revenue
reflects eight.

**This is worth finding, and it is dangerous to rely on.** Two rules:

1. **Measure it.** Consumption rate = units actually delivered ÷ units the
   customer was entitled to. Segment it; light and heavy users behave nothing
   alike.
2. **Never build the plan on it.** A business whose margin depends on customers
   not using what they paid for has a margin that disappears the moment
   engagement improves — and improving engagement is usually what retention work
   does. Model the downside at full consumption and say whether the business
   survives it.

If the answer is that it does not survive full consumption, that is the finding.
Lead with it.

## Your payment rail can cap your price

Recurring-payment methods often carry a per-mandate ceiling, a maximum
auto-debit amount, or step-up rules above a threshold. If the price you want
sits above that ceiling, the customer has to re-authorise manually, and
manual re-authorisation is where recurring revenue goes to die.

**Check the ceiling on the rail most of your customers actually use before
designing tiers.** This constraint is invisible in a pricing spreadsheet and
decisive in production. It varies by country and by method, so verify it for
your market rather than assuming the figure from someone else's.

Where the ceiling binds, the usual answer is to sell a different duration rather
than a different price point — a shorter commitment that fits under the ceiling
often beats a cheaper monthly plan.

## Sequencing with acquisition

If contribution per customer is thin because units run half-empty, spending more
on acquisition buys more thin customers. **Fix occupancy first, then scale.**
The exception is when occupancy is low precisely because you lack volume in a
given slot or location — then acquisition targeted at that slot *is* the
occupancy fix, and should be aimed there specifically rather than run broad.

## When to refuse

- The delivery unit has not been named, or its cost is unknown
- Occupancy is not measured and cannot be estimated from delivery records
- Fewer than a handful of delivery periods observed — occupancy is seasonal and
  a single week will mislead
- Delivery cost is genuinely per-customer, not per-unit. Say so and route to
  `unit-economics` instead

## Output

Cost per delivery unit, current occupancy, target occupancy, contribution per
unit at both, and the equivalent price rise that would match the occupancy gain.
Then the consumption rate with the full-consumption downside stated. Then one
line naming the lever to pull first, and the number that would change the
answer.

See also `unit-economics` for the marginal-versus-blended question, and
`pricing-decisions` before moving price.
