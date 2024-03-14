# Banking_Dataset_Assignment

The notebook file is designed to to process transaction data, correct OCR-like errors, normalize amount values, separate individual transactions from aggregated data, reconcile transactions, detect anomalies.

## Data cleaning approach:-

There were two types of OCR errors:-
1 has been scanned as 'l'
0 has been scanned as 'o'

Corrected OCR-like errors in account numbers and descriptions. Then I normalized amount values.

## Data Analysis approach:-

1. Identified and separated individual transactions from aggregated data
2. Identified aggregated data (subtotals/yearly totals)
3. Made a Group by on 'Transaction Date' column and calculated the sum of all montlhy transactions for individual transactions
4. Checked if monthly subtotal is correct
5. Found the difference between individual amount and Individual amount and checked if the monthly subtotal amount is correct

## Anomaly Detection approach:-

1. Calculated the difference between 1st(Q1) and 3rd quartile (Q3)
2. Kept the outlier boundary as :-

IQR = Q3 - Q1
lower_bound = Q1 - 1.5 * IQR
upper_bound = Q3 + 1.5 * IQR

## Library used:- 
Pandas, seaborn , matplotlib, numpy


