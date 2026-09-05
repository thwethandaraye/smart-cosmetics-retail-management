# Functional Requirements
## 1. Purpose

This document defines the functional requirements for the proposed **Smart Cosmetics Retail Management System**. These requirements describe the specific functions the system should provide to support the business requirements identified during the analysis.

## 2. Functional Requirements

### FR-01 — User Authentication
The system shall allow authorized users to log in using valid credentials.

### FR-02 — Role-Based Access
The system shall provide access to system functions based on the user's assigned role.

### FR-03 — Product Management
The system shall allow authorized users to create, view, update, and deactivate product records.

### FR-04 — Customer Management
The system shall allow authorized users to create, view, update, and search customer records.

### FR-05 — Order Creation
The system shall allow authorized sales staff to create customer orders containing one or more products and quantities.

### FR-06 — Order Tracking
The system shall allow authorized users to view and update the status of an order.

### FR-07 — Inventory Management
The system shall maintain the current inventory quantity for each product and update inventory when relevant transactions are recorded.

### FR-08 — Low-Stock Monitoring
The system shall identify products whose stock quantity falls below the configured reorder threshold.

### FR-09 — Sales Recording
The system shall record sales transactions with relevant information including product, quantity, unit price, salesperson, date, and total amount.

### FR-10 — Sales Validation
The system shall validate that the recorded sales amount is consistent with the quantity and unit price.
**Formula:**
`Sales Amount = Quantity × Unit Price`

### FR-11 — Sales Analysis
The system shall allow authorized users to analyze sales by product, country, salesperson, and time period.

### FR-12 — Sales Trend Reporting
The system shall generate sales reports showing performance across selected time periods.

### FR-13 — Product Performance Reporting
The system shall generate reports comparing sales performance among products.

### FR-14 — Regional Performance Reporting
The system shall generate reports comparing sales performance across countries or regions.

### FR-15 — Salesperson Performance Reporting
The system shall provide sales performance information for individual salespeople.

### FR-16 — Dashboard
The system shall provide a management dashboard displaying key business indicators such as total sales, product performance, regional performance, salesperson performance, sales trends, and inventory alerts.

### FR-17 — Data Search and Filtering
The system shall allow authorized users to search and filter business records using relevant criteria such as date, product, country, salesperson, and order status.

### FR-18 — Data Validation
The system shall validate required fields, data types, numeric ranges, dates, and relationships between related records before saving data.

### FR-19 — Transaction Identification
The system shall automatically assign a unique identifier to each order or sales transaction.

### FR-20 — Reporting
The system shall allow authorized users to generate and view operational and analytical reports.

## 3. Functional Requirements Summary

| ID	| Requirement	| Priority |
|-------|---------------|----------|
| FR-01	| User authentication	| High |
| FR-02	| Role-based access	| Medium |
| FR-03	| Product management	| High |
| FR-04	| Customer management	| High |
| FR-05	| Order creation	| High |
| FR-06	| Order tracking	| High |
| FR-07	| Inventory management	| High |
| FR-08	| Low-stock monitoring	| Medium |
| FR-09	| Sales recording	| High |
| FR-10	| Sales validation	| High |
| FR-11	| Sales analysis	| High |
| FR-12	| Sales trend reporting	| High |
| FR-13	| Product performance reporting	| High |
| FR-14	| Regional performance reporting	| High |
| FR-15	| Salesperson performance reporting	| Medium |
| FR-16	| Management dashboard	| High |
| FR-17	| Search and filtering	| High |
| FR-18	| Data validation	| High |
| FR-19	| Transaction identification |	High |
| FR-20	| Reporting	| High |

## 4. Requirement Traceability

The functional requirements translate the business requirements into specific system capabilities.

| Business Requirement	| Related Functional Requirements |
|-----------------------|---------------------------------|
| BR-01 Centralized Information	| FR-03–FR-09 |
| BR-02 Product Management	| FR-03 |
| BR-03 Customer Management	| FR-04 |
| BR-04 Order Management	| FR-05, FR-06 |
| BR-05 Inventory Visibility	| FR-07 |
| BR-06 Inventory Alerting	| FR-08 |
| BR-07 Sales Performance Monitoring	| FR-09, FR-11 |
| BR-08 Regional Analysis	| FR-14 |
| BR-09 Product Analysis	| FR-13 |
| BR-10 Sales Trend Monitoring	| FR-12 |
| BR-11 Salesperson Performance	| FR-15 |
| BR-12 Centralized Reporting	| FR-20 |
| BR-13 Data Quality	| FR-10, FR-18 |
| BR-14 Transaction Traceability	| FR-19 |
| BR-15 Role-Based Access	| FR-01, FR-02 |
| BR-16 Business Dashboard	| FR-16 |
| BR-17 Scalability	| Supported by the overall system structure |

## 5. Notes

These functional requirements represent the **proposed system design** for the simulated cosmetics retailer. They should be validated and refined through stakeholder interviews or workshops before actual implementation.