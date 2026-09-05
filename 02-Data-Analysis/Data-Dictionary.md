# Data Dictionary

> **Project context:** This data dictionary documents the fields contained in the `cosmetics_sales_data` worksheet of the cosmetics sales dataset used for the Smart Cosmetics Retail Management System case study. The dataset is used for educational and portfolio purposes.

## 1. Overview

A data dictionary provides a structured description of the data fields used within a dataset. It defines the meaning, format, analytical role, and business relevance of each field.

The main dataset contains **374 transaction records** and **7 original fields** covering salespeople, countries, products, transaction dates, sales amounts, quantities shipped, and unit prices.

The data can be grouped into:

- **Dimensions:** Sales Person, Country, Product, Date
- **Measures:** Amount ($), Boxes Shipped, Unit Price

---

## 2. Dataset Structure

| Attribute | Description |
|---|---|
| Dataset Name | Cosmetics Sales Dataset |
| Main Worksheet | `cosmetics_sales_data` |
| Number of Records | 374 |
| Number of Original Fields | 7 |
| Date Range | January 1, 2022 – August 30, 2022 |
| Salespeople | 10 |
| Countries | 6 |
| Products | 15 |
| Primary Analytical Subject | Cosmetics retail sales transactions |

---

## 3. Field Definitions

| Field Name | Data Type | Category | Description | Example |
|---|---|---|---|---|
| `Sales Person` | String | Dimension | Name of the salesperson associated with the transaction | Olivia D'Souza |
| `Country` | String | Dimension | Country or market associated with the transaction | United States |
| `Product` | String | Dimension | Name of the cosmetic product sold | Tea Tree Moisturizer |
| `Date` | Date/Datetime | Dimension | Date on which the sales transaction occurred | 2022-03-15 |
| `Amount ($)` | Float | Measure | Total monetary value of the transaction in US dollars | 1250.00 |
| `Boxes Shipped` | Integer | Measure | Number of product boxes shipped in the transaction | 25 |
| `Unit Price` | Float | Measure | Selling price per box/unit in US dollars | 50.00 |

---

## 4. Detailed Field Descriptions

### 4.1 Sales Person

**Field Name:** `Sales Person`

**Data Type:** String / Categorical

**Role:** Dimension

**Description:**  
Identifies the salesperson associated with each sales transaction.

**Analytical Uses:**

- Sales performance comparison
- Salesperson ranking
- Transaction-count analysis
- Average transaction value
- Performance reporting

**Example Values:**

- Olivia D'Souza
- Ethan Reddy
- Ava Sharma
- Mason Kapoor

**Business Relevance:**

This field allows management to compare sales performance between salespeople and identify differences in revenue and transaction activity.

**Data Quality Considerations:**

- Names should be stored consistently.
- Spelling and capitalization should be standardized.
- Each salesperson should have a unique identifier in a production system rather than relying only on names.

---

### 4.2 Country

**Field Name:** `Country`

**Data Type:** String / Categorical

**Role:** Dimension

**Description:**  
Identifies the country or geographic market associated with a transaction.

**Analytical Uses:**

- Regional sales analysis
- Market comparison
- Geographic performance reporting
- Sales-share analysis
- Market trend analysis

**Example Values:**

- United States
- New Zealand
- Australia
- United Kingdom
- Canada
- India

**Business Relevance:**

Country-level analysis helps management understand differences in sales performance between geographic markets.

**Data Quality Considerations:**

- Country names should use standardized values.
- A production system could use standardized country codes such as ISO country codes.

---

### 4.3 Product

**Field Name:** `Product`

**Data Type:** String / Categorical

**Role:** Dimension

**Description:**  
Identifies the cosmetic product associated with the transaction.

**Analytical Uses:**

- Product performance analysis
- Product ranking
- Revenue comparison
- Product sales trends
- Product-level reporting

**Example Values:**

- Tea Tree Moisturizer
- Hydrating Face Serum
- Hair Repair Oil
- Anti-Aging Serum
- Body Butter Cream
- Charcoal Face Wash

**Business Relevance:**

Product-level information allows management to identify products with relatively high or low sales and monitor product performance.

**Data Quality Considerations:**

- Product names should be standardized.
- A production database should use a unique `Product ID`.
- Product categories should ideally be stored separately from product names.

---

### 4.4 Date

**Field Name:** `Date`

**Data Type:** Date/Datetime

**Role:** Dimension

**Description:**  
Represents the date on which the sales transaction occurred.

**Analytical Uses:**

- Daily sales analysis
- Monthly sales analysis
- Time-series analysis
- Trend identification
- Date-range filtering

**Range in Dataset:**

`2022-01-01` to `2022-08-30`

**Business Relevance:**

Transaction dates allow management to monitor sales changes over time and identify periods of higher or lower sales activity.

**Data Quality Considerations:**

- Dates should use a consistent date format.
- Invalid or future dates should be prevented during data entry.
- A production analytics system may use a dedicated date dimension for more advanced reporting.

---

### 4.5 Amount ($)

**Field Name:** `Amount ($)`

**Data Type:** Float / Decimal

**Role:** Measure

**Description:**  
Represents the total monetary value of a sales transaction in US dollars.

**Analytical Uses:**

- Total revenue calculation
- Average transaction value
- Country sales
- Product sales
- Salesperson performance
- Monthly sales trends
- Sales-share calculations

**Example:**

If 20 boxes are shipped at a unit price of $50:

`Amount ($) = 20 × $50 = $1,000`

**Business Relevance:**

This is the primary financial measure used to evaluate sales performance in the dataset.

**Data Quality Considerations:**

The value should be consistent with:

`Boxes Shipped × Unit Price`

The analysis notebook checks this relationship.

**Important Limitation:**

`Amount ($)` represents sales revenue, not profit. Product cost, operating costs, and profit margin are not included in the dataset.

---

### 4.6 Boxes Shipped

**Field Name:** `Boxes Shipped`

**Data Type:** Integer

**Role:** Measure

**Description:**  
Represents the number of product boxes shipped for a transaction.

**Analytical Uses:**

- Quantity analysis
- Sales-volume analysis
- Product demand analysis
- Shipment-volume analysis
- Quantity-based performance comparisons

**Example:**

`Boxes Shipped = 25`

means that 25 boxes were shipped for the transaction.

**Business Relevance:**

The quantity shipped provides information about transaction volume and can be used alongside unit price and sales amount.

**Data Quality Considerations:**

- Values should be whole numbers.
- Values should normally be greater than zero for completed sales transactions.
- Negative values should only be permitted if a defined return/refund process exists.

**Important Limitation:**

`Boxes Shipped` does **not** represent current inventory or stock-on-hand.

Therefore, this field cannot be used by itself to determine:

- Current stock levels
- Stockouts
- Reorder requirements
- Inventory shortages

---

### 4.7 Unit Price

**Field Name:** `Unit Price`

**Data Type:** Float / Decimal

**Role:** Measure

**Description:**  
Represents the selling price of one product box/unit in US dollars.

**Analytical Uses:**

- Revenue validation
- Price comparison
- Product pricing analysis
- Revenue calculation

**Example:**

If:

`Boxes Shipped = 20`

and:

`Unit Price = $50`

then:

`Amount ($) = $1,000`

**Business Relevance:**

Unit price helps determine transaction value and provides a basic measure for comparing product pricing.

**Data Quality Considerations:**

- Values should normally be greater than zero.
- Currency should be consistently recorded in US dollars.
- A production system should maintain product pricing history if prices can change over time.

---

## 5. Derived Fields Used in Analysis

The original dataset contains seven fields. Additional fields can be derived during analysis to support reporting.

### 5.1 Calculated Amount

**Formula:**

```text
Calculated Amount = Boxes Shipped × Unit Price
```

**Purpose:**

Used to validate the recorded **Amount ($)** value.

**Example:**
```text
Boxes Shipped = 10
Unit Price = $25
Calculated Amount = $250
```
The calculated value can then be compared with the recorded transaction amount.

### 5.2 Amount Difference

**Formula:**
```text
Amount Difference = ABS(Amount ($) - Calculated Amount)
```
**Purpose:**

Used as a data-quality check to identify potential inconsistencies between transaction amount, quantity, and unit price.

### 5.3 Month

**Derived From:**

`Date`

**Purpose:**

Used to aggregate sales into monthly periods for time-series analysis.

**Example:**
```text
Date: 2022-03-15
Month: 2022-03
```
### 5.4 Sales Share (%)

**Formula:**
```text
Sales Share (%) = ( Category Sales / Total Sales ) × 100
```
**Purpose:**

Used to determine the percentage contribution of a country, product, or other category to total sales.

## 6. Dimension and Measure Classification
### Dimensions

Dimensions describe the characteristics by which sales can be grouped or filtered.

| Dimension	| Purpose |
|-----------|---------|
| Sales Person	| Analyze performance by salesperson |
| Country	| Analyze geographic performance |
| Product	| Analyze product performance |
| Date	| Analyze sales over time |

### Measures

Measures are numerical values that can be aggregated or analyzed.

| Measure	| Purpose |
|-----------|---------|
| Amount ($)	| Measure transaction revenue |
| Boxes Shipped	| Measure quantity shipped |
| Unit Price	| Measure selling price |

## 7. Key Relationships Between Fields

The main quantitative relationship in the dataset is:

`Boxes Shipped × Unit Price = Amount ($)`

This relationship provides a basic internal consistency check.

For example:
```text
Boxes Shipped = 20
Unit Price = $50

20 × $50 = $1,000

Amount ($) should therefore be approximately $1,000.
```
The relationship can be represented as:
```text
Product
   │
   ├── Unit Price
   │
   └── Boxes Shipped
          │
          ▼
     Amount ($)
```

## 8. Business Analysis Mapping

Each field supports specific business-analysis activities.

| Field	| Business Analysis Use |
|-------|-----------------------|
| Sales Person	| Sales performance requirements |
| Country	| Regional reporting requirements |
| Product	| Product management and analytics |
| Date	| Trend monitoring and reporting |
| Amount ($)	| Sales performance KPIs |
| Boxes Shipped	| Quantity and shipment analysis |
| Unit Price	| Pricing and transaction validation |

## 9. Data Model Considerations

Although the current dataset is a flat transaction table, a production retail management system should separate major business entities.

A possible conceptual structure is:

Customer
    │
    ▼
Order ──────── Payment
    │
    ▼
Order Item
    │
    ▼
Product ───── Category
    │
    ▼
Inventory

Employee / Salesperson
    │
    ▼
Order

Order
    │
    ▼
Delivery

This structure would reduce unnecessary duplication and allow the system to manage operational information that is not available in the current dataset.

## 10. Data Fields Missing From the Current Dataset

The current dataset is useful for sales analysis but does not contain several fields that would be required for a more complete retail management system.

| Missing Data	| Potential Purpose |
|---------------|-------------------|
| Customer ID	| Identify customers |
| Customer Name	| Customer management |
| Customer Contact	| Customer communication |
| Order ID	| Uniquely identify orders |
| Product ID	| Uniquely identify products |
| Product Category	| Product grouping |
| Stock Quantity	| Inventory monitoring |
| Reorder Level	| Replenishment monitoring |
| Supplier ID	| Supplier management |
| Payment Status	| Payment tracking |
| Delivery Status	| Delivery tracking |
| Order Status	| Order lifecycle management |
| Product Cost	| Cost analysis |
| Profit	| Profitability analysis |
| Profit Margin	| Financial performance analysis |

These missing fields should not be added to the existing dataset as invented values. Instead, they should be captured as requirements for the proposed system or identified as additional data sources needed for future analysis.

## 11. Data Quality Rules for the Proposed System

Based on the current analysis, the future system should consider the following validation rules.

| Rule ID	| Validation Rule	| Reason |
|-----------|-------------------|--------|
| DQ-01	| Salesperson must be a valid registered user	| Prevent invalid salesperson records |
| DQ-02	| Country must use an approved country value	| Maintain geographic consistency |
| DQ-03	| Product must exist in the product master	| Prevent invalid product references |
| DQ-04	| Transaction date must be valid	| Prevent invalid dates |
| DQ-05	| Boxes Shipped must be a valid positive quantity for sales	| Prevent invalid quantities |
| DQ-06	| Unit Price must be greater than zero	| Prevent invalid pricing |
| DQ-07	| Amount should equal quantity × unit price	| Maintain transaction consistency |
| DQ-08	| Required fields cannot be blank	| Reduce incomplete records |
| DQ-09	| Product and customer references should use unique IDs	| Improve data integrity |
| DQ-10	| Important transaction changes should be auditable	| Support accountability and traceability |

## 12. Data Dictionary Summary

The dataset provides a useful foundation for analyzing sales performance across four major dimensions:

**Who:** Sales Person

**Where:** Country

**What:** Product

**When:** Date

These dimensions are combined with three numerical measures:

**How much revenue:** Amount ($)

**How much quantity:** Boxes Shipped

**At what price:** Unit Price

This structure supports descriptive analysis and provides evidence for the Business Analysis case study.

However, the dataset represents only a subset of the information required by a complete cosmetics retail management system. Customer, order, inventory, payment, delivery, supplier, and profitability information would need to be captured separately.

Therefore, the data dictionary serves two purposes:

1. It defines the data currently available for analysis.
2. It identifies information requirements for the proposed future-state system.