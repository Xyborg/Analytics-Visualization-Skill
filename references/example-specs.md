# Example dashboard specifications

These examples show how to apply the skill outside JetMetrics' original e-commerce focus.

## Example 1: Paid search weekly diagnostic

### Job
Every Monday, determine why new-customer CAC missed target and decide which campaigns or query groups should get more or less spend.

### Key metric
New-customer CAC, current 7 days vs previous 7 days and vs target.

### Metric tree
New-customer CAC
- Spend
  - Clicks
  - CPC
- New customers
  - Conversion rate
  - Qualified sessions
  - Checkout completion

### Guardrails
- New-customer volume
- 30-day revenue per new customer
- Brand vs non-brand mix

### Breakdown dimensions
- campaign
- query theme
- device
- landing page
- market

### Page layout
1. CAC + target + volume at top.
2. Driver tree with same-period sparklines.
3. Campaign table showing CAC, spend, new customers, conversion rate, revenue/customer.
4. Query-theme heatmap.
5. Landing-page table for suspicious campaign slice.

## Example 2: SEO performance diagnosis

### Job
When organic new customers fall, identify whether the cause is demand, visibility, click-through, landing-page conversion, or tracking.

### Key metric
Organic new customers.

### Process map
Search demand → impressions → clicks → sessions → engaged/productive sessions → conversion → new customers

### Supporting metrics
- search demand proxy / query volume where available
- impressions
- average position or visibility index
- CTR
- organic sessions
- conversion rate
- new customers
- revenue per organic session

### Guardrails
- branded vs non-branded mix
- market/device distribution
- tracked landing-page coverage

### Breakdowns
- query cluster
- landing page / template
- brand vs non-brand
- country
- device

### Visualization choices
- map with aligned mini-trends;
- ranked bar for lost clicks by query cluster;
- landing-page table with sessions, CR, new customers, volume;
- annotation for algorithm update, migration, template release, or tracking change.

## Example 3: SaaS retention

### Job
At monthly review, determine whether retention is deteriorating and which acquisition cohorts or plans are responsible.

### Key metric
Logo retention or revenue retention at a defined age, e.g. month 3.

### Required diagnostic defaults
- cohort-first;
- explicit cohort age/window;
- pair retention with expansion/contraction or ARPA;
- preserve cohort size.

### Visuals
- cohort heatmap;
- retention curve by acquisition quarter;
- plan/channel table with cohort size + month-3 retention;
- driver tree for churn reason → product adoption → support issues → billing issues.

## Example 4: Customer support health

### Job
When CSAT declines, locate the process or team issue and decide what operational lever to change.

### Key metric
CSAT trend.

### Supporting metrics
Action:
- wait time
- resolution time
- handle time
- resolution rate
- automation rate

Result:
- ticket volume

Diagnostic:
- tickets per agent
- SLA compliance

Guardrails:
- ticket reopen rate
- agent satisfaction

Breakdowns:
- ticket type
- channel
- agent/team
- human involvement
