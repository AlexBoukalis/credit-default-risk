# Data

The raw dataset is not committed to this repo. Download it yourself and drop it in this folder.

## What to download

UCI "Default of Credit Card Clients" (Taiwan, 2005). 30,000 rows, 24 columns (one ID column, 23 predictors, 1 target).

## Where to get it

- UCI Machine Learning Repository (original source): https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients
- Kaggle mirror, already in the `UCI_Credit_Card.csv` format used here: https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset

After downloading, place the file here so the path is:

```
data/UCI_Credit_Card.csv
```

The notebook reads it from `../data/UCI_Credit_Card.csv`.

## Columns

- `ID` — client id
- `LIMIT_BAL` — credit limit (NT dollars)
- `SEX` — 1 = male, 2 = female
- `EDUCATION` — 1 = grad school, 2 = university, 3 = high school, 4 = other. The notebook folds the undocumented codes 0, 5, 6 into 4.
- `MARRIAGE` — 1 = married, 2 = single, 3 = other. The notebook folds the undocumented code 0 into 3.
- `AGE` — years
- `PAY_0, PAY_2 ... PAY_6` — repayment status for the last six months. **-2** = no balance / paid early, **-1** = paid in full on time, **0** = used revolving credit (not late), **1 to 9** = months of payment delay. `PAY_0` is the most recent month.
- `BILL_AMT1 ... BILL_AMT6` — bill amount for each of the six months
- `PAY_AMT1 ... PAY_AMT6` — amount paid for each of the six months
- `default.payment.next.month` — target. 1 = defaulted next month, 0 = paid.

## Why it is not committed

Linking the source keeps the repo small and avoids redistributing the dataset. The notebook ships with all outputs and charts already rendered, so you can read the full analysis without downloading anything.
