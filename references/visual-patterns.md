# Visual patterns observed in public JetMetrics examples

These are design observations from publicly available JetMetrics dashboard images and product screenshots.

## Pattern 1: Map + compact metric cards

A causal/process diagram uses small cards as nodes. Each node can contain:
- metric name;
- current value;
- period-over-period delta;
- compact sparkline or mini bar trend.

Connectors explain the reading direction. The card does not need to be visually heavy; the structure carries much of the meaning.

## Pattern 2: Map + aligned time context

When several drivers are compared, each node's mini-chart uses the same period and temporal alignment. This makes co-movement and divergence easier to spot.

Rule: do not compare mini-trends with mismatched windows or scales without clear labeling.

## Pattern 3: Funnel map + segment table

One public CRO dashboard places the funnel/metric map on the left and dense segment breakdown tables on the right.

This creates a deliberate workflow:
1. locate the weak funnel stage;
2. scan segments at that stage;
3. filter or drill into the responsible slice.

This is often stronger than placing all segment charts on separate pages.

## Pattern 4: Stage bands for long funnels

The GA4 full-funnel example groups the map into horizontal stage bands such as traffic, item views, cart, checkout, purchases, and revenue.

Use stage bands when:
- the map is tall or complex;
- the process naturally has phases;
- readers need to orient themselves quickly.

Keep band backgrounds subtle enough that cards and connectors remain dominant.

## Pattern 5: KPI-first tree

A driver-tree example places the target outcome at the top, direct components below, and deeper drivers farther down. Negative/positive changes are highlighted in node backgrounds or small status areas.

Use stronger emphasis at the root and progressively quieter treatment deeper in the tree.

## Pattern 6: Overview + local neighborhood

Large systems benefit from an overview map plus a focused detail view around one metric. The detail view includes only immediate upstream and downstream relationships.

This preserves context without forcing the user to inspect a huge map for every task.

## Pattern 7: Semantic highlights, not decorative palettes

Public examples generally reserve stronger colors for:
- error/underperformance;
- improvement;
- benchmark status;
- selected KPI;
- stage grouping.

Most structural elements remain neutral.

## Pattern 8: Values and trends live together

A useful metric card rarely shows only the current value. It pairs current state with at least one of:
- delta;
- trend;
- benchmark;
- target range;
- period comparison.

This reduces the need for a separate `KPI card row` disconnected from the process view.
