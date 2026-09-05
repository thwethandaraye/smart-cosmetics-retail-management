# Smart Cosmetics Retail Management System
### Business Analysis, Data Insights & Digital Process Improvement Case Study

> **Portfolio Project | Business Analysis • Data Analysis • Requirements Engineering**

---

## 📌 Project Overview

The **Smart Cosmetics Retail Management System** is a simulated business analysis and data analysis project for a fictional cosmetics retailer.

The project explores how a centralized digital management system could improve the way a cosmetics retailer manages **sales, products, customers, inventory, and business reporting**.

The project combines business analysis and data analysis techniques to move from a business problem and raw transaction data toward structured requirements and a proposed technology solution.

> **Note:** This is a simulated portfolio project. The company, operational processes, and proposed system are not based on an implemented real-world organization. Where information is not available in the dataset, assumptions are clearly identified.

---

## 🎯 Project Objectives

The main objectives of this project are to:

- Analyze cosmetics sales data to identify business insights.
- Identify business problems and information gaps.
- Analyze stakeholders and their potential requirements.
- Model the current business situation.
- Identify operational pain points.
- Perform gap analysis between the current and desired state.
- Translate business needs into structured requirements.
- Develop functional and non-functional requirements.
- Create user stories and acceptance criteria.
- Prioritize requirements using the MoSCoW method.
- Propose a centralized digital retail management solution.

---

# ❓ Business Problem

A growing cosmetics retailer needs reliable access to information about its sales performance, products, customers, inventory, and transactions.

When information is maintained through disconnected or manual processes, management may experience difficulties such as:

- Limited visibility into sales performance
- Difficulty comparing regional performance
- Variation in product performance
- Manual reporting activities
- Limited inventory visibility
- Difficulty tracking transactions
- Delayed access to business insights
- Risk of data-entry inconsistencies

The proposed solution is a centralized **Smart Cosmetics Retail Management System** that can integrate operational information and provide structured reporting and analytics.

---

# ❓ Central Business Question

**How can a cosmetics retailer use a centralized technology solution to improve sales operations, inventory management, customer management, and data-driven decision-making?**

---

# 📊 Data Analysis

The project uses a sample cosmetics sales dataset containing **374 sales transactions**.

The dataset includes:

| Field | Description |
|---|---|
| Sales Person | Employee associated with the transaction |
| Country | Country associated with the sale |
| Product | Product sold |
| Date | Transaction date |
| Amount ($) | Total transaction amount |
| Boxes Shipped | Quantity shipped |
| Unit Price | Price per unit |

The available data covers transactions from **January 1 to August 30, 2022**.

### Data Quality

Initial data-quality analysis identified:

- 374 records
- 7 columns
- No missing values in the available dataset
- No exact duplicate records
- Transaction amounts are consistent with quantity and unit price

The dataset does **not** contain:

- Customer information
- Stock-on-hand quantities
- Supplier information
- Product costs
- Profit margins
- Payment information
- Delivery status

Therefore, these areas are treated as **proposed system capabilities or information gaps**, rather than claims about the actual dataset.

---

# 📈 Key Business Insights

The exploratory analysis identified several areas that could support business improvement.

### Regional Sales

Sales performance differs considerably between countries.

This indicates the potential value of centralized regional sales analysis for comparing markets and supporting management decisions.

### Salesperson Performance

Sales performance varies between salespeople in terms of transaction volume and total sales.

A centralized performance dashboard could help management monitor salesperson performance more consistently.

### Sales Trends

Monthly sales fluctuate significantly across the observed period.

Monitoring sales trends could help management identify periods of stronger or weaker performance and investigate possible causes.

### Product Performance

Products generate different levels of sales revenue.

Product-level analysis could therefore support decisions around product strategy, sales focus, and future inventory planning.

---

# 🏢 Proposed Solution

The proposed **Smart Cosmetics Retail Management System** would provide centralized management of key retail information.

### Proposed Modules

**Product Management**
- Product creation and updating
- Product search
- Product status management

**Customer Management**
- Customer records
- Customer search
- Customer information management

**Order Management**
- Order creation
- Order tracking
- Order status management

**Inventory Management**
- Inventory visibility
- Inventory updates
- Low-stock monitoring

**Sales Management**
- Sales recording
- Sales validation
- Transaction traceability
- Salesperson performance monitoring

**Reporting & Analytics**
- Sales dashboards
- Regional analysis
- Product analysis
- Salesperson analysis
- Sales trend reporting

**User Management**
- Authentication
- Role-based access
- Permissions
- Auditability

> Inventory and customer functionality are proposed capabilities because the available sales dataset does not contain complete inventory or customer information.

---

# 📋 Business Analysis

The business analysis stage identifies the business context, stakeholders, current-state situation, pain points, and gaps.

### Current Business Analysis

The project covers:

- Business case
- Company background
- Dataset description
- Stakeholder analysis
- Current-state analysis
- Pain-point analysis
- Gap analysis

These activities establish the business context before defining system requirements.

---

# 📝 Requirements Engineering

The project translates identified business needs into structured requirements.

### Business Requirements

The project defines requirements covering areas such as:

- Centralized information management
- Product management
- Customer management
- Order management
- Inventory visibility
- Sales monitoring
- Regional analysis
- Product performance
- Sales trends
- Salesperson performance
- Reporting
- Data quality
- Transaction traceability
- Access control
- Business dashboards

### Functional Requirements

Functional requirements describe what the proposed system should do, including:

- User authentication
- Product management
- Customer management
- Order creation
- Order tracking
- Inventory management
- Sales recording
- Sales validation
- Sales analysis
- Reporting
- Dashboard functionality
- Search and filtering
- Transaction identification

### Non-Functional Requirements

The project also considers:

- Performance
- Security
- Availability
- Data integrity
- Usability
- Reliability
- Scalability
- Maintainability
- Compatibility
- Backup and recovery
- Auditability
- Privacy
- Extensibility

---

# 👤 User Stories

User stories are used to express requirements from the perspective of system users.

Example:

> **As a sales staff member, I want to create a customer order so that the transaction can be recorded and processed accurately.**

The project includes user stories for:

- Authentication
- Product management
- Customer management
- Order management
- Inventory monitoring
- Sales analysis
- Reporting
- Dashboards
- Data validation
- Transaction management

---

# ✅ Acceptance Criteria

Acceptance criteria are defined using a **Given / When / Then** structure to make requirements testable.

Example:

```text
Given a valid customer, product, and quantity are provided
When the sales staff creates an order
Then the system should create the order successfully
And generate a unique transaction ID
And calculate the transaction amount correctly.
```

# ⭐ Requirements Prioritization

Requirements are prioritized using the **MoSCoW framework**.

## Must Have

Core functionality required for the proposed solution, including:
- Centralized information
- Product management
- Customer management
- Order management
- Inventory visibility
- Sales monitoring
- Reporting
- Data validation
- Transaction traceability
- Role-based access

## Should Have

Important functionality that provides additional business value:
- Low-stock alerts
- Regional analytics
- Product performance analysis
- Salesperson performance analysis
- Business dashboard
- Scalability

## Could Have

Potential future enhancements:
- Sales forecasting
- Customer segmentation
- Product recommendations
- Advanced analytics
- Automated business recommendations

## Won't Have in Current Scope

The following are outside the current scope:
- Real payment processing
- Live delivery integration
- AI demand forecasting
- Live external e-commerce integration

# 🛠️ Tools & Technologies

| Area	 | Tools / Techniques |
|--------|--------------------|
| Business Analysis	| Business Case, Stakeholder Analysis, Gap Analysis |
| Requirements	| BR, FR, NFR, User Stories, Acceptance Criteria |
| Prioritization	| MoSCoW |
| Data Analysis	| Python, Pandas, NumPy |
| Data Visualization	| Matplotlib, Excel |
| Data Exploration	| Jupyter Notebook |
| Documentation	| Markdown |
| Version Control	| Git / GitHub |

# 📁 Current Project Structure
```text
smart-cosmetics-retail-management/
│
├── README.md
│
├── 01-Business-Analysis/
│   ├── Business-Case.md
│   ├── Company-Background.md
│   ├── Dataset-Description.md
│   ├── Stakeholder-Analysis.md
│   ├── Current-State-Analysis.md
│   ├── Pain-Points.md
│   └── Gap-Analysis.md
│
├── 02-Data-Analysis/
│   ├── Cosmetics_Retail_Analysis.ipynb
│   ├── Data-Dictionary.md
│   └── Data-Quality-Report.md
│
└── 03-Requirements/
    ├── Business-Requirements.md
    ├── Functional-Requirements.md
    ├── Non-Functional-Requirements.md
    ├── User-Stories.md
    ├── Acceptance-Criteria.md
    └── Requirements-Prioritization.md
```
# 🚧 Planned Project Development

The project will be expanded with additional business and system analysis deliverables.

## 04 — Process Modeling

Planned deliverables:
- AS-IS Process
- TO-BE Process
- Process Flow
- Process Improvement Analysis

## 05 — System Analysis

Planned deliverables:
- System Overview
- Stakeholder Context Diagram
- System Context Diagram
- Data Flow Diagram — Level 0
- Data Flow Diagram — Level 1
- Use Case Diagram
- Use Case Specifications

# 06 — Database Design

Planned deliverables:
- Entity Relationship Diagram
- Database Design
- Database Data Dictionary
- SQL Schema

## 07 — AI & Prompt Engineering

Planned deliverables:
- Prompt Library
- Requirements Analysis
- Process Analysis
- AI-Assisted Business Analysis Workflow

## 08 — Testing

Planned deliverables:
- Test Strategy
- Test Cases
- Requirements Traceability Matrix

## 09 — Portfolio Case Study
Final deliverable:
- Complete Business Analysis Case Study

# 📌 Project Methodology

The project follows an end-to-end analytical workflow:

Business Problem
       ↓
Business Analysis
       ↓
Data Analysis
       ↓
Stakeholder Analysis
       ↓
Pain-Point Identification
       ↓
Gap Analysis
       ↓
Requirements Engineering
       ↓
Process Modeling
       ↓
System Analysis
       ↓
Database Design
       ↓
Testing & Validation
       ↓
Proposed Digital Solution

# ⚠️ Assumptions & Limitations

This is a simulated portfolio project and not an implementation for a real organization.

The available dataset supports analysis of sales transactions, but it does not provide complete information about customers, inventory levels, suppliers, costs, payments, or delivery operations.

Consequently, operational workflows and requirements involving these areas are treated as **proposed or assumed scenarios**.

In a real business environment, these assumptions would need to be validated through:
- Stakeholder interviews
- Process observation
- Existing-system analysis
- Documentation review
- Data profiling
- User feedback

# 🚀 Future Improvements

Possible future extensions include:
- Develop a working web application
- Implement the proposed relational database
- Develop REST APIs
- Build an interactive Power BI dashboard
- Implement authentication and authorization
- Add automated inventory alerts
- Add customer segmentation
- Add sales forecasting
- Integrate payment and delivery systems
- Connect with an e-commerce platform
- Deploy the solution to the cloud

# 👩‍💻 About Me

Thwe Thandar Aye

Computer Science undergraduate interested in:
- Business Analysis
- Data Analysis
- Backend Development
- Data Engineering
- Digital Process Improvement

This project is part of my professional portfolio and demonstrates my ability to analyze business problems, work with data, define requirements, and translate business needs into structured technology solutions.

# 📫 Contact
**LinkedIn:** Thwe Thandar Aye 
**GitHub:** thwethandaraye 
**Email:** thwethandaraye19@gmail.com 
