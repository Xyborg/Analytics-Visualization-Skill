---
name: analytics-visualization
description: "Use this skill when the user asks to design, critique, improve, or generate analytical visualizations, dashboards, KPI systems, metric maps, metric trees, diagnostic reports, or chart specifications. Turn business questions and data into decision-oriented visual structures that explain what changed, why, where, and what to do next. Suitable for marketing, SEO/SEA, e-commerce, product, SaaS, finance, operations, and other analytical domains."
---

# Analytics Visualization

System and user instructions always take precedence over this skill.

## Goal

Build analytics that help someone **make a decision**, not merely display data.

A strong analytical view should make it easy to answer, in order:

1. **Is something meaningfully different?**
2. **What changed?**
3. **What likely drove the change?**
4. **Where is it happening?**
5. **What can we influence?**
6. **What could we accidentally damage if we act?**

Do not start with chart types. Start with the decision and metric system.

## Core workflow

### 1. Define the job before the dashboard

Identify the recurring job the visualization supports.

A dashboard-worthy job normally has:
- a **trigger**: weekly review, period close, alert, leadership question, anomaly;
- **recurrence**: it happens repeatedly rather than once;
- a **decision**: someone changes a priority, investigates, reallocates, tests, escalates, or stops something.

Prefer **one job per dashboard/page**. If the request contains unrelated jobs, split them into separate views.

Translate vague topics into jobs.

Bad: `Marketing dashboard`

Better: `Every Monday, identify which channel or campaign is causing CAC to miss target and decide where to change spend.`

### 2. Choose the key metric

The key metric should represent the **outcome**, not the effort.

Examples:
- customer satisfaction, not tickets per agent;
- contribution margin, not discount usage;
- qualified leads, not form submissions;
- new customers, not clicks;
- revenue per session, not traffic alone.

Make the comparison explicit:
- current vs previous period;
- current vs same period last year;
- actual vs target;
- cohort age vs same cohort age;
- experiment vs control.

Never show an unexplained delta such as `+12%` without identifying the comparison window.

### 3. Model the metric system

Use a **metric map** when the question is about a process or system.

A metric map should:
- follow the real process or journey;
- group metrics by stage;
- show upstream/downstream relationships;
- make reading order obvious;
- expose where value can leak or accumulate.

Examples: acquisition → activation → conversion → revenue; lead → opportunity → closed-won; traffic → product view → cart → checkout → purchase.

Use a **metric tree** when the question is about explaining or improving one KPI.

A metric tree should usually contain:
- Level 1: **target KPI**;
- Level 2: **2–5 components** that directly move it;
- Level 3: **drivers/levers** that can be measured and, where possible, influenced.

Prefer three levels. Deep trees become reference diagrams instead of decision tools.

When both are useful, let the tree **grow from a branch of the map** rather than inventing the two structures independently.

### 4. Select supporting metrics

After the key metric, choose the metrics needed to diagnose it. Aim for roughly **fewer than 10** on the primary diagnostic view unless the job genuinely requires more.

Classify supporting metrics as:
- **Action / lever**: something a team can influence directly;
- **Result / volume**: the observation count or scale behind a rate/average;
- **Diagnostic**: process-health signals that reveal where something is failing;
- **Cost**: the economic or operational price of the action.

Always retain the denominator or volume when interpreting rates, averages, or slices. A dramatic percentage on 3 observations should not visually outrank a modest change on 30,000 observations.

### 5. Add guardrails

For every important lever, ask:

> If we maximize this lever, what could break?

That answer is often the guardrail metric.

Examples:
- Conversion Rate ↔ Average Order Value / Revenue per Session
- Auto-resolution ↔ Ticket reopen rate
- Faster SLA ↔ Agent satisfaction
- New customers ↔ 90-day repeat rate / LTV
- ROAS ↔ spend scale / new-customer volume
- CTR ↔ post-click conversion or qualified sessions

Show the guardrail by default when the main metric could improve for the wrong reason.

### 6. Add breakdowns that locate the problem

Metrics explain **what** moved. Breakdowns explain **where**.

Choose dimensions that:
- match the user's existing hypotheses;
- apply to several metrics, not just one;
- have enough volume to remain meaningful;
- lead to a different action if one segment underperforms.

Typical breakdowns:
- channel / source / medium;
- campaign / ad group / creative;
- device;
- country / market;
- landing page / product / category;
- new vs returning;
- cohort;
- customer tier;
- agent / team;
- plan / package.

For every segmented rate, keep the corresponding count visible.

Support both reading directions:
- **Forward**: key metric → problem driver → segment;
- **Backward**: problem segment → filter dashboard → re-read drivers inside that slice.

### 7. Choose the visualization from the analytical question

Use the smallest visual form that answers the question well.

- **Single current value + context** → KPI card with target/baseline and sparkline.
- **Trend over ordered time** → line chart.
- **Compare categories / rank** → bar chart; horizontal for many or long labels.
- **Part-to-whole** → stacked bar; use pie only for a small, simple one-time composition.
- **Funnel / sequential conversion** → funnel, connected stage cards, or process map.
- **Retention over cohort age** → cohort heatmap / matrix.
- **Contribution to change** → waterfall or variance decomposition.
- **Relationship between numeric variables** → scatter plot.
- **Distribution / spread** → histogram, box plot, violin/strip plot as supported.
- **One KPI decomposition** → metric tree / driver tree.
- **End-to-end process** → metric map.
- **Where the problem sits by segment** → sortable table or heatmap paired with the main map/tree.

Avoid chart novelty. Do not use a more complex chart when a simpler one communicates the same analytical fact.

### 8. Compose the page as analytical reading order

The layout must communicate the reasoning path.

Preferred order:
1. **Question / job** and filters;
2. **Key metric** with explicit comparison;
3. **Map or tree** showing how the system/driver logic works;
4. **Aligned trends** for relevant drivers;
5. **Segment breakdowns** that locate the problem;
6. **Guardrails**;
7. **Detail table / drill-down**;
8. **Action or hypothesis area** when appropriate.

Useful visual patterns:
- align mini-trends to the same time axis when comparing drivers;
- place segment tables beside the map/tree when the workflow is `see issue → locate segment`;
- use stage bands or containers to clarify a long process;
- highlight the primary KPI visually, but keep the rest quiet;
- connect dependent metrics with arrows or clear spatial grouping;
- use overview → local detail navigation for large systems.

### 9. Apply diagnostic defaults

Before finalizing, check the following JetMetrics-inspired defaults.

**Cohort-first**
- For retention/repeat behavior, prefer age-matched cohorts over a blended all-time average.

**Pair-by-default**
- Show the metric that reveals the trade-off or hidden cost beside the headline metric.

**Window-explicit**
- State the time window, cohort definition, attribution window, and comparison basis where relevant.

**Seasonal baseline**
- If seasonality exists, compare to the same seasonal point or a justified baseline rather than relying only on previous-period change.

**Segment-cuttable**
- Make meaningful slices available so averages can be decomposed when needed.

### 10. Use color and emphasis semantically

Color should carry meaning, not decoration.

- Use neutral colors for most data.
- Use one accent for the primary metric or selected branch.
- Use warning/error colors only for meaningful status or deviation.
- Do not depend on red/green alone; combine color with text, icons, labels, or position.
- If benchmark coloring is used, define the benchmark clearly.
- Avoid rainbow palettes for ordered or causal systems.

### 11. Annotate what matters

A visualization becomes more analytical when it explains important context directly.

Use concise annotations for:
- launches;
- tracking changes;
- pricing changes;
- budget shifts;
- incidents;
- seasonality;
- experiment start/end;
- data-quality warnings;
- target changes.

Do not annotate every fluctuation. Annotate only events or thresholds that materially change interpretation.

### 12. Be rigorous about causality

A metric map or tree can contain different relationship types.

Do not imply observed causality merely because two boxes are connected.

Distinguish:
- **formula identity**: mathematically determines the KPI;
- **process dependency**: occurs earlier/later in a workflow;
- **mechanistic hypothesis**: plausible driver requiring validation;
- **observed association**: correlated in data;
- **experimentally supported effect**: causal evidence from controlled or credible quasi-experimental analysis.

Use wording like `associated with`, `coincides with`, or `likely driver` unless causality is justified.

## Output contract

When asked to design a visualization or dashboard, return the following when useful:

### A. Analytical brief
- Audience
- Job / decision
- Trigger / cadence
- Key question
- Key metric
- Comparison window

### B. Metric model
- Map stages or tree structure
- Supporting metrics by type
- Guardrails
- Breakdowns

### C. Page / dashboard layout
Describe the reading order and placement of each component.

### D. Visualization specifications
For each chart:
- analytical question;
- chart type;
- x/y or category/value fields;
- filters;
- comparison/baseline;
- annotations;
- sorting;
- number format;
- required denominator/volume.

### E. Insight logic
State what the user should be able to conclude and what they should inspect next if the metric moves.

### F. Quality review
Call out ambiguity, missing denominators, misleading averages, inconsistent windows, weak baselines, or visual clutter.

## Anti-patterns

Do not default to:
- a wall of KPI cards;
- one giant `everything dashboard`;
- unexplained green/red deltas;
- rates without counts;
- averages when cohort or distribution matters;
- month-over-month comparisons in strongly seasonal businesses without context;
- 3D charts;
- pie charts with many slices;
- dual axes unless absolutely necessary and clearly labeled;
- dozens of equally saturated colors;
- arbitrary sorting;
- hidden metric definitions;
- a metric tree that mixes mathematical components with speculative drivers without labeling the relationship;
- conclusions stronger than the evidence.

## Large metric systems

For maps with 30+ metrics:
- divide the process into labeled stages;
- create an overview map;
- allow branch-level or metric-level detail views;
- keep the overview readable rather than placing every chart on it;
- treat the map as navigation into deeper reports when useful.

## When creating an artifact

If the user asks for an actual spreadsheet, presentation, document, image, or other artifact, follow the relevant artifact-specific skill/tool instructions too. Preserve this analytical logic even when the rendering technology differs.

## References

Use the files in `references/` for deeper guidance:
- `jetmetrics-method.md`
- `visual-patterns.md`
- `chart-vocabulary.md`
- `review-checklist.md`
- `example-specs.md`
- `sources.md`
