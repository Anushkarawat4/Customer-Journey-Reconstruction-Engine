# Customer Journey Reconstruction Engine
## Day 2 — Customer Behavioral Feature Engineering

### Dataset
- Customer-level feature rows: 5,878
- Unique customers: 5,878
- Monthly snapshot rows: 88,515
- Unique customers in snapshots: 5,878
- Snapshot months: 25

### Overall customer features
Created:
- Total orders and total spend
- Average and median order value
- Total quantity and average quantity per order
- Average products per order
- First and last purchase dates
- Recency and customer lifetime
- Approximate order frequency
- Average, median and standard deviation of purchase gaps
- Product diversity
- RFM scores

### Monthly snapshot features
Created:
- Recency
- Lifetime orders and spend
- Orders, spend and quantity in the previous 30 days
- Orders and spend in the previous 90 days
- Orders and spend in the previous 365 days
- Average order value
- Purchase gap statistics
- Average quantity and product variety per order
- Product diversity over the previous 365 days
- Month-over-month changes in 90-day order and spend activity

### Snapshot methodology
Snapshots are created at month-end.
Features use transactions on or before each snapshot date.
Only customers with at least one purchase in the preceding
365 days are included in that month's snapshot.

### Important limitations
- The dataset covers a finite historical period.
- A customer absent from a snapshot may be inactive for more
  than 365 days; absence does not prove permanent churn.
- RFM scores are relative quintile-based scores.
- Purchase-frequency estimates are unreliable for customers
  with only one observed order.
- Monthly 90-day windows overlap.

### Next step
Discover customer behavioral states and transitions over time.