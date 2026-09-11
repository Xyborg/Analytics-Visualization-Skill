# Chart vocabulary for analytical dashboards

Use this as a fast selection guide after the metric logic is defined.

| Analytical question | Preferred visualization | Notes |
|---|---|---|
| What is the current state? | KPI card + comparison + sparkline | Never show a naked value when context matters |
| How has it changed over time? | Line chart | Use a common baseline/window when comparing series |
| Which category is bigger? | Sorted bar chart | Horizontal when labels are long or categories are many |
| How does composition differ? | Stacked bar / 100% stacked bar | Prefer over pie for cross-category comparison |
| What share of one total? | Pie/donut only for few slices | Use sparingly; bar is better for ranking |
| Where does a process leak? | Funnel / connected stage cards / metric map | Show both stage volume and step conversion |
| What drives a KPI? | Driver tree / metric tree | Label relationship type when not formulaic |
| What contributed to a delta? | Waterfall / variance bridge | Strong for period-to-period decomposition |
| Which cohorts deteriorated? | Cohort heatmap | Compare at matched cohort age |
| Which segment causes the issue? | Heatmap or sortable table | Keep volume next to rate |
| Are two metrics related? | Scatter | Add reference line only when meaningful |
| What does the distribution look like? | Histogram / box / strip | Prefer to averages when spread matters |
| Which branch changed first? | Metric map with aligned mini-trends | Useful for root-cause navigation |
| Are we on target by category? | Bullet chart / bar + target | Explicitly label target |
| How does rank change over time? | Bump chart | Use only when rank itself matters |
| How does a quantity accumulate? | Line / area | Avoid area when exact comparisons matter |
| What is the hierarchy and magnitude? | Treemap | Use cautiously; harder for precise comparison |

## Selection rules

1. Prefer **position on a common scale** for precise comparison.
2. Avoid encoding an important measure only by area or angle when a bar can do the job.
3. Use small multiples instead of an overloaded multi-series line chart when series compete visually.
4. Avoid dual axes unless the relationship is the analytical question and the scales are clearly labeled.
5. Sort categorical bars intentionally: magnitude, funnel order, business order, or chronological order.
6. Use consistent number formats and units across related views.
7. Rates need denominator/volume context when sample size can change interpretation.
