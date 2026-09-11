# Analytics visualization review checklist

Use this checklist to critique a dashboard or visualization before delivery.

## Decision fit

- [ ] Is there a clearly defined recurring job or decision?
- [ ] Is the primary audience identifiable?
- [ ] Does the page answer one coherent job rather than several unrelated ones?
- [ ] Is the key metric an outcome rather than an effort proxy?

## Metric logic

- [ ] Is the process or KPI logic explicit?
- [ ] If using a metric map, does the layout follow the real workflow?
- [ ] If using a metric tree, are components and drivers clearly distinguished?
- [ ] Are relationship types honest about causality?
- [ ] Are important guardrails present?
- [ ] Are supporting metrics compact enough to reason about?

## Comparison integrity

- [ ] Is every delta's comparison window explicit?
- [ ] Are attribution/cohort windows defined where relevant?
- [ ] Is seasonality handled appropriately?
- [ ] Are targets/benchmarks defined rather than implied?
- [ ] Are tracking or definition changes annotated?

## Diagnostic power

- [ ] Can the user move from key metric → driver → segment?
- [ ] Can the user filter a suspicious segment and re-read the full system?
- [ ] Are rates shown with meaningful counts/volume?
- [ ] Are cohorts used when lifecycle behavior would be hidden by averages?
- [ ] Is a natural counter-metric paired with the headline metric?

## Visual quality

- [ ] Does the reading order match the analytical reasoning path?
- [ ] Are the most important elements visually dominant?
- [ ] Are related trends aligned to the same period?
- [ ] Is color mostly neutral with semantic highlights?
- [ ] Does the design work without relying on red/green alone?
- [ ] Are labels readable without excessive legends?
- [ ] Are charts sorted logically?
- [ ] Are there unnecessary pies, gauges, 3D charts, or decorative effects?

## Actionability

- [ ] Does the view identify where to investigate next?
- [ ] Are actionable levers separated from descriptive diagnostics?
- [ ] Does the user know what could go wrong if a lever is pushed?
- [ ] Is there a clear path to drill down or inspect detail?

## Evidence

- [ ] Are causal claims supported, or appropriately softened?
- [ ] Are low-volume slices prevented from dominating the visual story?
- [ ] Are missing/partial data and data-quality issues visible?
