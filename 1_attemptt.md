# 1 — Attempt: claims, questions and predictions

> **Snapshot note:** This is a attempt-before-AI. 

## Claim 1

“Everything costs more now.”

**Question:** For each of the four products in the dataset, did its average listed price across the two cities increase between 1 January and 19 March 2026?

**Variables needed:** `date`, `item`, `city`, and `price`. I will compare the mean of the two city prices for each item on the first and last dates.

**Prediction:** I expect most or all four products to show an increase, but the size of the increase will differ by product.

## Claim 2

“Prices are always higher in one city.”

**Question:** For each product and date, is the listed price in City 2 higher than the listed price in City 1?

**Variables needed:** `date`, `item`, `city`, and `price`. I will pair the two city observations for every product-date combination and calculate the difference.

**Prediction:** I expect City 2 to be slightly more expensive for the products in this teaching dataset.

## Initial data expectations

* Rows: 96 observations.

* Distinct products: 4.

* Distinct cities: 2.

* Distinct dates: 12.

* The dataset appears to contain weekly observations for each product in each city.