# Customer Journey Reconstruction Engine
## Day 1 — Exploratory Data Analysis

### Dataset overview
- Unique customers: 5,878
- Unique invoices: 36,969
- Unique products: 4,631
- Recorded purchase-line value: £17,374,804.27

### Customer behavior
- Customers with at least two invoices: 4,255
- Repeat-customer rate: 72.39%
- Median interval between repeat orders: approximately 24.74 days
- 44.78% of observed repeat-order intervals exceed 30 days.
- 17.04% exceed 90 days.

### Initial observations
- Monthly sales show apparent seasonal peaks near the end of both years.
- The UK accounts for most transaction rows.
- Purchase frequency and spending vary considerably across customers.
- Some customers have exceptionally high order counts or spending.

### Caveats
- These results describe the cleaned dataset and depend on the
  cleaning rules used.
- Repeat purchasing does not necessarily imply long-term loyalty.
- High spending and order counts should be investigated for
  wholesale behavior and outliers.
- Seasonal patterns should be checked against the number of
  recorded days in each month.

### Next step
Build customer features over successive time windows and study
behavioral states and transitions.