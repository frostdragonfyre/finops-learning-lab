# Which AI workflow costs less per useful result?

**Goal:** compare complete workflow costs using an explicit definition of success.

**Prerequisites:** division and the idea of a cost per unit. No AI service or account is required.

## The situation

Two workflows each attempt **1,000 tasks** during a month. They use the same task mix and acceptance rubric. Review time and acceptance are measured consistently. A task counts as completed only when its final result meets the rubric after any required review or correction.

| Measure | Workflow A | Workflow B |
| --- | ---: | ---: |
| Tasks attempted | 1,000 | 1,000 |
| Total inference spending | $40 | $80 |
| Allocated platform costs | $20 | $20 |
| Human review and correction | 8 hours | 3 hours |
| Assumed review labor rate | $40/hour | $40/hour |
| Accepted completed tasks | 800 | 900 |

These are synthetic teaching figures. They are not provider prices, a model benchmark, or research findings. Assume the listed costs cover the modeled workflow for this comparison. All spending and review effort—including rejected attempts—remain in the numerator.

## Try the decisions

1. Which workflow has lower inference spending per attempt?
2. Calculate review labor cost for each workflow.
3. Add inference, platform, and review costs.
4. Divide the total by accepted completed tasks.
5. Explain why the two comparisons lead to different impressions.

<details>
<summary>Open the worked explanation</summary>

### Compare inference per attempt

- A: $40 / 1,000 = **$0.04 per attempt**.
- B: $80 / 1,000 = **$0.08 per attempt**.

On this narrow measure, A appears cheaper.

### Include review effort

- A: 8 × $40 = **$320** of review labor.
- B: 3 × $40 = **$120** of review labor.

### Include the modeled workflow cost

- A: $40 + $20 + $320 = **$380**.
- B: $80 + $20 + $120 = **$220**.

### Use the defined outcome

- A: $380 / 800 = **$0.475 per accepted task**.
- B: $220 / 900 ≈ **$0.244 per accepted task**.

Under these assumptions, B has a lower modeled cost per accepted result even though its inference spending per attempt is higher.

</details>

## Check what the comparison leaves out

Before making a real decision, examine integration, training, monitoring, latency, incident handling, and other relevant costs or requirements. Confirm that the task mix and acceptance criteria are comparable. A workflow that handles easier work is not automatically more efficient at the same task.

Labor cost also differs from cash savings. Less review time can free capacity without reducing payroll. State what the labor rate represents and how freed time would be used.

## Check your reasoning

Could you count only the successful attempts’ inference spending when calculating the cost per accepted task?

<details>
<summary>Review the reasoning</summary>

That would leave out spending required to operate the workflow. Include costs incurred across successful and unsuccessful attempts, then divide by the explicitly defined useful outcome. State any allocation or exclusion clearly.

</details>

## Record the decision

Use the [cost decision record](../templates/cost-decision-record.md) to document the unit, measurement period, task mix, cost boundary, acceptance criteria, and review trigger. Connect the economics to quality, risk, and ownership before recommending a change.

[Previous: shared cloud costs](01-shared-cloud-costs.md) · [Return to the lab](../README.md)
