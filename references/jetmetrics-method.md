# JetMetrics method: synthesized reference

This reference summarizes the recurring analytical design ideas found across JetMetrics' public materials. It is a synthesis, not a reproduction of any single article.

## 1. Dashboards are interfaces for analytical thinking

JetMetrics consistently argues that a collection of KPI cards can report change without explaining it. Their alternative is to make the structure of the business visible: process, dependencies, decompositions, segments, and paths for diagnosis.

Practical implication: the dashboard layout should mirror how a user reasons through a problem rather than how data happens to be stored.

## 2. Metric map = process model

A metric map is best used to represent an end-to-end process. Its shape follows the workflow rather than a fixed visual grammar. It may be linear, branched, cyclic, layered, or grouped.

A good map answers:
- What stages exist?
- What can be measured at each stage?
- What sits upstream and downstream?
- Where can value leak?
- Where should the analyst look next?

Maps are especially useful for operational dashboards and navigation across larger analytics systems.

## 3. Metric tree = impact model

A metric tree starts from one target metric and decomposes it into components and lower-level drivers.

A practical structure is:
- target KPI;
- 2–5 direct components;
- 15–20 lower-level drivers at most;
- usually no more than 3 levels on the working view.

Trees are useful for diagnosis, hypothesis generation, and identifying levers.

## 4. Trees should grow from maps

The map establishes a shared process model. A tree then focuses on a relevant branch and turns it into a KPI-specific diagnostic structure.

This reduces the risk that marketing, product, finance, and operations create incompatible explanations for the same KPI.

## 5. A dashboard should be built around a job

The 2026 JetMetrics dashboard framework starts from recurring work rather than a broad topic.

A useful job has:
- a trigger;
- repetition;
- a decision at the end.

The job determines the key metric. The key metric determines supporting metrics. Supporting metrics determine useful breakdowns.

## 6. Supporting metrics have different roles

A diagnostic view becomes easier to reason about when metrics are intentionally selected as:
- levers/actions;
- result/volume metrics;
- diagnostics;
- costs;
- guardrails.

The goal is not completeness. It is a compact set that supports the actual decision.

## 7. Breakdown logic is part of the design

JetMetrics frequently pairs maps with segment tables. The map answers which part of the system is weak. The table or filtered slice answers which device, channel, page, product, cohort, or other segment is responsible.

This supports two diagnostic directions:
- system → metric → segment;
- segment → filter → system.

## 8. Five diagnostic defaults

A later JetMetrics framework can be generalized into five defaults:

### Cohort-first
Blended retention or repeat metrics can hide deterioration by acquisition cohort. When lifecycle behavior matters, compare cohorts at the same age.

### Pair-by-default
A metric should be shown beside the natural counter-metric that reveals its cost or trade-off.

### Window-explicit
The measurement and comparison window must be visible. Identical numbers over different windows can imply different realities.

### Seasonal baseline
Previous-period comparisons often confuse seasonality with a business change. Use year-over-year or another appropriate seasonal baseline when necessary.

### Segment-cuttable
The aggregate should be decomposable into decision-relevant slices. Do not force infinite granularity; preserve adequate sample size.

## 9. Maps and charts can coexist

JetMetrics examples include several useful patterns:
- metric nodes containing value + delta + sparkline;
- maps with all mini-charts aligned to the same time period;
- horizontal funnel maps;
- local `metric neighborhood` views;
- full-funnel maps grouped into process stages;
- KPI-first maps where the target metric is visually emphasized;
- metric map + segment table side-by-side.

The point is not to replace charts with diagrams. It is to make the charts follow a system.

## 10. Living documentation

Maps should change when the process changes. Trees should change when evidence about drivers changes. Unsupported relationships should be removed; confirmed ones become stronger documentation.

Treat the metric system as a maintained analytical model, not a one-off poster.
