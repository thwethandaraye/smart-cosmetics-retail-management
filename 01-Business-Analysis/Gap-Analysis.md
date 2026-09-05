# Gap Analysis

> **Note:** Terra Tint Cosmetics is a fictional/simulated business created for this portfolio case study. The current-state information and identified gaps are based on the analyzed sales dataset and the simulated AS-IS process. They are not based on interviews with an actual company. Future-state capabilities represent proposed improvements and should be validated with stakeholders before implementation.

## 1. Overview

Gap analysis compares the current state of a business with its desired future state. It identifies the differences between existing capabilities and the capabilities required to achieve business objectives.

For Terra Tint Cosmetics, the gap analysis focuses on sales management, product management, operational information, inventory visibility, reporting, and data-driven decision-making.

The analysis follows the relationship:

**Current State → Gap → Desired State → Required Capability**

The identified gaps will be used as a foundation for defining business requirements and functional requirements for the proposed Smart Cosmetics Retail Management System.

---

## 2. Current State vs. Desired State

### Current State

The simulated current environment relies on sales transaction records and operational activities that may be managed across separate records or manual processes. Historical sales data can be analyzed, but there is limited information about real-time operational activities such as current inventory, order status, payment status, and delivery status.

### Desired State

The desired environment is a centralized retail management system that integrates core business information and processes. Authorized users should be able to access relevant information through a single system, while managers should have access to structured reports and analytics for decision-making.

---

## 3. Identified Business Gaps

### Gap 1: Limited Centralization of Business Information

#### Current State

Business activities such as product management, order processing, inventory checking, customer management, and sales reporting may require separate records or manual coordination within the simulated environment.

#### Gap

There is no defined centralized platform connecting the major business information areas.

#### Desired State

Business information should be maintained within an integrated system with a centralized database.

#### Required Capability

The proposed system should provide centralized management of:

- Products
- Customers
- Orders
- Inventory
- Sales
- Payments
- Employees and user accounts

#### Business Benefit

Centralized information can reduce information fragmentation and make relevant business data easier to access and manage.

---

### Gap 2: Limited Regional Sales Visibility

#### Current State

The dataset contains sales information by country, but management requires analysis to compare regional performance.

For example, the United States generated approximately **$628,488** in sales, while India generated approximately **$346,435** during the analyzed period.

#### Gap

Sales data exists, but there is no defined integrated capability for continuously monitoring regional performance.

#### Desired State

Managers should be able to view and compare sales performance across countries and time periods.

#### Required Capability

The system should provide:

- Country-level sales reports
- Date-based filtering
- Regional performance comparisons
- Sales trend visualization

#### Business Benefit

Improved regional visibility can support management in identifying high- and low-performing markets and making evidence-based decisions.

---

### Gap 3: Limited Salesperson Performance Monitoring

#### Current State

Salesperson performance varies within the dataset. The highest-performing salesperson generated approximately **$387,406**, while the lowest among the analyzed salespeople generated approximately **$223,433**.

#### Gap

The data can be analyzed manually, but a defined system capability for monitoring salesperson performance is not present in the simulated current state.

#### Desired State

Managers should be able to monitor salesperson performance using consistent metrics.

#### Required Capability

The system should support:

- Sales by salesperson
- Transaction count
- Average transaction value
- Sales ranking
- Date-based performance analysis

#### Business Benefit

A centralized performance view can help managers identify performance differences and support targeted management actions.

---

### Gap 4: Limited Product Performance Visibility

#### Current State

Product sales vary considerably. Tea Tree Moisturizer generated approximately **$260,905**, while Charcoal Face Wash generated approximately **$102,733** during the analyzed period.

#### Gap

Product performance information requires analysis before useful comparisons can be made.

#### Desired State

Managers should have direct access to product-level sales information and performance trends.

#### Required Capability

The system should provide:

- Product sales reports
- Product ranking
- Product-level sales trends
- Filtering by product and date
- Product performance comparisons

#### Business Benefit

Improved product visibility can support product management and sales planning.

---

### Gap 5: Limited Sales Trend Monitoring

#### Current State

The dataset shows substantial monthly sales fluctuations. Sales increased from approximately **$214,025 in February to $484,102 in March**, followed by lower sales in subsequent months.

#### Gap

Historical sales data is available, but continuous monitoring and visualization of sales trends are not defined within the current process.

#### Desired State

Management should be able to monitor sales trends through centralized dashboards and reports.

#### Required Capability

The system should provide:

- Monthly sales summaries
- Sales trend charts
- Date-range filtering
- Period-to-period comparisons
- Key performance indicators

#### Business Benefit

Faster access to sales trends can help management identify significant changes and investigate potential causes.

---

### Gap 6: Limited Operational Status Visibility

#### Current State

The simulated process includes order recording, product availability checking, payment confirmation, warehouse processing, and delivery.

However, the sales dataset does not contain operational status information for these activities.

#### Gap

There is no defined centralized mechanism for monitoring the status of operational activities.

#### Desired State

Authorized users should be able to view the current status of relevant orders and operational activities.

#### Required Capability

The proposed system should support status tracking for:

- Orders
- Payments
- Inventory
- Fulfillment
- Delivery

#### Business Benefit

Centralized status information can improve coordination between operational teams and reduce the need to obtain information manually.

---

### Gap 7: Inventory Information Gap

#### Current State

The dataset contains `Boxes Shipped`, but it does not contain stock-on-hand quantities, reorder points, inventory movement history, or stockout records.

Therefore, actual inventory shortages cannot be established from the available data.

#### Gap

The simulated business environment does not have a defined centralized capability for monitoring inventory status.

#### Desired State

Inventory staff should be able to monitor product quantities and inventory changes through a dedicated system.

#### Required Capability

The proposed system should support:

- Current stock quantity
- Inventory transactions
- Stock-in and stock-out records
- Configurable reorder thresholds
- Low-stock alerts
- Inventory history

#### Business Benefit

Improved inventory visibility can support product availability management and future replenishment decisions.

> **Important:** Inventory problems are treated as a proposed business concern rather than a confirmed problem because the available dataset does not contain sufficient inventory information.

---

### Gap 8: Manual Reporting and Analysis

#### Current State

The sales dataset can be analyzed using spreadsheets or analytical tools to produce information about regions, salespeople, products, and sales trends.

#### Gap

Turning raw transaction data into management information may require manual analysis and preparation.

#### Desired State

The system should automatically generate standardized reports and dashboards from centralized data.

#### Required Capability

The system should provide:

- Automated sales summaries
- Interactive dashboards
- Standardized reports
- Filtering and sorting
- Exportable reports
- Key performance indicators

#### Business Benefit

Automated reporting can reduce repetitive analytical work and provide faster access to business information.

---

### Gap 9: Limited Data Quality and Validation Controls

#### Current State

The analyzed dataset is relatively clean. It contains no missing values or exact duplicate records, and the `Amount ($)` values are consistent with `Boxes Shipped × Unit Price`.

However, these checks were performed during analysis rather than through a defined operational data-quality process.

#### Gap

There is no defined system-level mechanism for ensuring data quality as new transactions are entered.

#### Desired State

The proposed system should apply validation rules when users enter or update business information.

#### Required Capability

The system should provide:

- Required-field validation
- Data-type validation
- Valid product and customer references
- Quantity validation
- Price validation
- Duplicate prevention where appropriate
- Audit information for important changes

#### Business Benefit

Preventive validation can reduce the risk of incorrect or inconsistent business data as transaction volume increases.

---

## 4. Gap Analysis Matrix

| ID | Current State | Gap | Desired State | Required Capability | Priority |
|---|---|---|---|---|---|
| GAP-01 | Business information may be distributed across separate records | Lack of centralized information | Integrated business information | Centralized database and modules | High |
| GAP-02 | Regional sales require analysis | Limited regional visibility | Direct regional performance monitoring | Regional sales analytics | Medium |
| GAP-03 | Salesperson performance varies | Limited performance monitoring | Centralized salesperson performance view | Sales performance reporting | Medium |
| GAP-04 | Product performance differs significantly | Limited product visibility | Direct product performance monitoring | Product analytics | Medium |
| GAP-05 | Monthly sales fluctuate | Limited trend monitoring | Continuous sales trend visibility | Sales dashboard and trend reports | High |
| GAP-06 | Operational activities have multiple statuses | Limited status visibility | Centralized operational tracking | Order/payment/fulfillment status | High |
| GAP-07 | No stock-on-hand information in dataset | Inventory information gap | Centralized inventory visibility | Inventory management and alerts | High |
| GAP-08 | Analysis requires manual preparation | Manual reporting dependency | Automated reporting | Dashboards and reports | High |
| GAP-09 | Data quality checks are performed during analysis | Limited preventive validation | System-level data validation | Validation and data-quality controls | Medium |

---

## 5. Gap Prioritization

The gaps are prioritized according to their potential business impact, number of processes affected, and relevance to the proposed system.

### High Priority

**GAP-01: Centralized Business Information**

A centralized information structure is foundational because other system capabilities depend on reliable access to shared business data.

**GAP-05: Sales Trend Monitoring**

Sales monitoring is important because the dataset demonstrates significant changes in monthly sales performance.

**GAP-06: Operational Status Visibility**

Order, payment, fulfillment, and delivery information can affect multiple operational roles.

**GAP-07: Inventory Information Gap**

Inventory visibility is important for product availability and order fulfillment, although actual inventory problems have not been established from the current dataset.

**GAP-08: Automated Reporting**

Management requires timely access to business information, and automated reporting can reduce repetitive manual analysis.

### Medium Priority

**GAP-02: Regional Sales Visibility**

Regional analysis supports management decision-making but depends on the underlying sales data and reporting capabilities.

**GAP-03: Salesperson Performance Monitoring**

Performance monitoring supports sales management and staff evaluation.

**GAP-04: Product Performance Visibility**

Product analysis supports product and sales decisions.

**GAP-09: Data Quality and Validation**

Data validation becomes increasingly important as transaction volume and system usage grow.

---

## 6. Capability Gap Summary

The identified gaps can be grouped into five major capability areas.

### 6.1 Data Management

Required capabilities:

- Centralized database
- Structured business entities
- Data validation
- Data integrity controls
- Controlled access

### 6.2 Operational Management

Required capabilities:

- Order management
- Inventory management
- Payment status
- Fulfillment tracking
- Delivery status

### 6.3 Sales Management

Required capabilities:

- Sales transaction management
- Salesperson performance monitoring
- Regional analysis
- Product performance analysis

### 6.4 Reporting and Analytics

Required capabilities:

- Dashboards
- Sales reports
- Trend analysis
- Filtering
- Performance indicators
- Exportable reports

### 6.5 Decision Support

Required capabilities:

- Centralized business information
- Timely access to data
- Comparative analysis
- Exception identification
- Data-driven management reporting

---

## 7. From Business Gaps to System Capabilities

The gap analysis provides the bridge between the business problem and the proposed technology solution.

| Business Gap | System Capability |
|---|---|
| Fragmented information | Centralized database |
| Limited regional visibility | Regional sales dashboard |
| Limited salesperson monitoring | Sales performance module |
| Limited product visibility | Product analytics |
| Limited sales trend monitoring | Sales trend dashboard |
| Limited operational visibility | Order and status management |
| Inventory information gap | Inventory management module |
| Manual reporting | Automated reporting and BI |
| Limited preventive data validation | Data validation rules |

These capabilities will later be translated into detailed business requirements and functional requirements.

---

## 8. Business Requirements Derived from the Gap Analysis

The gap analysis provides the initial basis for the following high-level business requirements.

### BR-01: Centralized Business Information

The system should provide a centralized platform for managing core business information.

### BR-02: Sales Performance Visibility

The system should provide management with visibility into sales performance by product, salesperson, country, and time period.

### BR-03: Operational Status Visibility

The system should allow authorized users to monitor relevant order and operational statuses.

### BR-04: Inventory Visibility

The system should provide authorized users with access to current inventory information and configurable stock-level thresholds.

### BR-05: Automated Business Reporting

The system should provide standardized reports and dashboards for management decision-making.

### BR-06: Data Quality and Validation

The system should apply appropriate validation and integrity controls to business data.

### BR-07: Improved Decision Support

The system should transform operational data into structured information that supports evidence-based business decisions.

> These are high-level business requirements. Detailed functional requirements will be defined separately in `Functional-Requirements.md`.

---

## 9. Gap Closure Strategy

The proposed Smart Cosmetics Retail Management System will address the identified gaps through an integrated set of modules.

### Product Management

Addresses:

- Product information fragmentation
- Limited product visibility
- Product data consistency

### Customer Management

Addresses:

- Limited centralized customer information
- Difficulty maintaining customer records

### Order Management

Addresses:

- Order information fragmentation
- Limited order status visibility
- Manual order coordination

### Inventory Management

Addresses:

- Inventory information gap
- Limited stock visibility
- Lack of configurable low-stock monitoring

### Sales Management

Addresses:

- Salesperson performance monitoring
- Regional sales monitoring
- Sales transaction management

### Reporting and Analytics

Addresses:

- Manual reporting
- Limited trend monitoring
- Limited management visibility
- Product and regional performance analysis

### User Management

Addresses:

- Controlled access to business information
- Role-based system access
- Protection of sensitive operational data

---

## 10. Expected Future-State Improvements

If implemented successfully, the proposed system is expected to provide the following improvements:

- A centralized source of business information
- Faster access to operational data
- Improved visibility into sales performance
- More structured product and salesperson analysis
- Better inventory information visibility
- Reduced dependency on manual reporting
- Improved data consistency through validation
- More efficient information sharing between business functions
- Stronger support for data-driven decision-making

These are **expected benefits**, not measured results. Actual improvements would need to be evaluated after implementation using defined performance indicators.

---

## 11. Key Performance Indicators for Future Evaluation

To evaluate whether the identified gaps have been successfully addressed, the business could measure:

| KPI | Purpose |
|---|---|
| Report preparation time | Measure efficiency of reporting |
| Order processing time | Measure operational efficiency |
| Data-entry error rate | Measure data quality |
| Inventory update accuracy | Measure inventory information reliability |
| Low-stock detection time | Measure inventory monitoring |
| Dashboard/report access time | Measure information availability |
| Sales reporting frequency | Measure reporting capability |
| Order status visibility | Measure operational transparency |

These KPIs are proposed evaluation measures and are not available in the current dataset.

---

## 12. Key Business Analysis Insight

The gap analysis demonstrates that the main opportunity is to move from a primarily transaction-oriented and potentially fragmented information environment toward an integrated, data-driven retail management environment.

The current dataset provides useful evidence of sales differences across countries, products, salespeople, and months. However, it does not contain sufficient information about customers, inventory, payments, delivery, suppliers, costs, or profitability.

Therefore, the proposed system should combine **operational management** with **business intelligence**, rather than functioning only as a sales dashboard.

The desired transformation can be represented as:

**Fragmented / Limited Information**
  
↓  

**Centralized Business Data**
  
↓  

**Integrated Business Processes**
  
↓  

**Automated Reporting & Analytics**
  
↓  

**Improved Visibility**
  
↓  

**Data-Driven Decision-Making**

---

## 13. Transition to Requirements Analysis

The gap analysis identifies what capabilities are missing or need improvement. The next stage is to define exactly what the proposed system must do to close those gaps.

The analysis will therefore progress from:

**Pain Points → Gaps → Business Requirements → Functional Requirements → User Stories → Acceptance Criteria → Test Cases**

This creates a traceable relationship between the original business problems and the proposed system functionality.