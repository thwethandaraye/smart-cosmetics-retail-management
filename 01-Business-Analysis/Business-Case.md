# Smart Cosmetics Retail Management System
## Business Analysis, Data Insights & Digital Process Improvement Case Study

**Project type:** Business Analysis portfolio case study
**Business domain:** Cosmetics retail / e-commerce
**Dataset:** `cosmetics_sales_data.xlsx`
**Status:** Proposed / simulated business solution
**Important:** The dataset provides sales evidence. Where the dataset does not contain information—such as actual inventory on hand, stockouts, customers, or order status—I treat those as **proposed system requirements**, not proven problems.

## 1. Executive Summary

The cosmetics retail business operates in a data-rich environment where sales transactions are generated across multiple countries, products, salespeople, and dates. However, without a centralized system for managing operational data and transforming it into actionable information, management may face difficulties monitoring sales performance, identifying product trends, comparing regional performance, and making timely decisions.

The provided cosmetics sales dataset contains **374 sales transactions**, covering **6 countries**, **15 products**, and **10 salespeople** from **January 1 to August 30, 2022**. Total recorded sales amount to approximately **$2.91 million**.

Analysis of the dataset shows significant differences in performance across countries, products, salespeople, and months. The USA generated the highest sales at approximately **$628,488**, while India generated the lowest at approximately **$346,435**. At the product level, Tea Tree Moisturizer was the highest-revenue product at approximately **$260,905**, while Charcoal Face Wash generated approximately **$102,733**. Monthly sales also fluctuated substantially, ranging from approximately **$214,025 in February** to **$484,102 in March**.

These findings indicate an opportunity to develop a **Smart Cosmetics Retail Management System** that centralizes sales, product, customer, inventory, and reporting processes and provides management with timely, structured business information.

The proposed solution will combine **business analysis, process improvement, requirements engineering, database design, data analysis, and AI-assisted business analysis**.

## 2. Business Overview

For this case study, the business is modeled as a **fictional cosmetics retailer**, referred to as **Terra Tint Cosmetics**.

Terra Tint Cosmetics sells a range of beauty and personal-care products across multiple markets. Its product portfolio includes skincare, haircare, body-care, and other cosmetic products.

The business works with multiple salespeople and serves customers across different countries. As the business grows, management requires reliable information about:

- Sales performance
- Product performance
- Regional performance
- Salesperson performance
- Sales trends
- Customer orders
- Inventory availability
- Operational processes
- Business performance

The objective of this project is to analyze available sales data and use the findings to design a proposed technology solution that can support these activities.

**Note:** Terra Tint Cosmetics is a simulated business created for this portfolio project. The dataset is used as the analytical evidence for the case study and should not be presented as confidential company data.

## 3. Business Context

The provided dataset represents transactional sales activity.

The primary dataset contains the following fields:

| Field	| Description |
|-------|-------------|
| Sales Person	| Employee responsible for the sale |
| Country	| Country associated with the transaction |
| Product	| Product sold |
| Date	| Transaction date |
| Amount ($)	| Revenue/value of the transaction |
| Boxes Shipped	| Number of boxes shipped |
| Unit Price	| Price per box/unit |

The workbook also contains several supporting sheets:

- `Region`
- `SalesPerson`
- `SalesTrend`
- `InvoiceAmount`
- `DashBoard`

The main transaction sheet contains **374 records and 7 fields**. The data covers **January 1, 2022 through August 30, 2022**.

## 4. Business Problem
### 4.1 Problem Statement

Terra Tint Cosmetics needs a more structured approach to managing and analyzing its sales and operational information.

The available sales data demonstrates differences in performance across markets, products, employees, and time periods. However, simply having transactional data does not automatically provide management with an efficient way to monitor performance or identify areas requiring attention.

The business therefore needs a centralized retail management solution that can:

1. Consolidate operational information.
2. Improve visibility of sales performance.
3. Support product and regional analysis.
4. Reduce dependence on fragmented/manual reporting.
5. Provide reliable management reports.
6. Support future inventory and order management.
7. Enable faster, data-driven decision-making.

## 5. Evidence From the Dataset

The business case is based on the actual sales dataset rather than hypothetical numbers.

### 5.1 Overall Sales

The dataset contains:

- 374 transactions
- 6 countries
- 15 products
- 10 salespeople
- $2,909,104.12 total sales
- January–August 2022 sales period

The dataset contains no missing values and no exact duplicate transaction rows.
Additionally, the `Amount ($)` values correspond to:

`Boxes Shipped × Unit Price`

within floating-point calculation tolerance, providing a useful internal consistency check.
This suggests that the dataset is sufficiently structured for the initial analytical stage of the project.

## 6. Key Business Findings
### 6.1 Uneven Regional Performance

Sales vary considerably between countries.

| Country	| Sales |
|-----------|-------|
| USA	| $628,487.86 |
| New Zealand	| $557,059.85 |
| Australia	| $505,497.64 |
| UK	| $497,061.54 |
| Canada	| $374,562.31 |
| India	| $346,434.92 |

The USA generated the highest recorded sales, while India generated the lowest.
The difference between the highest and lowest markets is approximately **$282,053**.

#### Business implication

Management should be able to quickly compare markets and identify:
- High-performing markets
- Lower-performing markets
- Changes in regional performance
- Products performing well in specific markets
- Opportunities for targeted sales strategies

This supports the need for regional sales analytics within the proposed system.

## 7. Product Performance

Product revenue also varies significantly.

### Highest-revenue products
| Product	| Sales |
|-----------|-------|
| Tea Tree Moisturizer	| $260,905.44 |
| Hydrating Face Serum	| $250,323.33 |
| Hair Repair Oil	| $232,864.77 |
| Anti-Aging Serum	| $232,248.00 |
| Body Butter Cream	| $222,923.58 |

### Lowest-revenue products
| Product	| Sales |
|-----------|-------|
| Charcoal Face Wash	| $102,733.42 |
| Salicylic Acid Cleanser	| $110,329.72 |
| Niacinamide Toner	| $141,841.47 |
| Rose Water Toner	| $151,324.68 |
| Lip Balm Pack	| $170,100.69 |

The highest-revenue product generated approximately **2.54 times** the revenue of the lowest-revenue product.

#### Business implication

Management needs visibility into product performance to support decisions such as:
- Which products should receive greater attention?
- Which products are generating relatively low revenue?
- Which products should be monitored by region?
- Which products might require promotional strategies?
- Which products may require closer inventory monitoring?

The current dataset does **not** contain stock-on-hand, reorder points, or stockout information, so this project will **not claim that inventory shortages currently exist**.
Instead, inventory monitoring will be designed as a **future capability of the proposed system**.

## 8. Salesperson Performance

Sales also differ among salespeople.

| Salesperson	| Sales |
|---------------|-------|
| Olivia D'Souza	| $387,405.91 |
| Sophia Nair	| $319,887.82 |
| Isabella Roy	| $302,087.60 |
| Ethan Reddy	| $298,595.61 |
| Lucas Verma	| $295,166.91 |
| Ananya Gupta	| $293,204.67 |
| Noah Mehta	| $272,188.08 |
| Liam Patel	| $270,960.55 |
| Ava Sharma	| $246,174.28 |
| Mason Kapoor	| $223,432.69 |

Olivia D'Souza generated the highest recorded sales, while Mason Kapoor generated the lowest.

#### Business implication

Management could benefit from a salesperson performance module that allows authorized managers to monitor:
- Revenue by salesperson
- Number of transactions
- Average transaction value
- Performance over time
- Regional performance
- Product sales by salesperson

The objective is not simply to rank employees, but to provide actionable performance information.

## 9. Monthly Sales Fluctuation

Monthly sales show considerable variation.

| Month	| Sales |
|-------|-------|
| January	| $359,762.51 |
| February	| $214,024.56 |
| March	| $484,101.59 |
| April	| $452,650.04 |
| May	| $396,609.09 |
| June	| $367,001.65 |
| July	| $359,655.73 |
| August	| $275,298.95 |

February recorded the lowest monthly sales, while March recorded the highest.
The increase from February to March was approximately **126%**, while sales declined by approximately **43%** from March to August.

#### Business implication

Management should be able to monitor sales trends and investigate significant changes.

A centralized dashboard could provide:
- Daily/monthly sales
- Sales growth/decline
- Sales by country
- Sales by product
- Sales by salesperson
- Trend comparisons
- Filters for specific periods

This would reduce the time required to manually compile and interpret sales information.

## 10. Data Quality and Governance Opportunity

The current dataset itself is relatively clean:
- No missing values were identified.
- No exact duplicate rows were identified.
- `Amount ($)` is mathematically consistent with `Boxes Shipped × Unit Price`.

Therefore, it would be inaccurate to claim that the current business has a serious data-quality problem.
However, as transaction volume increases, maintaining data quality manually can become more difficult.

#### Business implication

The proposed system should therefore include data-quality controls such as:
- Required fields
- Valid product IDs
- Valid salesperson IDs
- Valid dates
- Numeric validation
- Referential integrity
- Duplicate transaction checks
- Consistent product/category records

This changes the argument from:

`"The company currently has bad data."`

to:

`"The company needs scalable controls to maintain data quality as transaction volume and system complexity increase."`

That is much stronger from a Business Analyst perspective.

## 11. Business Problems and Opportunities

Based on the dataset and business context, the project will focus on these **seven core areas**.

| ID	| Business Problem / Opportunity |	Evidence |
|-------|--------------------------------|-----------|
| BP-01	| Uneven regional sales performance	| Sales vary from $346K to $628K |
| BP-02	| Variation in salesperson performance	| Sales vary from $223K to $387K |
| BP-03	| Significant monthly sales fluctuations	| Monthly sales vary from $214K to $484K |
| BP-04	| Uneven product performance	| Products range from ~$103K to ~$261K |
| BP-05	| Need for centralized reporting	| Multiple analytical views are maintained separately |
| BP-06	| Need for scalable data-quality controls	| Current data is clean, but future growth increases control requirements |
| BP-07	| Need for faster, centralized decision support	| Management needs multiple dimensions of analysis |

## 12. Proposed Solution
### Smart Cosmetics Retail Management System

The proposed solution is a centralized retail management platform designed to connect operational processes and analytical reporting.

#### Proposed modules
| Module | Basis |
|--------|-------|
| Product Management | Dataset + proposed system |
| Sales Management | **Strongly supported by dataset** |
| Reporting & Analytics | **Strongly supported by dataset** |
| Customer Management | Proposed system capability |
| Order Management | Proposed system capability |
| Inventory Management | Proposed system capability |
| User Management | Proposed system capability |

The system would use a centralized database to store and manage business information.

## 13. Proposed System Concept
Current conceptual process
```text
Customer
    ↓
Online Store / Social Media
    ↓
Sales Staff
    ↓
Order Record
    ↓
Inventory Check
    ↓
Payment Confirmation
    ↓
Warehouse
    ↓
Delivery
    ↓
Sales Reporting

Potential weaknesses in this conceptual process include:

Repetitive data entry
Separate operational information
Manual reporting
Delayed visibility
Difficulty maintaining consistent information

These are business-process assumptions for the simulated case, not claims that the real dataset proves these activities currently occur.

14. Proposed Future State

The proposed TO-BE architecture is:

                     ┌───────────────────┐
                     │     Customers     │
                     └─────────┬─────────┘
                               │
                               ▼
                     ┌───────────────────┐
                     │ Smart Retail      │
                     │ Management System │
                     └─────────┬─────────┘
                               │
       ┌───────────────┬───────┼────────┬───────────────┐
       ▼               ▼       ▼        ▼               ▼
    Products        Orders   Sales   Inventory       Customers
       │               │       │        │               │
       └───────────────┴───────┼────────┴───────────────┘
                               ▼
                     ┌───────────────────┐
                     │ Central Database  │
                     └─────────┬─────────┘
                               │
                               ▼
                     ┌───────────────────┐
                     │ BI & Reporting    │
                     │ Dashboard         │
                     └───────────────────┘
                               │
                               ▼
                           Management
15. Business Objectives

The project will pursue the following objectives.

BO-01 — Centralize business information

Create a structured system for managing product, customer, order, sales, and inventory information.

BO-02 — Improve sales visibility

Provide management with timely information about sales performance across:

Countries
Products
Salespeople
Time periods
BO-03 — Improve decision-making

Convert transactional data into actionable business information through dashboards and reports.

BO-04 — Reduce repetitive manual processes

Identify opportunities to automate repetitive data-entry and reporting activities.

BO-05 — Improve data consistency

Introduce structured validation and centralized data management.

BO-06 — Support operational scalability

Design a system that can support increased transaction volume and additional products, markets, employees, and customers.

BO-07 — Enable future inventory visibility

Introduce inventory-management capabilities that can eventually support:

Stock levels
Reorder thresholds
Low-stock alerts
Inventory movement
Product availability

Again, these are proposed capabilities, not findings from the current dataset.

16. Expected Business Benefits

If implemented successfully, the proposed system is expected to provide:

1. Better management visibility

Managers can access sales information without manually consolidating multiple reports.

2. Faster decision-making

Dashboards can highlight important changes in sales and product performance.

3. Improved product management

Product-level information can support promotional and portfolio decisions.

4. Improved regional analysis

Management can compare market performance and identify opportunities.

5. Better salesperson monitoring

Managers can monitor performance using consistent metrics.

6. Improved data consistency

Centralized validation can reduce inconsistent or incomplete records.

7. Scalability

A centralized system can support future growth better than disconnected spreadsheets.

17. Project Scope
17.1 In Scope

The project will cover:

Business analysis
Business problem identification
Dataset analysis
Stakeholder analysis
Current-state process modeling
Future-state process modeling
Gap analysis
Business requirements
Functional requirements
Non-functional requirements
User stories
Acceptance criteria
Use-case analysis
Data-flow diagrams
Database design
ERD
SQL database design
Data-quality considerations
Reporting/dashboard requirements
AI-assisted requirements analysis
Test cases
Requirements Traceability Matrix
Portfolio case-study documentation
18. Out of Scope

The following are outside the initial scope:

Building a production-ready e-commerce website
Real payment processing
Real customer accounts
Real logistics integration
Real warehouse hardware
Predictive AI models
Live inventory synchronization
Real company implementation
Actual customer data collection

This keeps the project focused on Business Analysis and system analysis, rather than turning it into a generic software-development project.

19. Key Stakeholders
Stakeholder	Interest / Responsibility
Business Owner	Overall business performance and ROI
General Manager	Business operations and strategic decisions
Sales Manager	Sales performance and salesperson monitoring
Sales Staff	Customer orders and sales records
Inventory Staff	Product availability and stock management
Warehouse Staff	Product movement and fulfillment
Customers	Product availability and order experience
Finance Staff	Sales/payment information
IT/System Administrator	System configuration and access
Business Analyst	Requirements and process analysis
Developers	System implementation
QA/Testers	System validation
20. High-Level Requirements Direction

The business case leads naturally into the next stage of requirements analysis.

Business Requirement 1

BR-01: The business shall maintain centralized information for products, customers, orders, sales, and inventory.

Business Requirement 2

BR-02: The business shall improve visibility into sales and operational performance.

Business Requirement 3

BR-03: The business shall reduce repetitive manual data-management and reporting activities.

Business Requirement 4

BR-04: The business shall provide reliable reports to support management decision-making.

21. Example Functional Requirements

The business requirements can later be translated into functional requirements.

FR-01 — Product Management

The system shall allow authorized users to create, view, update, and deactivate product records.

FR-02 — Order Management

The system shall allow authorized sales staff to record customer orders.

FR-03 — Inventory Update

The system shall update inventory quantities when an order is confirmed.

FR-04 — Low-Stock Monitoring

The system shall identify products whose available quantity falls below a configured threshold.

FR-05 — Sales Reporting

The system shall allow authorized users to view sales reports.

FR-06 — Sales Filtering

The system shall allow users to filter sales information by:

Date
Country
Product
Salesperson
Product category
FR-07 — Dashboard

The system shall provide management with a dashboard displaying key sales indicators.

22. Success Measures

Because this is a proposed system, we should not invent actual improvements such as "sales increased by 20%."

Instead, the project can define measurable success criteria for future implementation.

Area	Proposed KPI
Reporting	Time required to produce standard reports
Data quality	Percentage of records passing validation
Sales visibility	Availability of current sales information
Inventory	Accuracy of inventory records
Process efficiency	Number of manual steps in key workflows
System adoption	Percentage of intended users actively using the system
Decision support	Availability of required management reports
23. Assumptions

This case study makes several assumptions because the dataset only contains sales transactions.

GlowBeauty Cosmetics is a simulated business.
The dataset represents historical sales activity.
Salespeople are employees responsible for sales transactions.
The business requires management reporting.
The business may eventually require centralized inventory management.
Customers and orders exist as part of the proposed retail process.
The current dataset does not contain customer-level or inventory-level information.
Inventory requirements are therefore proposed system capabilities rather than conclusions from the dataset.
24. Constraints

The project has several limitations.

Data limitations

The dataset does not contain:

Customer ID
Customer demographics
Inventory on hand
Stockout records
Reorder points
Supplier information
Cost of goods sold
Profit/margin
Payment information
Delivery information
Order status

Therefore, the analysis is primarily focused on sales revenue and transaction-level performance.

Time limitation

The dataset covers only January–August 2022. Therefore, it should not be treated as a complete annual or current business-performance dataset.

Business limitation

The business is simulated, so stakeholder requirements and operational processes need to be clearly labeled as proposed/assumed rather than actual company processes.

25. Risks
Risk	Impact	Mitigation
Limited historical data	Medium	Clearly define analysis period
Missing inventory data	High	Treat inventory as proposed capability
Missing customer information	Medium	Define customer module conceptually
Incorrect assumptions	High	Validate requirements with stakeholders in a real implementation
Data-quality issues during future growth	Medium	Implement validation rules
User resistance to new system	Medium	Provide training and clear workflows
Scope expansion	High	Define MVP and project boundaries
26. High-Level Project Approach

The project will follow this Business Analysis chain:

ACTUAL DATA
     ↓
DATA FINDINGS
     ↓
BUSINESS IMPLICATION
     ↓
BUSINESS PROBLEM
     ↓
BUSINESS REQUIREMENT
     ↓
FUNCTIONAL REQUIREMENT
     ↓
FEATURE
     ↓
USER STORY
     ↓
ACCEPTANCE CRITERIA
     ↓
TEST CASE

For example:

High variation in product revenue
              ↓
Management needs better product visibility
              ↓
Business requirement for product analytics
              ↓
Product performance reporting
              ↓
Dashboard feature
              ↓
User story for Sales Manager
              ↓
Acceptance criteria
              ↓
Test case

This chain is particularly important because it demonstrates actual Business Analyst thinking, rather than simply creating a dashboard.

27. Proposed MVP

To keep the project realistic, the first version of the system should focus on:

MVP Module 1 — Product Management
Product records
Product categories
Product prices
MVP Module 2 — Sales Management
Sales transactions
Salesperson
Country
Date
Amount
Quantity
MVP Module 3 — Inventory Management
Product stock
Stock threshold
Stock movement
Low-stock notification
MVP Module 4 — Reporting
Sales dashboard
Product performance
Country performance
Salesperson performance
Monthly trends
MVP Module 5 — User Management
Admin
Manager
Sales staff
Inventory staff

Customer management and advanced features can be added later.

28. Business Case Conclusion

The analysis of the provided cosmetics sales dataset demonstrates meaningful variation in regional, product, salesperson, and monthly sales performance. With total recorded sales of approximately $2.91 million across 374 transactions, the dataset provides sufficient evidence to justify a structured analytical and systems-analysis case study.

The strongest business opportunity is not simply to create another sales dashboard. Instead, the business can use the available sales evidence as the starting point for designing a centralized Cosmetics Retail Management System.

The proposed solution would integrate sales, product, customer, inventory, and reporting functions while establishing structured requirements and data-management processes.

The project therefore provides a foundation for progressing from:

Raw sales data → Business insight → Business problem → Requirements → Process design → System design → Database → Testing

This approach will demonstrate practical competencies in Business Analysis, requirements engineering, process modeling, data analysis, database design, and AI-assisted analysis.