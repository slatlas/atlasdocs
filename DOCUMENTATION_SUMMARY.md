# Atlas Documentation - Menu Items Summary

This document summarizes all menu items from the Angular navigation service that have been documented.

## Documentation Created

### Core Features (5 items)
- ✓ Dashboard (Host, Portal, Tenant variants)
- ✓ Search
- ✓ Tenants
- ✓ Editions
- ✓ Help Center

### Area Management (11 main + 15 lookup items)
**Feature:** `App.LeaseManagementFeature`

Main Items:
- ✓ Customers
- ✓ Customer Projects
- ✓ Transfer Project
- ✓ Leases
- ✓ Areas
- ✓ Locations
- ✓ Location Inventory Requests
- ✓ Batteries
- ✓ Personnel
- ✓ Consignment Locations
- ✓ Vendors
- ✓ Field Alerts

Lookup Items: Customer Types, Customer Project Ledger Accounts, Customer Project Types, Location Types, Location Lift Types, Location Injection Points, Location Event Types, Location Status Types, Location Orientations, Personnel Types, Field Alert Types, Pumps, Pump Issue Types, Pump Statuses, Pump Types

### Distribution (9 main + 11 lookup items)
**Feature:** `App.BillingManagementFeature`

Main Items:
- ✓ Delivery Orders
- ✓ Order Scheduling
- ✓ Sales Orders
- ✓ Order Tracker
- ✓ Treatments
- ✓ Treatment Routes
- ✓ Treatment Approvals
- ✓ Route Tracker

Lookup Items: Delivery Types, Order Service Types, Order Status, Order Authorization Types, Treatment Types, Treatment Routes, Treatment Route Types, Treatment Schedule Frequencies, Treatment Exception Types, Shipment Containers, Shipment Types, Vehicles

### Product Management (10 main + 7 lookup items)
**Feature:** `App.ProductManagementFeature`

Main Items:
- ✓ Products
- ✓ Product Inventory
- ✓ Location Tank Inventory
- ✓ Purchase Orders
- ✓ Internal Purchase Orders
- ✓ Warehouses
- ✓ Price Schedules
- ✓ Shipments
- ✓ Product Blend Batches
- ✓ Lab QC Requests

Lookup Items: Product Categories, Product Types, Vehicles, Vehicle Types, Warehouses, Warehouse Divisions, Product QC Fields

### Billing (2 main + 9 lookup items)
**Feature:** `App.BillingManagementFeature`

Main Items:
- ✓ Ready To Bill
- ✓ Invoices

Lookup Items: Billing Periods, Invoice Templates, Invoice Terms, Invoice Types, Price Schedule Calculation Types, Price Schedule Fee Types, Sales Tax Codes, Sales Types

### LIMS (1 main + 11 lookup items)
**Feature:** `App.LabInformationManagementSystemFeature`

Main Item:
- ✓ LIMS Dashboard (already documented)
- ✓ Added Lookups documentation

Lookup Items: Field Types, Fields, Lab Agencies, Lab Order Status, Lab Import Types, Lab Type Products, Lab Order Priorities, Lab Collection Points, Lab Export Templates, Lab Types

### Standalone Features (4 items)
- ✓ Calendar
- ✓ Production (Location Productions)
- ✓ Frac Jobs (Feature: `App.FracJobsFeature`)
- ✓ Reports (Feature: `App.ReportsFeature`)

### Administration Section

#### Schedules (6 items)
- ✓ Schedules
- ✓ Schedule Field Types
- ✓ Schedule Parameter Types
- ✓ Schedule Time Frames
- ✓ Schedule Types
- ✓ Background Job Logs

#### System (13 items)
- ✓ Settings (Host/Tenant) - referenced existing documentation
- ✓ Roles - referenced existing documentation
- ✓ Users
- ✓ QuickBooks Authentication Sessions
- ✓ Email Templates
- ✓ Invoice Statuses
- ✓ Mobile Logs
- ✓ Audit Logs
- ✓ Visual Settings (UI Customization)
- ✓ Languages
- ✓ Organization Units
- ✓ Maintenance
- ✓ Subscription Management
- ✓ Integrations
- ✓ Dynamic Extensions

#### Analytics (3 items)
- ✓ Dashboards
- ✓ Dashboard Builder
- ✓ Queries

#### Other Admin (1 item)
- ✓ Location Matchers

#### Lookup Organization
- ✓ Lookup Index
- ✓ Billing Lookups Index
- ✓ Area Management Lookups Index
- ✓ Distribution Lookups Index
- ✓ LIMS Lookups Index
- ✓ Product Lookups Index
- ✓ Misc Lookups Index

## Total Documentation Files Created

- **75+ documentation files** covering all active menu items
- Organized by functional area as requested
- Grouped by feature flags as requested
- Each item includes 1-2 sentence basic description
- Includes route paths and permission requirements
- Cross-referenced related documentation

## File Structure

```
/Dashboard/Index.md
/Search/Index.md
/Tenants/Index.md
/Editions/Index.md
/HelpCenter/Index.md
/AreaManagement/
  - Index.md
  - Customers.md
  - CustomerProjects.md
  - [11 main items...]
  - Lookups.md
/Distribution/
  - Index.md
  - DeliveryOrders.md
  - [8 more items...]
  - Lookups.md
/Product/
  - Index.md
  - Products.md
  - [9 more items...]
  - Lookups.md
/Billing/
  - Index.md
  - ReadyToBill.md
  - Invoices.md
  - Lookups.md
/LIMS/
  - [existing files...]
  - Lookups.md (new)
/Calendar/Index.md
/Production/Index.md
/FracJobs/Index.md
/Reports/Index.md
/Administration/
  - Index.md
  - LocationMatchers.md
  - Dashboards.md
  - DashboardBuilder.md
  - Queries.md
  - Schedules/
    - Index.md
    - [6 schedule items...]
  - Lookup/
    - Index.md
    - [6 lookup category indexes...]
/System/
  - Index.md
  - Users.md
  - [12 more system items...]
```

## Notes

- Documentation follows the basic description format (1-2 sentences) as requested
- All active menu items from the navigation service are documented
- Commented-out items were excluded as requested
- Organization is by functional area with feature flag groupings
- Each document includes route, permission, and feature requirements where applicable

