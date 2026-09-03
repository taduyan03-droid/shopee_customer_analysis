# Shopee Customer Fraud Analysis

## Project Overview

This project analyzes customer and transaction data to identify potential
fraudulent behavior related to Shopee's promotional program.

The promotion provides a 30% discount on the total order value, capped at
20,000 VND. The analysis focuses on identifying buyers and sellers who may
have exploited the promotion and investigating potential collusion between
the two sides.

## Business Problem

Several customers were suspected of colluding with sellers to abuse the
promotion program.

The analysis aims to answer:

- Which order values appear most frequently among potentially fraudulent
  transactions?
- Which sellers show suspicious transaction patterns?
- Which buyers show suspicious purchasing behavior?
- Is there evidence suggesting collusion between buyers and sellers?
- What transaction patterns could indicate promotional abuse?

## Hypotheses

### H1 — Buyer-Seller Collusion

Buyers and sellers may collude to exploit the promotion.

This hypothesis is investigated by checking transaction IDs and the IDs of
both parties, particularly whether their transaction timing and order
volume show suspicious patterns.

### H2 — Optimal Fraudulent Order Value

Fraudulent transactions may concentrate around the 60,000–70,000 VND range,
where the 20,000 VND maximum subsidy can be fully utilized.

## Analysis

### 1. Overall Transaction Analysis

The dataset contains 4,611 orders.

Among them, 524 orders have a value of 70,000 VND, accounting for more than
11% of all orders.

A total of 3,436 orders received the maximum 20,000 VND subsidy.

### 2. Potential Fraudulent Sellers

The analysis identifies sellers with unusually high concentrations of
transactions around the 65,000–70,000 VND range.

The three sellers with the strongest potential fraud signals are:

- Seller ID 10979
- Seller ID 8576
- Seller ID 8591

Seller 10979 shows the strongest potential signal, with two products
having a high number of transactions in the 65,000–70,000 VND range within
a four-day period.

### 3. Potential Fraudulent Buyers

Potentially fraudulent buyers tend to show:

- Order values concentrated around 70,000–80,000 VND
- Multiple orders within a relatively short period
- Approximately 7–10 orders in the observed pattern

These behaviors are consistent with the hypothesis that buyers may attempt
to maximize the promotional benefit while minimizing their effective cost.

### 4. Buyer-Seller Collusion

The analysis identified:

- 337 buyers
- 207 sellers

who conducted transactions at exactly 70,000 VND.

The concentration of transactions at this value is substantially higher
than other order values and raises a strong suspicion of promotional abuse
and potential collusion.

## Case Study

Seller ID 10979 shows the strongest potential connection with buyer
101867621 over a four-day period.

However, the observed transactions between the two parties account for only
around 3% of the seller's total 87 transactions.

Therefore, the analysis cannot conclusively prove that the buyer and seller
colluded.

A further hypothesis is that the seller may have used multiple fake UIDs
to distribute transactions and reduce the concentration of orders under
a single buyer account.

## Key Findings

- 70,000 VND is the most prominent suspicious order value in the dataset.
- 524 out of 4,611 orders have a value of 70,000 VND.
- 3,436 orders received the maximum 20,000 VND subsidy.
- Seller 10979 shows the strongest potential fraud signal among the
  identified sellers.
- Buyer behavior shows suspicious concentration around 70,000–80,000 VND
  and repeated purchases.
- 337 buyers and 207 sellers were involved in transactions valued at
  70,000 VND.
- The analysis identifies strong indicators of promotional abuse but does
  not conclusively prove buyer-seller collusion.

## Conclusion

The analysis cannot conclusively establish collusion between specific
buyers and sellers.

However, fraudulent transactions show a clear concentration around
70,000 VND and occur within a short four-day period.

These patterns provide evidence of potential promotional abuse and suggest
that further investigation should focus on transaction timing, buyer-seller
relationships, repeated order patterns, and the use of multiple UIDs.

## Project Files

| File | Description |
|---|---|
| `README.md` | Project overview, methodology, findings and conclusion |
| `Shopee_customer_report.pdf` | Full analysis report |
| `customer_fraud_analysis.sql` | SQL queries used for the analysis |

## Author

**Tạ Duy An**

Data Analyst Portfolio Project
