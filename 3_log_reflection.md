# 3 — Check log and reflection

## Verification log

| Check | Result | Evidence / reason |
|---|---|---|
| Predicted row count | Accepted | 96 rows, matching the prediction. |
| Predicted distinct products | Accepted | 4 products. |
| Predicted distinct cities | Accepted | 2 cities. |
| Predicted distinct dates | Accepted | 12 dates. |
| Missing values | Accepted | No missing values in the six columns. |
| Duplicate rows | Accepted | No exact duplicate rows. |
| “Everything costs more” as a literal conclusion | Rejected | Only four products are included, so the data cannot represent everything people buy. |
| “Staples are unaffordable” | Rejected | No household income, wages, expenditure, budget or affordability threshold is provided. |
| “These are official PBS price observations” | Rejected | The CSV label explicitly says illustrative teaching data, not actual PBS observations. |
| City comparison | Accepted | All 48 matched product-date pairs show City 2 exactly PKR 6/kg above City 1. |

## AI-use / verification record

The AI-generated analytical suggestions were treated as hypotheses, not evidence. The following alternatives were considered and checked against the available columns:

1. Did each product's two-city average rise from the first to the last date? **Accepted:** `date`, `item`, and `price` exist.
2. Was City 2 more expensive than City 1 for each matched product and date? **Accepted:** `city`, `date`, `item`, and `price` exist.
3. Did the price rise make the products unaffordable for households? **Rejected:** income and household budget variables are absent.
4. Did the price movements prove Pakistan's national inflation rate? **Rejected:** the file has only two invented city labels and four products, and is marked illustrative.
5. Did every good in the economy become more expensive? **Rejected:** the dataset covers only four named teaching products.

**Log row:** Used the supplied CSV in a Python notebook; checked dimensions, distinct values, missing values, duplicates, first-to-last product averages, and matched city price differences. The notebook contains the calculations and printed evidence.

## Reflection (about 100 words)

The data can say something narrow but useful about the four products included in this exercise. Their average listed prices across the two cities were higher on 19 March than on 1 January 2026. It also shows a consistent difference between the two city labels: City 2 is PKR 6 per kg higher in every matched observation. However, the data cannot explain why prices changed or whether people could afford the products. It does not include wages, household budgets, other goods or real market observations. Since the file is labelled illustrative, I cannot use it to make claims about actual PBS prices or Pakistan's overall inflation.

## Most tempting unsupported suggestion

The most tempting suggestion was to describe the results as proof that the cost of living in Pakistan increased. That sounds like a strong headline, but the dataset is too limited and explicitly illustrative. It contains no income or expenditure information, so it also cannot support a claim about affordability.
