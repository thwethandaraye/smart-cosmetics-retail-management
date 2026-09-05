# User Stories
## 1. Purpose

This document defines user stories for the proposed **Smart Cosmetics Retail Management System**. The stories describe system needs from the perspective of different users and connect the business and functional requirements to practical user activities.

The user stories follow the format:
**`As a [user], I want [goal], so that [benefit].`**

## 2. User Stories

### US-01 — User Login
As a system user, I want to log in securely, so that I can access the functions authorized for my role.
Related: FR-01, FR-02

### US-02 — Manage Products
As a product manager, I want to create, update, and view product information, so that product records remain accurate and up to date.
Related: FR-03

### US-03 — Manage Customers
As a sales staff member, I want to create and update customer records, so that customer information can be maintained centrally.
Related: FR-04

### US-04 — Create Customer Orders
As a sales staff member, I want to create customer orders with products and quantities, so that sales can be recorded accurately.
Related: FR-05, FR-09

### US-05 — Track Orders
As a sales or customer service staff member, I want to view and update order status, so that I can monitor order progress.
Related: FR-06

### US-06 — Monitor Inventory
As an inventory staff member, I want to view and update product stock quantities, so that current inventory information remains accurate.
Related: FR-07

### US-07 — Receive Low-Stock Alerts
As an inventory staff member, I want to identify products below their reorder threshold, so that I can take appropriate replenishment action.
Related: FR-08

### US-08 — Analyze Sales
As a manager, I want to analyze sales by product, country, salesperson, and time period, so that I can evaluate business performance.
Related: FR-11

### US-09 — Monitor Sales Trends
As a manager, I want to view sales trends over time, so that I can identify changes in sales performance.
Related: FR-12

### US-10 — Compare Product Performance
As a manager, I want to compare product sales performance, so that I can identify high- and low-performing products.
Related: FR-13

### US-11 — Compare Regional Performance
As a manager, I want to compare sales across countries or regions, so that I can identify differences in market performance.
Related: FR-14

### US-12 — Monitor Salesperson Performance
As a sales manager, I want to review individual salesperson performance, so that I can monitor sales results and identify areas for improvement.
Related: FR-15

### US-13 — View Management Dashboard
As a manager, I want to view key business indicators in one dashboard, so that I can access important information quickly.
Related: FR-16

### US-14 — Search and Filter Records
As a system user, I want to search and filter business records, so that I can quickly find relevant information.
Related: FR-17

### US-15 — Validate Business Data
As a system administrator, I want the system to validate business data before saving it, so that inaccurate or incomplete records can be prevented.
Related: FR-18

### US-16 — Identify Transactions
As a manager, I want every transaction to have a unique identifier, so that individual transactions can be traced and audited.
Related: FR-19

### US-17 — Generate Reports
As a manager, I want to generate sales and operational reports, so that I can support data-driven business decisions.
Related: FR-20

## 3. User Story Summary

| ID	| User Role	| User Story Goal	| Priority |
|-------|-----------|-------------------|----------|
| US-01	| System User	| Secure login	| High |
| US-02	| Product Manager	| Manage products | High |
| US-03	| Sales Staff	| Manage customers	| High |
| US-04	| Sales Staff	| Create orders	| High |
| US-05	| Sales/Customer Service |	Track orders	| High |
| US-06	| Inventory Staff	| Monitor inventory	 | High |
| US-07	| Inventory Staff	| Identify low stock	 | Medium |
| US-08	| Manager	| Analyze sales	| High |
| US-09	| Manager	| Monitor sales trends	| High |
| US-10	| Manager	| Compare products	| High |
| US-11	| Manager	| Compare regions	| High |
| US-12	| Sales Manager	| Monitor salesperson performance	| Medium |
| US-13	| Manager	| View dashboard	| High |
| US-14	| System User	| Search and filter records	| High |
| US-15	| Administrator	| Validate data	| High |
| US-16	| Manager	| Trace transactions	| High |
| US-17	| Manager	| Generate reports	| High |

## 4. Traceability

The user stories provide the next level of detail after the functional requirements:
**Business Requirement → Functional Requirement → User Story → Acceptance Criteria → Test Case**

For example:
```text
BR-10: Sales trend monitoring
↓
FR-12: System shall generate sales trend reports
↓
US-09: As a manager, I want to view sales trends over time...
↓
Acceptance Criteria: Manager can select a time period and view corresponding sales results.
↓
Test Case: Verify that the system correctly displays sales trends for the selected period.
```