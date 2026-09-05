# Dataset Description

> **Note:** The dataset used in this case study is analyzed for
> educational and portfolio purposes. It provides the quantitative
> evidence used to identify sales patterns and business opportunities
> for the simulated Terra Tint Cosmetics business.

## 1. Dataset Overview

The dataset contains historical cosmetics sales transaction records
covering the period from January 1, 2022 to August 30, 2022. It is
used as the primary data source for analyzing sales performance,
product performance, geographic performance, salesperson performance,
and sales trends.

The main transaction dataset contains 374 records and seven fields.
Each record represents a sales transaction containing information
about the salesperson, country, product, transaction date, sales
amount, quantity shipped, and unit price.

## 2. Dataset Scope

The dataset covers the following areas:

- **Time period:** January 1, 2022 to August 30, 2022
- **Transactions:** 374
- **Salespeople:** 10
- **Countries:** 6
- **Products:** 15
- **Total recorded sales:** approximately $2.91 million

The dataset provides sufficient information to examine sales-related
patterns across different dimensions of the business.

## 3. Dataset Fields

The main dataset contains the following fields:

| Field | Data Type | Description |
|---|---|---|
| Sales Person | Text | Name of the salesperson associated with the transaction |
| Country | Text | Country associated with the sale |
| Product | Text | Product sold in the transaction |
| Date | Date | Date on which the transaction occurred |
| Amount ($) | Numeric | Total recorded sales amount for the transaction |
| Boxes Shipped | Integer | Number of boxes shipped in the transaction |
| Unit Price | Numeric | Price per box/unit recorded for the product |

## 4. Data Dimensions

The dataset can be analyzed using several business dimensions.

### 4.1 Geographic Dimension

The `Country` field allows sales performance to be compared across
different geographic markets.

The six countries represented in the dataset are:

- United States
- New Zealand
- Australia
- United Kingdom
- Canada
- India

### 4.2 Product Dimension

The `Product` field allows the performance of individual cosmetics
products to be analyzed.

The dataset contains 15 different products, allowing comparisons of
product-level sales contribution and identification of higher- and
lower-performing products.

### 4.3 Salesperson Dimension

The `Sales Person` field identifies the salesperson associated with
each transaction.

With 10 salespeople represented in the dataset, sales performance
and transaction activity can be compared across individual
salespeople.

### 4.4 Time Dimension

The `Date` field allows sales transactions to be analyzed over time.

Monthly aggregation can be used to identify changes in sales volume,
periods of higher or lower sales activity, and overall sales trends.

## 5. Key Measures

The primary quantitative measures available in the dataset are:

### Sales Amount

The `Amount ($)` field represents the recorded monetary value of
each transaction. It can be aggregated to calculate total sales and
compare revenue contribution across countries, products,
salespeople, and time periods.

### Boxes Shipped

The `Boxes Shipped` field represents the quantity shipped for each
transaction. It can be used to examine shipment volume and compare
sales activity across different products and markets.

### Unit Price

The `Unit Price` field represents the recorded price per unit or
box. It can be used to examine pricing differences across products
and transactions.

## 6. Data Quality Assessment

The main transaction dataset was reviewed for basic data quality
issues, including missing values, duplicate records, and numerical
consistency.

### Missing Values

No missing values were identified in the seven fields of the main
transaction dataset.

### Duplicate Records

No exact duplicate rows were identified in the main transaction
dataset.

### Numerical Consistency

The relationship between `Amount ($)`, `Boxes Shipped`, and
`Unit Price` was checked using the expected calculation:

```text
Amount ($) = Boxes Shipped × Unit Price
```

The recorded values are consistent with this relationship, providing
a basic validation check for the transaction amounts.

## 7. Data Preparation

Before analysis, the dataset can be prepared through the following
steps:

1. Review the structure and data types of each field.
2. Check for missing values.
3. Check for duplicate records.
4. Validate numerical relationships between relevant fields.
5. Standardize field formats where necessary.
6. Aggregate transactions by relevant business dimensions.
7. Calculate summary measures and performance indicators.
8. Visualize important trends and patterns.

These preparation activities support reliable analysis and provide a
basis for the business findings presented later in the project.

## 8. Analytical Opportunities

The dataset can be used to investigate several business questions,
including:

- Which countries generate the highest sales?
- Which products contribute the most to total sales?
- How does sales performance vary among salespeople?
- How do sales change from month to month?
- Which products have relatively high or low sales contribution?
- Which geographic markets contribute the largest share of sales?
- How does transaction volume vary across products and markets?

The answers to these questions will be used to identify business
findings and potential improvement opportunities.

## 9. Key Data Findings

Initial analysis of the dataset identified several notable patterns.

### Geographic Sales Performance

The United States generated the highest recorded sales at
approximately $628,488, followed by New Zealand at approximately
$557,060 and Australia at approximately $505,498.

This indicates that sales contribution differs considerably across
geographic markets.

### Product Sales Performance

Tea Tree Moisturizer generated the highest recorded product sales at
approximately $260,905, followed by Hydrating Face Serum at
approximately $250,323.

Charcoal Face Wash generated the lowest recorded product sales at
approximately $102,733.

This indicates substantial variation in sales contribution between
products.

### Salesperson Performance

Sales contribution also varies across salespeople. Olivia D'Souza
recorded the highest total sales among the salespeople represented in
the dataset, at approximately $387,406.

This provides an opportunity to analyze salesperson performance and
transaction patterns.

### Monthly Sales Performance

Monthly sales also fluctuate during the analyzed period. Recorded
monthly sales increased substantially from February to March and
then generally declined toward August.

This indicates that time-based sales monitoring could provide useful
information for management decision-making.

## 10. Data Limitations

Although the dataset provides useful sales information, it has
several limitations.

The dataset does not contain:

- Customer profiles or customer demographics
- Customer purchase history
- Inventory stock levels
- Reorder points
- Stockout records
- Supplier information
- Payment status
- Delivery status
- Product cost
- Profit or margin
- Marketing campaign information
- Product categories

Therefore, the dataset can support analysis of sales-related patterns
but cannot independently establish actual inventory shortages,
customer retention problems, supplier performance issues, or
profitability.

Inventory management, customer management, order management, and
other capabilities discussed later in the project should therefore
be treated as **proposed system requirements**, rather than findings
directly proven by the dataset.

## 11. Relationship to the Business Analysis

The dataset serves as an evidence base for the wider Business
Analysis process.

The analysis follows this relationship:

```text
Dataset
   ↓
Data Analysis
   ↓
Business Findings
   ↓
Business Implications
   ↓
Business Problems / Opportunities
   ↓
Requirements
   ↓
Proposed System
```

The findings from the dataset will be combined with the simulated
business process analysis to identify pain points and gaps. These
findings will subsequently inform the business requirements and
functional requirements for the Smart Cosmetics Retail Management
System.

## 12. Summary

The dataset provides 374 historical cosmetics sales transactions
across six countries, 15 products, and 10 salespeople. It provides
useful dimensions for examining sales performance across geography,
products, salespeople, and time.

The data quality assessment found no missing values or exact duplicate
records in the main transaction dataset, and the recorded sales
amounts are consistent with the relationship between boxes shipped
and unit price.

Although the dataset is limited to sales-related information, it
provides a strong quantitative foundation for identifying business
patterns and supporting the subsequent Business Analysis activities
in this case study.