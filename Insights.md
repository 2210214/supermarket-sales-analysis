# Supermarket Sales Analysis – Business Insights

## Project Overview
This project analyzes 1,000 point-of-sale transactions from three supermarket branches (A – Yangon, B – Mandalay, C – Naypyitaw) over Q1 2019 (January 1 – March 30). The Power BI dashboard tracks sales, profitability, and customer behavior across branch, product line, customer type, and payment method, with monthly trend tracking.

All figures below are calculated directly from the source dataset (`supermarket_sales.csv`), unfiltered, unless stated otherwise.

## KPIs (Q1 2019, all branches)

| KPI | Value |
|---|---|
| Total Sales | $322,966.75 |
| Total COGS | $307,587.38 |
| Gross Income | $15,379.37 |
| Gross Margin % | 4.76% |
| Total Quantity Sold | 5,510 units |
| Total Transactions | 1,000 |
| Average Transaction Value | $322.97 |
| Average Customer Rating | 6.97 / 10 |

**Note on Gross Margin %:** this metric is structurally flat at ~4.76% across every branch, product line, and month in this dataset — gross income is fixed at exactly 5% of cost of goods sold for every transaction, so the ratio of gross income to sales can't move regardless of how the data is sliced. It's a real, correctly calculated KPI — it's just not a metric that will reveal variation in this particular dataset.

## Sales by Branch

| Branch | City | Sales | Share of Total | Transactions | Avg Rating |
|---|---|---|---|---|---|
| C | Naypyitaw | $110,568.71 | 34.2% | 328 | 7.07 |
| A | Yangon | $106,200.37 | 32.9% | 340 | 7.03 |
| B | Mandalay | $106,197.67 | 32.9% | 332 | 6.82 |

Branch performance is essentially even — Branch C holds a narrow lead (~1.4 percentage points above A and B), and Branches A and B are effectively tied. There is no dominant or underperforming branch in this period.

## Sales & Profitability by Product Line

| Product Line | Sales | Gross Income | Share of Sales |
|---|---|---|---|
| Food and beverages | $56,144.84 | $2,673.56 | 17.4% |
| Sports and travel | $55,122.83 | $2,624.90 | 17.1% |
| Electronic accessories | $54,337.53 | $2,587.50 | 16.8% |
| Fashion accessories | $54,305.89 | $2,585.99 | 16.8% |
| Home and lifestyle | $53,861.91 | $2,564.85 | 16.7% |
| Health and beauty | $49,193.74 | $2,342.56 | 15.2% |

Product line performance is tightly clustered — the gap between the top line (Food and beverages) and the bottom line (Health and beauty) is only 14.1%. Food and beverages leads on both sales and gross income; Health and beauty is the consistent lowest performer, though not by a wide margin.

By customer rating, Food and beverages also scores highest (7.11), while Home and lifestyle scores lowest (6.84) — a gap of less than 0.3 points, so ratings are broadly consistent across categories.

## Sales by Customer Type

| Customer Type | Sales | Transactions | Avg Rating |
|---|---|---|---|
| Member | $164,223.44 | 501 | 6.94 |
| Normal | $158,743.30 | 499 | 7.01 |
| **Difference** | **+3.4%** | **+2** | -0.07 |

Member and Normal (non-loyalty) customers are nearly split 50/50 by both revenue and transaction count. Membership does not currently correlate with meaningfully higher spend per customer in this dataset, and satisfaction ratings are essentially identical between the two groups.

## Transactions by Payment Method

| Payment Method | Sales | Transactions |
|---|---|---|
| Cash | $112,206.57 | 344 |
| Ewallet | $109,993.11 | 345 |
| Credit card | $100,767.07 | 311 |

Cash and Ewallet are used almost equally (344 vs. 345 transactions) and are both moderately ahead of Credit card, which trails by roughly 10% in transaction count.

## Monthly Sales & Gross Income Trend

| Month | Sales | Gross Income | Transactions |
|---|---|---|---|
| January | $116,291.87 | $5,537.71 | 352 |
| February | $97,219.37 | $4,629.49 | 303 |
| March | $109,455.51 | $5,212.17 | 345 |

Sales dip in February (both in total value and transaction count) before recovering in March, though March doesn't fully return to January's level. Since the dataset only spans three months, this shouldn't be read as a strong seasonal pattern — it's a short-term dip worth monitoring with more data.

## Key Findings

1. **No single branch, product line, or customer segment dominates.** Every major breakdown in this dataset (branch, product line, customer type, payment method) falls within a 10–15% spread — performance is broadly even across the business.
2. **Branch C and the Food & Beverages line are the closest things to "top performers,"** but only by narrow margins, not decisively.
3. **Membership status doesn't show a clear revenue or satisfaction advantage** over non-member (Normal) customers in this period.
4. **February is a soft month** for both sales and transaction volume relative to January and March.
5. **Gross margin is structurally uniform** at ~4.76% across every dimension — a feature of how this dataset was generated, not a business insight to act on.

## Recommendations

1. **Investigate the February dip** — with only one quarter of data, it's not possible to tell if this is seasonal or a one-off; recommend tracking the same period next year before drawing conclusions.
2. **Health and beauty is the consistent lowest performer** across sales, gross income, and customer rating — worth a closer look at pricing, placement, or promotion for this category, even though the gap to other lines is modest.
3. **Membership isn't currently driving incremental value** — if loyalty-program investment is a priority, this data suggests the current program isn't differentiating Member spend from Normal customer spend, and may be worth revisiting.
4. **Credit card usage trails Cash and Ewallet** — if card-processing fees are lower than cash-handling costs, there may be a case for lightly incentivizing card/e-wallet payments, though this dataset doesn't include cost-per-payment-method data to confirm that assumption.

## Conclusion

Across Q1 2019, the three branches performed at a comparable level, generating $322,966.75 in total sales and $15,379.37 in gross income from 1,000 transactions. No product line, branch, or customer segment stands out as a clear over- or under-performer — the business shows balanced demand across categories, with only modest month-to-month and category-level variation. The clearest actionable signals are the February softness in sales volume and the consistently lower performance of the Health and beauty line, both of which merit further investigation with additional data.
