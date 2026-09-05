# Acceptance Criteria
## 1. Purpose

This document defines the acceptance criteria for the **Smart Cosmetics Retail Management System**. The criteria specify the conditions that must be satisfied for each major user story to be considered successfully implemented.
The criteria use the **Given–When–Then** format where appropriate.

## 2. Acceptance Criteria
### US-01 — User Login
- Given a registered user has valid credentials, when they submit the login form, then the system shall authenticate the user and provide access to authorized functions.
- Given invalid credentials are entered, when the user attempts to log in, then the system shall reject the login.
Related: FR-01, FR-02

### US-02 — Manage Products
- Given an authorized user, when they enter valid product information, then the system shall save the product record.
- When an existing product is updated, then the system shall save the updated information.
Related: FR-03

### US-03 — Manage Customers
- Given an authorized user, when valid customer information is submitted, then the system shall create a customer record.
- When an existing customer is searched, then the system shall display the matching record.
Related: FR-04

### US-04 — Create Customer Orders
- Given an authorized sales user, when they select a customer, product, and valid quantity, then the system shall create an order.
- Then the system shall calculate the order amount using the applicable product price and quantity.
Then the system shall assign a unique order identifier.
Related: FR-05, FR-09, FR-19

### US-05 — Track Orders
- Given an existing order, when an authorized user views it, then the system shall display its current status.
- When the order status is updated, then the new status shall be saved and displayed.
Related: FR-06

### US-06 — Monitor Inventory
- Given a valid product record, when an authorized inventory user updates its stock quantity, then the system shall save the updated quantity.
- When an inventory-affecting transaction is completed, then the corresponding inventory quantity shall be updated.
Related: FR-07

### US-07 — Receive Low-Stock Alerts
- Given a product has a defined reorder threshold, when its stock quantity falls below that threshold, then the system shall identify the product as low stock.
- Then the product shall be displayed in the low-stock monitoring view.
Related: FR-08

### US-08 — Analyze Sales
- Given sales data exists, when a manager selects a product, country, salesperson, or time period, then the system shall display the relevant sales results.
- Then the displayed totals shall be calculated from the underlying transaction data.
Related: FR-11

### US-09 — Monitor Sales Trends
- Given sales records exist for multiple dates, when a manager selects a time period, then the system shall display sales performance across that period.
- Then the results shall be presented in an appropriate trend format.
Related: FR-12

### US-10 — Compare Product Performance
- Given sales data exists for multiple products, when a manager requests product performance, then the system shall display sales results for the selected products.
- Then products shall be comparable using a consistent sales metric.
Related: FR-13

### US-11 — Compare Regional Performance
- Given sales data exists for multiple countries or regions, when a manager requests regional analysis, then the system shall display sales results by country or region.
- Then the results shall use consistent calculation rules.
Related: FR-14

### US-12 — Monitor Salesperson Performance
- Given sales records are associated with salespeople, when a sales manager requests performance information, then the system shall display sales results for each salesperson.
- Then the manager shall be able to compare salesperson performance.
Related: FR-15

### US-13 — View Management Dashboard
- Given a manager is authorized to access the dashboard, when they open it, then the system shall display key business indicators.
- Then dashboard figures shall reflect the underlying business data.
Related: FR-16

### US-14 — Search and Filter Records
- Given business records exist, when a user enters valid search or filter criteria, then the system shall display matching records.
- When no records match the criteria, then the system shall indicate that no matching records were found.
Related: FR-17

### US-15 — Validate Business Data
- Given required information is missing or invalid, when a user attempts to save a record, then the system shall reject the invalid input and provide an appropriate validation message.
- Given quantity and unit price are valid, when a sales transaction is calculated, then the system shall verify that:
`Sales Amount = Quantity × Unit Price`
Related: FR-10, FR-18

### US-16 — Identify Transactions
- Given a new transaction is created, when it is saved, then the system shall assign a unique transaction or order ID.
- Then the identifier shall allow the transaction to be retrieved and distinguished from other transactions.
Related: FR-19

### US-17 — Generate Reports
- Given the user has reporting access, when they select a report type and relevant filters, then the system shall generate the corresponding report.
- Then the report shall contain data consistent with the underlying records.
Related: FR-20

## 3. Acceptance Criteria Summary

| User Story	| Main Acceptance Condition	| Priority |
|---------------|---------------------------|----------|
| US-01	| Valid users can log in	| High |
| US-02	| Products can be managed	| High |
| US-03	| Customer records can be managed	| High |
| US-04	| Valid orders can be created	| High |
| US-05	| Order status can be tracked	| High |
| US-06	| Inventory can be updated	| High |
| US-07	| Low-stock products are identified	| Medium |
| US-08	| Sales can be analyzed	| High |
| US-09	| Sales trends can be displayed	| High |
| US-10	| Product performance can be compared	| High |
| US-11	| Regional performance can be compared	| High |
| US-12	| Salesperson performance can be reviewed	| Medium |
| US-13	| Dashboard displays key indicators	| High |
| US-14	| Records can be searched and filtered	| High |
| US-15	| Invalid data is rejected	| High |
| US-16	| Transactions receive unique IDs	| High |
| US-17	| Reports can be generated	| High |

## 4. Traceability

The acceptance criteria complete the requirements chain:
**`Business Requirement → Functional Requirement → User Story → Acceptance Criteria`**

For example:
```text
BR-10: Sales Trend Monitoring
↓
FR-12: Generate sales trend reports
↓
US-09: Manager wants to monitor sales trends
↓
Acceptance Criteria: Selected-period sales trends are correctly displayed
```
These acceptance criteria will provide the foundation for the Test-Strategy.md and Test-Cases.md documents in the testing section.