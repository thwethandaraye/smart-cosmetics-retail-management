# Stakeholder Analysis

> **Note:** The stakeholders identified in this document are based on
> the simulated business environment of Terra Tint Cosmetics. They are
> defined for the purpose of this Business Analysis case study and are
> not based on interviews with an actual organization.

## 1. Stakeholder Overview

Stakeholders are individuals or groups who interact with, influence,
or are affected by the proposed Smart Cosmetics Retail Management
System.

The stakeholder analysis identifies the primary users of the system,
their responsibilities, business interests, level of influence, and
information requirements. Understanding these factors helps ensure
that the proposed solution addresses the needs of different
stakeholder groups.

The main stakeholders identified for this project are:

- Business Manager
- Sales Staff
- Inventory Staff
- Warehouse Staff
- Finance Staff
- Customers
- IT / Development Team
- System Administrator

## 2. Stakeholder Identification

### 2.1 Business Manager

The Business Manager is responsible for monitoring overall business
performance and making operational and strategic decisions.

**Primary interests:**

- Overall sales performance
- Product performance
- Geographic market performance
- Sales trends
- Business KPIs
- Operational efficiency

**System needs:**

- Sales dashboards
- Management reports
- Product performance analysis
- Geographic performance analysis
- Sales trend analysis
- Access to summarized business information

### 2.2 Sales Staff

Sales staff interact directly with customers and are responsible for
supporting sales activities and recording customer orders.

**Primary interests:**

- Product information
- Customer information
- Order processing
- Product availability
- Sales performance

**System needs:**

- Product search and information
- Customer records
- Order creation and management
- Product availability information
- Access to relevant sales information

### 2.3 Inventory Staff

Inventory staff are responsible for monitoring product availability
and maintaining accurate inventory information.

**Primary interests:**

- Current stock levels
- Product availability
- Stock movements
- Low-stock products
- Inventory accuracy

**System needs:**

- Inventory records
- Stock-level monitoring
- Inventory updates
- Low-stock alerts
- Inventory reports

> **Note:** Inventory requirements are proposed capabilities of the
> future system. The available sales dataset does not contain actual
> stock-on-hand, reorder-point, or stockout information.

### 2.4 Warehouse Staff

Warehouse staff are responsible for preparing products for order
fulfillment and coordinating the physical handling of orders.

**Primary interests:**

- Confirmed orders
- Product quantities
- Fulfillment status
- Order information

**System needs:**

- Access to confirmed orders
- Order details
- Product quantities
- Fulfillment status
- Clear order-processing information

### 2.5 Finance Staff

Finance staff are responsible for monitoring financial transaction
information and supporting financial record management.

**Primary interests:**

- Sales amounts
- Payment information
- Transaction records
- Financial reporting

**System needs:**

- Sales transaction information
- Payment status
- Financial reports
- Transaction history

### 2.6 Customers

Customers purchase cosmetics products and are directly affected by the
quality and efficiency of the purchasing process.

**Primary interests:**

- Accurate product information
- Product availability
- Order confirmation
- Payment confirmation
- Order status
- Delivery information

**System needs:**

- Product information
- Product availability
- Order confirmation
- Order status
- Clear communication throughout the purchasing process

### 2.7 IT / Development Team

The IT or development team is responsible for designing,
implementing, testing, and maintaining the proposed system.

**Primary interests:**

- Clear business requirements
- Functional requirements
- System workflows
- Data structures
- Technical constraints
- Acceptance criteria

**System needs:**

- Business requirements
- Functional and non-functional requirements
- User stories
- Process models
- Data-flow diagrams
- Database specifications
- Acceptance criteria
- Testing requirements

### 2.8 System Administrator

The System Administrator manages user accounts, permissions, and
system-level access.

**Primary interests:**

- System security
- User access
- Roles and permissions
- Data protection
- System availability

**System needs:**

- User account management
- Role-based access control
- Permission management
- User activity monitoring
- System configuration

## 3. Stakeholder Summary

| Stakeholder | Primary Responsibility | Main Interest | Key System Needs | Influence |
|---|---|---|---|---|
| Business Manager | Business decisions | Business performance | Dashboards, reports, KPIs | High |
| Sales Staff | Sales activities | Orders and customers | Product, customer, order information | Medium |
| Inventory Staff | Inventory operations | Stock availability | Inventory records and alerts | Medium |
| Warehouse Staff | Order fulfillment | Order preparation | Order and fulfillment information | Medium |
| Finance Staff | Financial operations | Transactions and payments | Sales and payment information | Medium |
| Customers | Product purchases | Product and order experience | Product availability and order status | Medium |
| IT / Development Team | System development | Requirements and system design | Specifications and models | High |
| System Administrator | System administration | Security and access | Users, roles, permissions | High |

## 4. Stakeholder Influence and Interest

Stakeholders can be categorized according to their level of influence
over the project and their level of interest in the proposed system.

### High Influence / High Interest

**Business Manager**

The Business Manager has significant influence over business
decisions and a strong interest in the information provided by the
system.

**IT / Development Team**

The development team has significant influence over the technical
implementation of the system and requires detailed business and
technical requirements.

**System Administrator**

The System Administrator has high influence over system access,
security, and administration.

### High Influence / Lower Interest

**Finance Staff**

Finance staff may have significant influence over financial
information requirements but may not interact with every part of the
system.

### Lower Influence / High Interest

**Sales Staff**

Sales staff are frequent operational users and therefore have a
strong interest in system usability and efficient order processing.

**Inventory Staff**

Inventory staff have a strong interest in accurate inventory
information and monitoring capabilities.

**Warehouse Staff**

Warehouse staff depend on accurate order information to support
fulfillment activities.

### Lower Influence / Variable Interest

**Customers**

Customers are important users and beneficiaries of the purchasing
process, although they may have less direct influence over internal
system design decisions.

## 5. Power-Interest Matrix

The stakeholder classification can be represented using a
power-interest matrix:

```text
                         HIGH POWER
                              │
            Manage Closely   │   Keep Satisfied
                              │
       Business Manager       │       Finance Staff
       IT / Development       │
       System Administrator   │
                              │
──────────────────────────────┼────────────────────────
                              │
            Keep Informed     │   Monitor
                              │
       Sales Staff            │
       Inventory Staff        │
       Warehouse Staff        │
                              │       Customers
                              │
                         LOW POWER
```

The matrix helps determine the appropriate level of stakeholder
engagement throughout the project.

## 6. Stakeholder Communication Needs

Different stakeholders require different types of information.

| Stakeholder | Information Required | Preferred Communication |
|---|---|---|
| Business Manager | KPIs, reports, business findings | Management reports, meetings |
| Sales Staff | Orders, customers, products | System interface, training |
| Inventory Staff | Stock levels, alerts | System interface, operational reports |
| Warehouse Staff | Orders, quantities, fulfillment status | System interface, order reports |
| Finance Staff | Transactions, payments, sales | Financial reports, system records |
| Customers | Products, orders, delivery | Customer interface, notifications |
| IT / Development Team | Requirements, workflows, specifications | Requirements documents, workshops |
| System Administrator | Users, permissions, security | Administration interface, technical documentation |

## 7. Stakeholder Engagement Strategy

The proposed stakeholder engagement approach is based on the level
of influence and interest of each stakeholder.

### Business Manager

The Business Manager should be involved in defining business
objectives, prioritizing requirements, reviewing proposed processes,
and validating whether the system supports business goals.

### Sales Staff

Sales staff should participate in requirements elicitation related
to customer management, product information, order processing, and
sales activities.

### Inventory Staff

Inventory staff should contribute to requirements related to stock
management, inventory updates, availability monitoring, and
replenishment alerts.

### Warehouse Staff

Warehouse staff should provide input on order fulfillment,
warehouse workflows, and information required to prepare and dispatch
orders.

### Finance Staff

Finance staff should provide requirements related to transaction
records, payment information, and financial reporting.

### Customers

Customer needs should be considered when defining product
information, availability, order confirmation, and order-status
functionality.

### IT / Development Team

The development team should work closely with business stakeholders
to clarify requirements, identify technical constraints, review
system models, and validate proposed functionality.

### System Administrator

The System Administrator should be involved in defining user roles,
permissions, authentication, and system-security requirements.

## 8. Key Stakeholder Questions

During a real requirements elicitation process, the following
questions could be used to validate stakeholder needs:

### Business Manager

- Which business KPIs are most important?
- Which reports are currently required for decision-making?
- How frequently should management reports be generated?
- Which business processes should be prioritized for improvement?

### Sales Staff

- How are customer orders currently recorded?
- What information is required when creating an order?
- How do staff check product availability?
- Which sales activities require the most manual effort?

### Inventory Staff

- How is inventory currently recorded?
- How are low-stock products identified?
- What inventory threshold should trigger an alert?
- How frequently should inventory information be updated?

### Warehouse Staff

- How are confirmed orders received?
- What information is required to prepare an order?
- How is fulfillment status currently tracked?

### Finance Staff

- What payment information must be recorded?
- Which financial reports are required?
- How should transaction records be reconciled?

### IT / Development Team

- What technical constraints must the system satisfy?
- What existing systems need to be integrated?
- What database structure is appropriate?
- What security requirements must be implemented?

## 9. Stakeholder Analysis Summary

The stakeholder analysis demonstrates that the proposed system must
support both operational and management-level requirements.

Operational users require efficient access to products, customers,
orders, inventory, and fulfillment information, while management
requires reliable reports and analytics for decision-making.

The IT and system administration stakeholders require clear
requirements, system models, data structures, security rules, and
acceptance criteria to support successful system development.

These stakeholder needs will be used as inputs for the subsequent
current-state analysis, pain-point identification, and requirements
definition activities.