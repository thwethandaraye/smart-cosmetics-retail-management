# Data Quality Report

## 1. Purpose

This report evaluates the quality, consistency, completeness, and reliability of the cosmetics sales dataset used in the Smart Cosmetics Retail Management System project.

Data quality assessment is important because business analysis and system requirements should be based on reliable information. The assessment focuses on completeness, uniqueness, consistency, validity, accuracy, and potential limitations of the dataset.

The analysis was performed using Python, Pandas, and Excel.

---

## 2. Dataset Overview

The dataset contains sales transaction records for a simulated cosmetics retail business.

| Attribute | Value |
|---|---:|
| Number of records | 374 |
| Number of original fields | 7 |
| Number of salespeople | 10 |
| Number of countries | 6 |
| Number of products | 15 |
| Start date | January 1, 2022 |
| End date | August 30, 2022 |
| Total sales amount | $2,909,104.12 |

The original fields are:

- Sales Person
- Country
- Product
- Date
- Amount ($)
- Boxes Shipped
- Unit Price

The dataset represents transaction-level sales information and is primarily suitable for sales performance, product performance, regional analysis, and sales trend analysis.

---

## 3. Data Quality Dimensions

The following dimensions were considered during the assessment:

1. **Completeness** – whether required fields contain missing values.
2. **Uniqueness** – whether duplicate transaction records exist.
3. **Consistency** – whether related values follow the same logical rules.
4. **Validity** – whether values have appropriate data types and reasonable formats.
5. **Accuracy** – whether calculated values are consistent with their source values.
6. **Integrity** – whether relationships between fields are logically maintained.
7. **Timeliness** – whether the available date range is sufficient for the intended analysis.

---

## 4. Completeness Assessment

### 4.1 Missing Values

All seven fields were checked for missing values.

| Field | Missing Values | Status |
|---|---:|---|
| Sales Person | 0 | Pass |
| Country | 0 | Pass |
| Product | 0 | Pass |
| Date | 0 | Pass |
| Amount ($) | 0 | Pass |
| Boxes Shipped | 0 | Pass |
| Unit Price | 0 | Pass |

### Finding

No missing values were identified in the main transaction dataset.

This indicates that the dataset is complete for the available fields and can be used for the planned sales analysis without requiring missing-value imputation.

### Business Implication

Because all transaction records contain values for the required analytical fields, calculations such as total sales, product performance, salesperson performance, regional sales, and monthly trends can be performed without excluding records because of missing data.

---

## 5. Uniqueness Assessment

The dataset was checked for exact duplicate rows.

### Result

- Total records: **374**
- Exact duplicate records: **0**

### Finding

No exact duplicate rows were identified.

### Business Implication

The absence of exact duplicates reduces the risk of overstating sales figures during aggregation.

However, the dataset does not contain a unique transaction or invoice ID. Therefore, it is not possible to determine whether two separate records could represent the same business transaction if their values differ in at least one field.

### Recommendation

A production retail management system should assign a unique identifier to every transaction, such as:

- Transaction ID
- Order ID
- Invoice ID

This would improve transaction traceability and prevent duplicate transactions from being recorded.

---

## 6. Data Type and Format Validation

The data types of the fields were reviewed to determine whether they are appropriate for analysis.

| Field | Data Type | Assessment |
|---|---|---|
| Sales Person | Text | Valid |
| Country | Text | Valid |
| Product | Text | Valid |
| Date | DateTime | Valid |
| Amount ($) | Numeric | Valid |
| Boxes Shipped | Integer | Valid |
| Unit Price | Numeric | Valid |

### Finding

The fields have appropriate data types for their intended purposes.

The `Date` field is stored as a date/time value, allowing time-based analysis. `Amount ($)` and `Unit Price` are numeric values, while `Boxes Shipped` is an integer quantity.

### Business Implication

The current data types support aggregation, filtering, sorting, calculations, and trend analysis.

---

## 7. Numerical Consistency and Accuracy

A key validation performed on the dataset was the relationship between sales amount, quantity shipped, and unit price.

The expected sales amount can be calculated using:

**Calculated Amount = Boxes Shipped × Unit Price**

The calculated value was compared with the recorded `Amount ($)` value for each transaction.

### Validation Result

The calculated amounts were consistent with the recorded sales amounts.

The difference between the recorded amount and the calculated amount was effectively zero across the dataset, allowing for normal floating-point representation.

### Finding

This indicates a strong internal consistency between:

- `Boxes Shipped`
- `Unit Price`
- `Amount ($)`

### Business Implication

This validation increases confidence that the sales amount field follows the expected calculation rule.

In a production system, this relationship should be implemented as a validation rule so that incorrect transaction amounts can be detected before the data is stored or included in reports.

---

## 8. Categorical Value Assessment

The categorical fields were reviewed to identify the number of distinct values.

| Field | Distinct Values |
|---|---:|
| Sales Person | 10 |
| Country | 6 |
| Product | 15 |

The dataset contains a relatively small and manageable number of categorical values.

### Finding

The values are suitable for grouping and aggregation.

For example:

- Sales can be grouped by country.
- Sales can be grouped by salesperson.
- Sales can be grouped by product.
- Sales can be analyzed across different time periods.

### Recommendation

In a production database, entities such as countries, products, and employees should be stored using controlled reference data or unique IDs.

For example:

```text
Country
-------
Country_ID
Country_Name
```
and:
```text
Product
-------
Product_ID
Product_Name
Unit_Price
Category_ID
```
This can reduce inconsistent spelling and improve referential integrity.

## 9. Date Range and Timeliness

The dataset covers transactions from:

**January 1, 2022 to August 30, 2022**

This provides approximately eight months of sales data.

**Finding**

The date range is sufficient for demonstrating short-term sales trends and comparing monthly performance.

However, it is limited for:

- Year-over-year analysis
- Seasonal analysis across multiple years
- Long-term growth analysis
- Annual forecasting
- Identification of recurring seasonal patterns

### Business Implication

The available data can support the current portfolio analysis, but a real retail management system should continuously collect transaction data.

A longer historical dataset would allow management to identify recurring patterns and make more reliable forecasts.

## 10. Business-Level Data Quality Findings

The technical validation shows that the dataset is generally clean. However, data quality also depends on whether the dataset contains the information required for operational decision-making.
Several important business fields are not available.

### Missing Business Information

The dataset does not contain:
- Customer ID
- Customer name or customer profile
- Order ID
- Invoice ID
- Product category
- Inventory on hand
- Reorder point
- Stock level
- Supplier information
- Payment status
- Delivery status
- Order status
- Sales channel
- Discount
- Tax
- Cost of goods sold
- Profit or margin

### Finding

The dataset is sufficient for analyzing historical sales performance but is not sufficient for complete retail operations management.

For example, `Boxes Shipped` indicates the quantity shipped in a transaction, but it does not represent current inventory stock.

Therefore, the dataset cannot be used to confirm:
- stockouts,
- overstocking,
- low-stock conditions,
- reorder requirements,
- inventory turnover,
- or warehouse availability.

### Business Implication

The proposed Smart Cosmetics Retail Management System should capture additional operational data that is not present in the current dataset.
This distinction is important because the project should not treat missing information as evidence of an existing business problem.

## 11. Data Quality Summary

| Quality Dimension	| Result	| Assessment |
|-------------------|-----------|------------|
| Completeness	| No missing values	| Good |
| Uniqueness	| No exact duplicates	| Good |
| Data Types	| Appropriate types	| Good |
| Numerical Consistency	| Amount aligns with quantity × unit price |	Good |
| Categorical Data	| Manageable distinct values	| Good |
| Date Coverage	| January–August 2022	| Limited |
| Transaction Identification	| No unique transaction ID |	Needs improvement |
| Operational Data	| Several business fields unavailable | Needs improvement |
| Inventory Data	| No stock-level information	| Not available |
| Historical Depth	| Less than one year	| Limited |

## 12. Overall Data Quality Assessment

The dataset has good technical quality for the intended exploratory sales analysis. It contains no missing values or exact duplicate rows, uses appropriate data types, and maintains a consistent relationship between the number of boxes shipped, unit price, and recorded sales amount.

However, the dataset has limitations from an operational business-analysis perspective. It does not contain transaction identifiers, customer information, inventory balances, order status, payment information, or other operational attributes required for a complete retail management system.

Therefore, the dataset should be considered reliable for historical sales analysis but incomplete for comprehensive retail operations management.

## 13. Data Quality Recommendations

Based on the assessment, the following improvements are recommended for the proposed system.

### 13.1 Add Unique Transaction Identifiers

Every transaction should have a unique:
- Order ID
- Invoice ID
- Transaction ID
This will improve traceability and duplicate detection.

### 13.2 Introduce Controlled Master Data

Products, employees, countries, and other entities should use unique identifiers and controlled values.
This can reduce inconsistent entries and improve referential integrity.

### 13.3 Add Inventory Data

The system should maintain:
- Current stock quantity
- Reorder point
- Minimum stock level
- Maximum stock level
- Stock movement
- Supplier information
This would allow inventory-related requirements to be supported by actual operational data.

### 13.4 Add Customer and Order Information

Customer and order information should be stored separately from transaction-level sales data.

This would support:
- Customer management
- Order tracking
- Customer analysis
- Sales history
- Order status monitoring

### 13.5 Implement Automated Validation Rules

The proposed system should validate important business rules automatically.

For example:
`Sales Amount = Quantity × Unit Price`

Other validation rules could include:
- Quantity must be greater than zero.
- Unit price must not be negative.
- Product ID must exist in the product table.
- Salesperson ID must exist in the employee table.
- Order ID must be unique.
- Transaction date must be valid.

## 14. Data Quality Controls for the Proposed System

The following controls are recommended:

| Control	| Purpose |
|-----------|---------|
| Required fields	| Prevent incomplete transactions |
| Unique IDs	| Prevent duplicate transaction identification |
| Data type validation	| Prevent invalid values |
| Range validation	| Prevent unreasonable quantities or prices |
| Referential integrity	| Ensure related records exist |
| Calculation validation	| Verify sales amount calculations |
| Controlled vocabulary	| Reduce inconsistent categorical values |
| Audit fields	| Track record creation and modification |
| Automated quality checks	| Detect data problems early |
| Data-quality reporting	| Monitor quality over time |

## 15. Relationship to Business Analysis

The data-quality assessment directly supports the Business Analysis phase of the project.
The assessment identifies not only whether the current dataset is usable, but also what information the future system should capture.

For example:

**Data limitation**
No current inventory balance is available.

↓

**Business implication**
Management cannot determine current stock availability from the dataset.

↓

**Business requirement**
The system should maintain current inventory information.

↓

**Functional requirement**
The system shall update inventory quantities when inventory-affecting transactions are recorded.

↓

**System capability**
Inventory Management Module

This demonstrates how data analysis can be translated into business and system requirements.

## 16. Conclusion

The cosmetics sales dataset is technically suitable for exploratory sales analysis because it is complete, contains no exact duplicate rows, uses appropriate data types, and demonstrates internal numerical consistency.

The main limitations are related to the scope of the available business information rather than basic data quality. The dataset does not contain sufficient information for customer management, inventory management, order tracking, payment monitoring, or other operational functions.

These findings provide a foundation for designing the proposed Smart Cosmetics Retail Management System. The future system should introduce stronger data governance, unique identifiers, validation rules, centralized master data, and additional operational data fields to support reliable business processes and decision-making.