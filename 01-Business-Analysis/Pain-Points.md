# Pain Points Analysis

> **Note:** Terra Tint Cosmetics is a fictional/simulated business created for this portfolio case study. The pain points below are based on the dataset analysis and the assumed AS-IS business process documented in `Current-State-Analysis.md`. They are not based on interviews with an actual company.

## 1. Overview

Pain-point analysis identifies problems, inefficiencies, risks, and limitations within the current business environment. It connects the current-state analysis with the business requirements for the proposed Smart Cosmetics Retail Management System.

The analysis combines two sources of evidence:

1. **Data-supported observations** from the cosmetics sales dataset.
2. **Process-related assumptions** based on the simulated current-state business process.

The purpose is not only to identify what is happening, but also to understand the potential business impact and determine where a technology-based solution could provide improvement.

---

## 2. Identified Pain Points

### Pain Point 1: Uneven Sales Performance Across Countries

The dataset shows noticeable differences in sales performance across the six countries.

The United States generated the highest sales at approximately **$628,488**, while India generated approximately **$346,435**. This indicates that sales performance is not evenly distributed across the geographic markets.

#### Business Impact

Without effective regional analysis, management may have difficulty identifying:

- High-performing and low-performing markets
- Changes in regional sales performance
- Markets that may require additional attention
- Opportunities for improving sales strategies

#### Evidence

This pain point is directly supported by the sales dataset through country-level sales analysis.

#### Potential Improvement

The proposed system should provide regional sales reporting and allow managers to filter and compare performance by country and time period.

---

### Pain Point 2: Variation in Salesperson Performance

Sales performance also varies between individual salespeople. For example, the highest-performing salesperson generated approximately **$387,406**, while the lowest among the analyzed salespeople generated approximately **$223,433**.

This difference may indicate variation in sales activity, customer interactions, product knowledge, territory performance, or other factors.

#### Business Impact

Limited visibility into salesperson performance can make it difficult for management to:

- Monitor individual performance
- Identify performance gaps
- Compare sales results
- Recognize high-performing staff
- Provide targeted support or training

#### Evidence

This pain point is supported by the salesperson-level analysis of the dataset.

#### Potential Improvement

The proposed system should provide salesperson performance reports containing metrics such as total sales, transaction count, and average transaction value.

---

### Pain Point 3: Significant Monthly Sales Fluctuations

The dataset shows considerable variation in monthly sales.

Sales increased from approximately **$214,025 in February to $484,102 in March**, representing a substantial increase. Sales then declined during the following months, reaching approximately **$275,299 in August**.

#### Business Impact

Large changes in monthly sales can make it more difficult to:

- Monitor sales performance
- Identify changes in demand
- Plan business activities
- Investigate unusual changes in revenue
- Support management decision-making

#### Evidence

This pain point is directly supported by the monthly sales analysis.

#### Potential Improvement

The proposed system should include time-based sales dashboards and trend reports that allow managers to identify changes in sales performance quickly.

---

### Pain Point 4: Large Differences in Product Performance

Product-level analysis shows that some products generate significantly more revenue than others.

For example, **Tea Tree Moisturizer** generated approximately **$260,905**, while **Charcoal Face Wash** generated approximately **$102,733** during the analyzed period.

This represents a substantial difference in product performance.

#### Business Impact

Without centralized product performance analysis, management may have difficulty determining:

- Which products generate the most revenue
- Which products have relatively low sales
- Changes in product demand
- Which products require further investigation
- Which products should receive greater management attention

#### Evidence

This pain point is directly supported by product-level sales analysis.

#### Potential Improvement

The proposed system should provide product performance reports and filtering capabilities to support product-level decision-making.

---

### Pain Point 5: Fragmented Business Information

The simulated current-state process involves multiple operational activities, including order recording, product availability checking, payment confirmation, warehouse processing, delivery, and sales reporting.

If these activities are managed using separate records or spreadsheets, information may become fragmented across different operational areas.

#### Business Impact

Fragmented information can lead to:

- Repeated data entry
- Difficulty locating information
- Inconsistent information between records
- Delays when retrieving business information
- Greater dependency on manual coordination

#### Evidence

This is primarily a **process-based assumption** within the simulated business environment. It is not directly proven by the sales dataset.

#### Potential Improvement

A centralized system should provide a common source of business information for products, customers, orders, inventory, and sales.

---

### Pain Point 6: Limited Real-Time Operational Visibility

The analyzed dataset provides historical transaction information, but it does not provide real-time information about current orders, inventory status, customer activity, payment status, or delivery progress.

This creates a limitation in the current information environment.

#### Business Impact

Limited operational visibility can make it more difficult for staff and managers to:

- Monitor current business activities
- Track order status
- Identify operational issues quickly
- Monitor product availability
- Respond to changes in business conditions

#### Evidence

The dataset contains historical sales transactions but does not contain real-time operational status information.

#### Potential Improvement

The proposed system should centralize operational information and provide appropriate status tracking for orders, inventory, payments, and deliveries.

---

### Pain Point 7: Lack of Inventory Visibility

Inventory management is an important requirement for a cosmetics retailer because product availability affects order fulfillment and customer service.

However, the current dataset contains **Boxes Shipped**, rather than stock-on-hand quantities, reorder points, stockout records, or inventory movement history.

Therefore, the dataset cannot establish that GlowBeauty Cosmetics currently experiences inventory shortages.

The pain point is instead identified as a **potential information gap** in the simulated current-state environment.

#### Business Impact

If inventory information is not centralized, staff may have difficulty:

- Checking current stock levels
- Identifying products approaching a defined threshold
- Coordinating inventory with orders
- Monitoring inventory changes
- Supporting replenishment decisions

#### Evidence

This is a proposed business-analysis concern rather than a confirmed inventory problem. The available dataset does not contain sufficient information to measure stockouts or inventory shortages.

#### Potential Improvement

The proposed system should include inventory records, stock-level monitoring, inventory movement tracking, and configurable low-stock thresholds.

---

## 3. Pain Point Summary

| ID | Pain Point | Evidence Type | Potential Business Impact | Proposed Improvement |
|---|---|---|---|---|
| PP-01 | Uneven regional sales performance | Data-supported | Difficult to compare and monitor markets | Regional sales analytics |
| PP-02 | Variation in salesperson performance | Data-supported | Limited performance monitoring | Salesperson performance reporting |
| PP-03 | Significant monthly sales fluctuations | Data-supported | Difficult to monitor trends and changes | Sales trend dashboard |
| PP-04 | Large differences in product performance | Data-supported | Limited product-level decision support | Product performance analytics |
| PP-05 | Fragmented business information | Process assumption | Repeated work and information delays | Centralized business system |
| PP-06 | Limited real-time operational visibility | Data/process limitation | Slower operational decision-making | Centralized status tracking |
| PP-07 | Lack of inventory visibility | Data limitation / proposed concern | Potential difficulty managing product availability | Inventory management module |

---

## 4. Root-Cause Analysis

The identified pain points can be grouped into several underlying causes.

### 4.1 Data Visibility

Sales information exists in the dataset, but managers need structured ways to compare performance across products, countries, salespeople, and time periods.

**Underlying issue:** Business data is not automatically transformed into actionable management information.

---

### 4.2 Information Centralization

The simulated business process involves several operational activities that may require coordination between different roles.

**Underlying issue:** Information may be distributed across different operational records rather than maintained through a centralized system.

---

### 4.3 Manual Processes

Activities such as order recording, information checking, reporting, and coordination may require manual effort in the simulated current environment.

**Underlying issue:** Repetitive manual activities can increase processing time and create opportunities for human error.

---

### 4.4 Limited Operational Monitoring

Historical transaction data can support analysis, but it does not provide complete visibility into current orders, inventory, payments, or deliveries.

**Underlying issue:** The available information environment does not provide a complete operational view of the business.

---

### 4.5 Limited Decision-Support Capability

Managers need to understand not only individual transactions but also broader patterns and trends.

**Underlying issue:** Without integrated reporting and analytics, converting operational data into actionable insights can require additional manual analysis.

---

## 5. Business Impact Analysis

The pain points can affect different areas of the business.

| Business Area | Potential Impact |
|---|---|
| Sales Management | Limited visibility into salesperson and regional performance |
| Product Management | Difficulty comparing product performance |
| Inventory Management | Limited visibility into stock status |
| Order Management | Potential delays in accessing order information |
| Customer Service | Potential difficulty confirming product and order information |
| Management Reporting | Increased dependency on manual analysis |
| Decision-Making | Slower access to actionable information |
| Data Management | Potential duplication or inconsistency when information is maintained separately |

---

## 6. Prioritization of Pain Points

The following prioritization is based on the potential business impact and relevance to the proposed system.

| Priority | Pain Point | Reason |
|---|---|---|
| High | PP-05 Fragmented Business Information | Can affect multiple business processes and user groups |
| High | PP-06 Limited Operational Visibility | Can reduce the speed of operational decision-making |
| High | PP-07 Lack of Inventory Visibility | Important for product availability and order fulfillment |
| Medium | PP-03 Monthly Sales Fluctuations | Requires monitoring to support management decisions |
| Medium | PP-04 Product Performance Differences | Useful for product and sales strategy |
| Medium | PP-01 Regional Sales Differences | Useful for geographic performance monitoring |
| Medium | PP-02 Salesperson Performance Variation | Useful for performance management |

> **Note:** The prioritization represents a simulated business-analysis assessment. It should be validated with actual stakeholders before implementation.

---

## 7. Pain Point to Business Need Mapping

The identified pain points lead to several business needs.

| Pain Point | Business Need |
|---|---|
| Uneven regional sales performance | Regional sales visibility |
| Variation in salesperson performance | Sales performance monitoring |
| Monthly sales fluctuations | Sales trend analysis |
| Product performance differences | Product performance monitoring |
| Fragmented information | Centralized business information |
| Limited operational visibility | Real-time or near-real-time status visibility |
| Lack of inventory visibility | Centralized inventory management |

These business needs will be used as inputs when defining the business requirements and functional requirements for the proposed system.

---

## 8. Key Business Analysis Insight

The analysis shows that the main issue is not simply the availability of sales data. The more important challenge is how business information can be **organized, integrated, monitored, and transformed into actionable insights**.

The dataset demonstrates measurable differences in sales performance across countries, products, salespeople, and months. However, the dataset also has important limitations because it does not contain customer, inventory, payment, delivery, supplier, cost, or profit information.

Therefore, the proposed Smart Cosmetics Retail Management System should not be designed only as a sales dashboard. It should provide a centralized platform that connects operational processes with reporting and analytics.

The key improvement direction is:

**Fragmented Information → Centralized Data → Integrated Business Processes → Better Visibility → Data-Driven Decision-Making**

---

## 9. Transition to Gap Analysis

The identified pain points describe the problems and limitations of the current state. The next step is to compare the current capabilities with the capabilities required by the business.

The **Gap Analysis** will identify:

- What the current environment can support
- What the business needs to support
- The gaps between the current and desired states
- The capabilities required to close those gaps
- How the proposed Smart Cosmetics Retail Management System can address them

The analysis will therefore transition from:

**Pain Points → Business Gaps → Business Requirements → Proposed Solution**