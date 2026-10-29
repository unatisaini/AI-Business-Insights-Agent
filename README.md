# AI-Powered Business Insights Agent

An automated agent that turns weekly sales data into a decision report: what changed, why, what comes next, and what to do.

## Business questions
1. Which categories and regions make the most profit?
2. How does discounting affect profit, and is the effect causal?
3. What will weekly sales look like over the next 8 weeks?
4. Which weeks or segments are unusual (anomalies)?
5. What should a manager do about it?

## Data
Superstore Dataset (Kaggle): 9,994 order lines, 21 columns, 2014-01-03 to 2017-12-30. No missing values or duplicate rows.

## First finding
Profit falls as discount rises. Order lines with a discount above 20% lost about $135k in total, while undiscounted lines made about $321k.

| Discount | Order lines | Avg profit per line |
|---|---|---|
| 0% | 4,798 | $66.9 |
| 1-20% | 3,803 | $26.5 |
| 21-40% | 460 | -$77.9 |
| >40% | 933 | -$106.7 |

This is a correlation. The causal analysis will test whether discounts cause the losses.

## Plan
Cleaning and weekly KPIs, then forecasting, anomaly detection, causal analysis, an LLM report with a fact-check step, a feedback loop, n8n automation and a Streamlit dashboard.

## Status
Work in progress. Day 1 done: setup, data loading, cleaning and first analysis.
