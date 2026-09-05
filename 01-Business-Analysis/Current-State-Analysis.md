# Current-State Analysis

> **Note:** Terra Tint Cosmetics is a fictional/simulated business
> created for this case study. The current-state processes described
> below represent assumptions developed for Business Analysis and
> system-design purposes. They are not based on direct observation or
> interviews with a real organization.

## 1. Current-State Overview

The current-state analysis describes how the simulated Terrs Tint
Cosmetics business is assumed to manage its sales and operational
activities before the implementation of the proposed Smart Cosmetics
Retail Management System.

The current environment involves several interconnected activities,
including customer interaction, order recording, product availability
checking, payment confirmation, order fulfillment, delivery, sales
recording, and management reporting.

Information is assumed to move between different business activities
and users rather than being managed through one centralized
management system.

The purpose of this analysis is to establish the AS-IS baseline,
identify potential process inefficiencies, and provide a foundation
for the subsequent pain-point and gap analyses.

## 2. Current Business Process

The simulated current business process begins when a customer selects
a product and places an order. Sales staff receive and record the
order before checking product availability. After payment is
confirmed, the order is passed to the warehouse for fulfillment and
delivery.

The completed transaction is then recorded as sales information and
used for reporting and analysis.

The overall process can be represented as follows:

```text
Customer
    ↓
Online Store / Social Media
    ↓
Sales Staff
    ↓
Record Order
    ↓
Check Product Availability
    ↓
Confirm Payment
    ↓
Warehouse
    ↓
Delivery
    ↓
Record Sales Transaction
    ↓
Sales Reporting
```

## 3. AS-IS Process Description

### 3.1 Customer Interaction

The customer browses available cosmetics products through an online
store or social media channel and selects the products they want to
purchase.

The customer provides the information required to process the order,
such as selected products, quantities, and delivery information.

### 3.2 Sales Staff

Sales staff receive customer orders and confirm the requested
products and quantities.

They are responsible for recording order information and coordinating
the next stages of the sales process.

### 3.3 Order Recording

The order information is recorded so that the requested products,
quantities, and customer information can be processed.

In the simulated current state, order information may be recorded
through operational records rather than through a single integrated
retail management platform.

### 3.4 Product Availability Check

Before fulfillment, product availability is checked to determine
whether the requested products can be supplied.

This activity requires sales and inventory-related information to be
available to the staff processing the order.

```text
Order Received
      ↓
Check Product Availability
      ↓
Product Available?
    ↙       ↘
  Yes        No
   ↓          ↓
Continue    Notify Customer
   ↓
Payment
```

### 3.5 Payment Confirmation

After product availability is confirmed, payment information is
checked and the order is confirmed for fulfillment.

The payment confirmation acts as a control point before the order is
sent to the warehouse.

### 3.6 Order Fulfillment

The warehouse receives the confirmed order and prepares the required
products.

Warehouse staff use the order information to verify the products and
quantities required for fulfillment.

### 3.7 Delivery

After the order has been prepared, it is transferred to the delivery
process.

The order is then delivered to the customer.

### 3.8 Sales Transaction Recording

The completed transaction is recorded as sales information.

The sales dataset used in this case study represents this type of
transaction-level information and contains fields such as sales
person, country, product, date, sales amount, boxes shipped, and unit
price.

### 3.9 Sales Reporting

Sales transaction data is analyzed to produce information about
business performance.

Management can use sales information to examine performance by
product, country, salesperson, and time period.

However, repeated analysis of transaction-level data can require
additional manual effort, particularly as the amount of data
increases.

## 4. Current Information Flow

The major information flow in the simulated current state is:

```text
Customer Information
        ↓
Sales Staff
        ↓
Order Information
        ↓
Product Availability
        ↓
Payment Confirmation
        ↓
Fulfillment Information
        ↓
Sales Transaction
        ↓
Sales Reporting
        ↓
Management Decision-Making
```

Information is therefore passed through several stages before it
becomes available for management analysis.

## 5. Current Data and Reporting Environment

The available sales dataset provides transaction-level information
that can be analyzed across multiple business dimensions.

The current analysis can be performed using:

- Salesperson
- Country
- Product
- Date
- Sales Amount
- Boxes Shipped
- Unit Price

These fields support analysis of sales performance and trends.

For example, management can analyze:

- Total sales by country
- Total sales by product
- Sales by salesperson
- Monthly sales trends
- Transaction volume
- Product sales contribution

The dataset therefore demonstrates the availability of useful sales
information but does not provide an integrated view of all business
operations.

## 6. Current-State Observations

The current-state analysis identifies several areas that may require
improvement.

### 6.1 Information Fragmentation

Different operational activities require different types of
information, including customer, order, product, inventory, payment,
fulfillment, and sales information.

Without a centralized system, information can become distributed
across different operational activities and records.

### 6.2 Limited Operational Visibility

Sales information is available for analysis, but the dataset does
not contain integrated customer, inventory, payment, or delivery
information.

This limits the ability to obtain a complete view of the customer's
order lifecycle from a single source.

### 6.3 Reporting Dependency on Transaction Data

Sales reporting requires transaction data to be organized and
analyzed according to different business dimensions.

As transaction volume increases, manually preparing or repeatedly
analyzing reports may become less efficient.

### 6.4 Limited Real-Time Performance Monitoring

The available dataset represents historical transactions rather than
a real-time operational system.

Consequently, management analysis is primarily retrospective rather
than based on continuously updated operational information.

### 6.5 Limited Inventory Information

The available dataset includes `Boxes Shipped`, but it does not
include stock-on-hand quantities, reorder points, stockout records,
or inventory movements.

Therefore, actual inventory problems cannot be established from the
dataset.

However, the absence of integrated inventory information represents
an opportunity for the proposed system to provide centralized
inventory visibility.

## 7. Current-State Business Evidence

The sales data provides several observations that are relevant to the
current-state analysis.

### Geographic Performance

Sales performance differs across the six countries represented in
the dataset. The United States has the highest recorded sales,
followed by New Zealand and Australia.

This demonstrates the importance of geographic sales monitoring.

### Product Performance

Sales contribution varies considerably across the 15 products in the
dataset. Tea Tree Moisturizer records the highest product sales,
while Charcoal Face Wash records the lowest.

This indicates a need for effective product-level performance
monitoring.

### Salesperson Performance

The dataset contains transactions associated with 10 salespeople.
Sales contribution varies between salespeople, providing an
opportunity to monitor individual sales performance.

### Monthly Sales Trends

Sales also vary across the analyzed months. There is a substantial
increase from February to March, followed by lower monthly sales
toward August.

This demonstrates the value of monitoring sales trends over time.

## 8. AS-IS Process Risks

The current-state process presents several potential operational
risks:

| Risk ID | Current-State Risk | Potential Business Impact |
|---|---|---|
| R-01 | Information distributed across processes | Reduced information visibility |
| R-02 | Repeated manual data handling | Increased processing effort |
| R-03 | Separate sales analysis activities | Slower access to business insights |
| R-04 | Limited integrated order visibility | Difficulty monitoring order progress |
| R-05 | Limited inventory information | Difficulty monitoring product availability |
| R-06 | Historical rather than real-time analysis | Delayed identification of performance changes |
| R-07 | Increasing data volume | Greater reporting and data-management effort |

These risks are potential process risks identified from the simulated
business environment. They should be validated with stakeholders in
a real implementation.

## 9. Current-State Summary

The simulated AS-IS process involves multiple activities from
customer interaction through order fulfillment and sales reporting.
Although sales transaction data provides useful information for
performance analysis, the available data does not provide an
integrated view of the complete retail operation.

The current-state analysis therefore indicates opportunities to
improve information centralization, operational visibility, sales
reporting, and process coordination.

These observations will be used to identify specific pain points in
the next stage of the Business Analysis process.

## 10. Transition to Pain-Point Analysis

The relationship between the current state and the next analysis
stage is:

```text
Current-State Process
        ↓
Current-State Observations
        ↓
Potential Risks / Inefficiencies
        ↓
Pain Points
        ↓
Business Requirements
        ↓
Proposed Future State
```

The identified pain points will be documented and prioritized in
`Pain-Points.md`.