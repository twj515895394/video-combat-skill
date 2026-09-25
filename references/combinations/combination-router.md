# Combination Pattern Router

Combination references store **causal action grammar**, not fixed move lists.

Load only when the task needs help composing a continuous exchange.

| Need | Route |
|---|---|
| attacker keeps pressure after hit/miss/block | `pressure-chains.md` |
| defender turns defense into offense | `counter-conversions.md` |
| striking collapses into clinch/throw | `clinch-throw-transitions.md` |
| fight repeatedly changes between long/mid/close range | `range-conversions.md` |
| failed action / landing / stumble must become next beat | `recovery-failure-chains.md` |
| grounded wuxia uses pillars/rails/steps/height changes | `wuxia-spatial-chains.md` |

## Combination grammar format

A useful pattern must contain:

`trigger state -> action -> defender response -> changed state -> next opportunity`

Never store:
- “jab-cross-hook-low kick” without explaining why each next action is available,
- a fixed movie choreography that can only be copied literally,
- style-incompatible actions without constraints.

## Style precedence

Base style decides whether a pattern is appropriate.

Examples:
- Boxing may use pressure-chains and counter-conversions.
- Sanda may use range-conversions + clinch-throw-transitions.
- BJJ mostly uses positional transition grammar instead of striking chains.
- Grounded wuxia may use wuxia-spatial-chains after the base style remains valid.

## Load budget

Normally load at most **one** combination file for a short 5-15 second generation task.
Load two only if the fight deliberately changes domains, e.g. striking -> throw.
