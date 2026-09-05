# Non-Functional Requirements
## 1. Purpose

This document defines the non-functional requirements (NFRs) for the proposed **Smart Cosmetics Retail Management System**. These requirements describe the quality attributes and operational standards the system should satisfy in addition to its functional capabilities.

## 2. Non-Functional Requirements

### NFR-01 — Performance
The system should respond to normal user actions and database queries within 3 seconds under expected operating conditions.

### NFR-02 — Availability
The system should be available during normal business operating hours, with planned maintenance communicated to users in advance.

### NFR-03 — Security
The system shall protect business and customer information through authentication, authorization, secure password storage, and role-based access control.

### NFR-04 — Data Integrity
The system shall maintain accurate and consistent data by enforcing validation rules, unique identifiers, and referential integrity.

### NFR-05 — Usability
The system interface should be simple and intuitive so that users can perform common tasks with minimal training.

### NFR-06 — Reliability
The system should process transactions consistently and prevent data loss or corruption during normal operation.

### NFR-07 — Scalability
The system should support increasing numbers of products, customers, users, orders, and transactions without requiring major architectural changes.

### NFR-08 — Maintainability
The system should use modular components, clear documentation, and structured code to make future maintenance and enhancement easier.

### NFR-09 — Compatibility
The system should operate correctly on commonly used modern web browsers and standard desktop devices.

### NFR-10 — Backup and Recovery
The system should perform regular backups of critical business data and provide a mechanism for recovering data after system failure.

### NFR-11 — Auditability
The system should record important user and data activities, such as creating, updating, or deleting business records, where appropriate.

### NFR-12 — Data Privacy
The system shall restrict access to customer and business information to authorized users and collect only information required for legitimate business purposes.

### NFR-13 — Extensibility
The system should allow future features, modules, and integrations to be added without significantly affecting existing functionality.

## 3. NFR Summary

| ID	| Quality Attribute	| Requirement |
|-------|-------------------|-------------|
| NFR-01	| Performance	| Normal operations should respond within 3 seconds |
| NFR-02	| Availability	| System available during business hours |
| NFR-03	| Security	| Protect data through authentication and access control |
| NFR-04	| Data Integrity	| Maintain accurate and consistent data |
| NFR-05	| Usability	| Provide an intuitive user interface |
| NFR-06	| Reliability	| Prevent transaction failure and data corruption |
| NFR-07	| Scalability	| Support future growth |
| NFR-08	| Maintainability	| Use modular design and documentation |
| NFR-09	| Compatibility	| Support modern browsers and standard devices |
| NFR-10	| Backup & Recovery	| Protect and recover critical data |
| NFR-11	| Auditability	| Record important system activities |
| NFR-12	| Data Privacy	| Restrict access to sensitive information |
| NFR-13	| Extensibility	| Support future features and integrations |

## 4. Relationship to Functional Requirements

Functional requirements define **what the system does**, while non-functional requirements define **how well the system should perform those functions**.

For example:
`FR-07: The system shall maintain current inventory quantities.`

The related NFRs include:
- NFR-01: Inventory information should be retrieved efficiently.
- NFR-04: Inventory quantities must remain accurate and consistent.
- NFR-03: Only authorized users should modify inventory.
- NFR-06: Inventory updates should be processed reliably.