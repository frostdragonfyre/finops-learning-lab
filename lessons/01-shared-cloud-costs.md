# Who owns the shared cloud bill?

**Goal:** compare three allocation rules and explain which assumptions make each useful.

**Prerequisites:** percentages and basic arithmetic. No cloud account is needed.

## The situation

A shared service costs **$12,000 for one month**. Three teams use it:

| Team | Measured usage share |
| --- | ---: |
| Atlas | 50% |
| Beacon | 30% |
| Cedar | 20% |

Assume the measurements are complete and comparable. All figures and team names are synthetic.

## Try the decisions

1. Divide the entire bill equally. What does each team receive?
2. Allocate the bill by measured usage. What changes?
3. Allocate 50% equally and 50% by usage. Calculate each team’s allocation.
4. Check that every method allocates the full $12,000 exactly once.
5. Suppose usage explains consumption but the service also maintains minimum shared capacity. What would you investigate before selecting a rule?

<details>
<summary>Open the worked explanation after trying the questions</summary>

### Equal split

Each team receives $12,000 / 3 = **$4,000**. This rule is simple, but it does not represent the differences in measured consumption.

### Usage-based allocation

Multiply the bill by each share:

- Atlas: $12,000 × 0.50 = **$6,000**.
- Beacon: $12,000 × 0.30 = **$3,600**.
- Cedar: $12,000 × 0.20 = **$2,400**.

Total: **$12,000**.

### A blended rule

The equal portion is $6,000 / 3 = $2,000 per team. Allocate the remaining $6,000 by usage.

| Team | Equal portion | Usage portion | Total |
| --- | ---: | ---: | ---: |
| Atlas | $2,000 | $3,000 | **$5,000** |
| Beacon | $2,000 | $1,800 | **$3,800** |
| Cedar | $2,000 | $1,200 | **$3,200** |

Total: **$12,000**.

For any equal-allocation fraction `e` from 0 to 1:

`team allocation = total bill × (e / number of teams + (1 − e) × usage share)`

The model assumes the entire bill is allocated, the shares sum to one, and the same measurement basis is appropriate for each team.

</details>

## Explain what the number means

A usage rule can make consumption visible. An equal rule can express a shared base obligation. A blend can express both, but its percentage still needs a reason. Investigate which costs vary with use, which support common capacity, and what the allocation is meant to accomplish.

The formula does not decide which rule is fair. People must explain the service, its beneficiaries, the quality of the measurement, and the accountability they want to establish.

## Check your reasoning

One team’s usage data is missing. Is zero a sound substitute?

<details>
<summary>Review the reasoning</summary>

Missing measurement does not establish zero consumption. Make the gap visible, agree on an interim basis, name its owner, and set a review date. Explain how the limitation could affect each allocation.

</details>

## Record the decision

Use the [cost decision record](../templates/cost-decision-record.md). Include the basis, assumptions, data owner, and the changes that would trigger a review.

[Next: AI unit economics](02-ai-unit-economics.md) · [Return to the lab](../README.md)
