# Sprintly SaaS Product Analytics Dashboard

---

# Overview

Sprintly is a fictional SaaS project management platform that enables organizations to manage projects, tasks, users, and team collaboration.

This project demonstrates an end-to-end Product Analytics solution built using **SQL Server**, **T-SQL**, **Power BI**, and a **Medallion Architecture (Bronze → Silver → Gold)**.

The solution transforms raw SaaS operational data into business-ready insights to help stakeholders monitor customer acquisition, product adoption, customer health, churn risk, and revenue growth opportunities.

---

# Business Objectives

The analytics solution was designed to answer the following business questions:

* How is Sprintly's customer base growing?
* Which acquisition channels perform best?
* How do Free and Starter customers use the platform?
* Which customers require proactive attention?
* Which Free Tier customers have the highest upgrade potential?
* How can Sprintly improve product adoption and paid conversions?

---

# Technology Stack

| Technology  | Purpose                   |
| ----------- | ------------------------- |
| SQL Server  | Data Warehouse            |
| T-SQL       | ETL & Data Transformation |
| Power BI    | Dashboard & Reporting     |
| DAX         | Business Metrics          |
| CSV Files   | Source Data               |
| Star Schema | Dimensional Modeling      |

---

# Dataset

The project uses six operational datasets.

| Dataset           | Description              |
| ----------------- | ------------------------ |
| accounts.csv      | Customer Accounts        |
| users.csv         | Users                    |
| projects.csv      | Projects                 |
| tasks.csv         | Tasks                    |
| events.csv        | Product Usage Events     |
| subscriptions.csv | Subscription Information |

---

# Solution Architecture

The project follows the **Medallion Architecture** consisting of Bronze, Silver, and Gold layers before serving analytical data to Power BI.

## Architecture Diagram

```markdown
![Architecture](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Sprintly%20Analytics%20Architecture.drawio.png)
```

---

## Bronze Layer

### Purpose

Raw Data Ingestion Layer

### Responsibilities

* Import CSV files
* Preserve raw data
* Batch Processing
* Full Load
* Truncate & Insert
* No Transformations

---

## Silver Layer

### Purpose

Data Cleansing & Standardization

### Transformations

* Duplicate Removal
* Null Handling
* Date Standardization
* Company Size Standardization
* Data Type Conversion
* Business Rule Validation
* Derived Columns
* Data Quality Checks

---

## Gold Layer

### Purpose

Business Ready Analytics Layer

### Deliverables

* Star Schema
* KPI Calculations
* Product Usage Metrics
* Customer Health Metrics
* Revenue Metrics
* Conversion Metrics
* Business Logic
* Aggregations

---

# Data Model

The Gold Layer follows a Star Schema.

## Dimension Tables

* Dim Accounts
* Dim Date

## Fact Table

* Fact Account Metrics

---

# Dashboard Overview

The solution consists of **5 analytical dashboard pages**.

---

# Dashboard Navigation

```markdown
### Collapsed Navigation

![Collapsed Navigation](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Collapsed%20Menu.png)

### Expanded Navigation

![Expanded Navigation](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Expanded%20Menu.png)
```

---

# Filter Panel

```markdown
![Filter Panel](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Filter%20Pane.png)
```

The dashboard supports interactive filtering across all report pages using:

* Subscription Plan
* Acquisition Channel
* Company Size
* Industry

---

# Dashboard Pages

---

# Business Overview

### Purpose

Provides an executive summary of Sprintly's customer base.

### KPIs

* Total Accounts
* Total Users
* Average Completion Rate
* Average Engagement Rate

### Visuals

* Monthly Customer Signups
* Subscription Plan Distribution
* Accounts by Acquisition Channel
* Accounts by Company Size

```markdown
![Business Overview](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Business%20Overview.png)
```

---

# Product Usage & Adoption

### Purpose

Analyzes customer interaction with the Sprintly platform.

### KPIs

* Average Engagement Rate
* Average Projects per Account
* Average Tasks
* Total Projects

### Visuals

* Login Activity by Subscription Plan
* Project Adoption by Subscription Plan
* Task Activity by Subscription Plan
* Customer Engagement vs Project Activity

```markdown
![Product Usage](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Product%20Usage%20and%20Adoption.png)
```

---

# Customer Health & Retention

### Purpose

Monitors customer engagement and identifies accounts requiring attention.

### KPIs

* Average Engagement Rate
* Average Active Days
* Paid Churn Rate
* Total Events

### Visuals

* Customer Health Distribution
* Average Engagement by Acquisition Channel
* Accounts Requiring Attention
* Customer Health Summary

```markdown
![Customer Health](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Customer%20Health%20and%20Retention.png)
```

---

# Revenue & Conversion Opportunities

### Purpose

Highlights opportunities to improve Free-to-Starter conversions.

### KPIs

* Total Accounts
* Paid Accounts
* Free Accounts
* Paid Conversion Rate

### Visuals

* Paid Accounts by Acquisition Channel
* Paid Conversion Rate by Acquisition Channel
* Average Days to Convert
* High-Potential Free Accounts

```markdown
![Revenue Dashboard](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Revenue%20Conversions%20and%20Opportunities.png)
```

---

# Executive Insights & Recommendations

### Purpose

Transforms analytical findings into strategic business recommendations.

### Sections

* Executive Summary
* Key Insights
* Recommended Actions

```markdown
![Executive Insights](https://github.com/jaynitdhamanskar/sprintly-saas-product-analytics-dashboard/blob/main/screenshots/Executive%20Insights%20and%20Recommendations.png)
```

---

# Key Business Insights

* Starter customers demonstrate significantly higher product adoption than Free Tier customers.
* Product engagement increases with project activity.
* Referral and Organic Search contribute the largest number of paid customers.
* Only **18.3%** of customer accounts have upgraded to the Starter plan.
* Highly engaged Free Tier customers present strong revenue opportunities.
* Customer health monitoring helps identify accounts requiring proactive intervention.

---

# Business Recommendations

* Improve product onboarding to encourage early project creation.
* Launch personalized upgrade campaigns targeting highly engaged Free Tier customers.
* Increase investment in high-performing acquisition channels.
* Monitor customer health metrics proactively.
* Promote collaborative product features to improve long-term retention.

---

# Author

**Jaynit Dhamanskar**
