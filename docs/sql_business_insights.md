# SQL Business Analysis — Olist E-Commerce

## Project Overview

This analysis uses the Olist e-commerce dataset to understand sales performance, customer behavior, payment methods, seller performance, delivery performance, customer reviews, and order status.

**Tools:** MySQL, SQL

## 1. Monthly Orders and Item Sales

- Monthly order volume and item sales were analyzed.
- November 2017 recorded the highest order count among the months in the query results, with 7,451 orders.
- Item sales represent product prices only; freight charges and profit are excluded.
- The first and last months contain very few orders, so these periods should be interpreted cautiously.

## 2. Product Category Performance

- Health & Beauty generated the highest item sales among the categories analyzed: 1,258,681.34.
- Watches & Gifts ranked second, generating 1,205,005.68.
- Bed Bath & Table recorded the highest number of distinct orders among the top 10 categories, with 9,417 orders.

## 3. Payment Method Analysis

- Credit cards generated the highest payment value: 12,542,084.19.
- Boleto generated 2,869,361.27.
- Voucher payments had an average payment value of 65.70.
- Three `not_defined` payment records had a total payment value of zero and may require further investigation.

## 4. Delivery Performance

- 88,644 delivered orders were on time or early.
- 7,826 delivered orders were late.
- Approximately 91.9% were on time or early, while 8.1% were late.
- Late orders had an average calendar-date difference of 8.87 days beyond the estimated delivery date, based on SQL `DATEDIFF()`.

## 5. Customer Repeat Rate

- 96,096 unique customers were analyzed.
- 93,099 customers (96.88%) placed only one order.
- 2,997 customers (3.12%) placed multiple orders.
- Increasing repeat purchases may be a potential customer-retention opportunity.

## 6. Customer Value Analysis

- 95,420 customers with order-item records were included.
- Total item spend was 13,591,643.70.
- Average item spend per included customer was 142.44.
- Average orders per included customer was 1.03.
- These figures represent item sales, not profit, and exclude freight charges.

## 7. Seller Performance

- The highest-selling seller in the query generated 229,472.63 in item sales across 1,132 distinct orders.
- The seller with the most orders among the top 10 had 1,806 orders.
- The highest average item price among the top 10 sellers was 543.36.
- Seller performance was ranked by item sales; profitability was not calculated.

## 8. Customer Review Analysis

- 57,328 reviews (57.78%) had a 5-star rating.
- 19,142 reviews (19.29%) had a 4-star rating.
- Combined, 77.07% of reviews had 4 or 5 stars.
- 11,424 reviews (11.51%) had a 1-star rating.
- Low-rated reviews could be investigated alongside delivery and product experience data.

## 9. Order Data Quality

- The orders table contained 99,441 records.
- All 99,441 order IDs were unique.
- No order IDs or customer IDs were missing in the orders table.
- This validates basic ID completeness and uniqueness, not every aspect of data quality.

## 10. Order Status Analysis

- Delivered orders: 96,478 (97.02%).
- Shipped orders: 1,107 (1.11%).
- Canceled orders: 625 (0.63%).
- Unavailable orders: 609 (0.61%).
- Other statuses included invoiced, processing, created, and approved.
- Cancellation and unavailability reasons require additional investigation.

## Key Business Recommendations

1. Explore customer-retention strategies to encourage repeat purchases.
2. Investigate reasons behind 1-star reviews and late deliveries.
3. Monitor canceled and unavailable orders.
4. Compare category and seller performance using sales, order volume, and customer feedback.
5. Keep sales, freight, and profit metrics separate; profit requires cost data.

## Important Notes

- Monetary values are in the dataset's original currency, Brazilian Real (BRL).
- Item sales are based on product prices and do not include freight or profit.
- Results describe the available dataset period and should not automatically be generalized to all e-commerce businesses.

