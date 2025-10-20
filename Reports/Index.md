# Reports

Reports provides a library of pre-built and custom reports for analyzing operations, production, treatments, billing, and other business data. This module enables data-driven decision making across all areas of the business.

**Route:** `/app/main/reporting/reports`
**Permission:** `Pages.Reports`
**Feature Required:** `App.ReportsFeature`

## Overview

The Reports module offers comprehensive reporting capabilities covering all aspects of Atlas operations. Reports can be filtered, scheduled, exported, and customized to meet specific business needs.

## Key Features

* Browse report catalog by category
* Filter and parameterize reports
* Schedule automatic report generation
* Export reports to PDF, Excel, or CSV
* Email reports to distribution lists
* Create custom reports using report builder
* Save report favorites and presets
* View report history
* Dashboard integration for key metrics

## Report Categories

* **Production Reports** - Well production, trends, and performance
* **Treatment Reports** - Treatment history, products used, effectiveness
* **Billing Reports** - Invoices, revenue, accounts receivable
* **Inventory Reports** - Stock levels, usage, replenishment
* **Operations Reports** - Field activities, route performance, exceptions
* **Lab Reports** - Test results, trends, compliance
* **Customer Reports** - Customer-specific operations and billing
* **Management Reports** - KPIs, dashboards, executive summaries

## Report Formats

* **Tabular** - Grid-based data tables
* **Charts** - Graphs and visualizations
* **Dashboard** - Multi-metric displays
* **Custom** - User-defined layouts

## Scheduling Reports

Reports can be scheduled to run automatically:
* Daily, weekly, monthly, or custom frequencies
* Automatic email delivery
* Saved to document repository
* Alert notifications on specific conditions

## Lookup Tables

### Report Types
**Route:** `/app/admin/reporting/reportTypes`  
**Permission:** `Pages.Administration.ReportTypes`  
**Feature Required:** `App.ReportsFeature`

Report Types categorize reports by purpose and content (e.g., Operational, Financial, Regulatory, Customer-Facing) for organization and access control.

### Report Time Periods
**Route:** `/app/admin/reporting/reportTimePeriods`  
**Permission:** `Pages.Administration.ReportTimePeriods`  
**Feature Required:** `App.ReportsFeature`

Report Time Periods define standard date ranges for reports (e.g., Last 7 Days, Month to Date, Last Month, Quarter to Date, Year to Date, Custom Range).

### Report Categories
**Route:** `/app/admin/reporting/reportCategories`  
**Permission:** `Pages.Administration.ReportCategories`  
**Feature Required:** `App.ReportsFeature`

Report Categories organize reports into logical groupings (e.g., Production, Billing, Inventory, Operations, Lab) for easier browsing and discovery.

