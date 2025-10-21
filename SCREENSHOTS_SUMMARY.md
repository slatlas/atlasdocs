# Atlas Documentation Screenshots Summary

## Overview
This document provides a summary of all screenshots captured from the Atlas Oil Field Chemical Inventory & Treatment Software (Sandbox Environment) on October 20, 2025.

**Important:** All screenshots contain customer names, usernames, and other sensitive data that need to be masked before publication.

## Screenshots Captured

### Login & Dashboard
1. **Login-Page.PNG** - Main login page showing username/password fields and language selection
2. **Dashboard-Main.PNG** - Main dashboard with:
   - Sales Summary chart (showing ~$2M in sales)
   - Recent activities (Lab Orders, Customers, Leases, Locations)
   - Lab turnaround time metrics
   - Top Locations map

### Area Management Section (10 screenshots)
3. **AreaManagement-Customers.PNG** - Customer list showing 1,207 customers
   - Columns: Type, Name, Account Id, Title, Email, Address, City, State, Zip, Is Active
   - Examples: 1776 ENERGY OPERATORS LLC, 3FEARNS LLC, 3-T EXPLORATION INC, etc.

4. **AreaManagement-CustomerProjects.PNG** - Customer Projects dashboard
   - Planned vs Actual Revenue chart
   - Project Search with filters (Customer, Project Manager, Status, Project number)
   - Job Type and Activity Type filters
   - Shows active projects with progress tracking

5. **AreaManagement-Leases.PNG** - Leases list showing 14,045 total leases
   - Columns: Lease, Ship To, Customer, Area, Alias, Polygon, Is Active
   - Examples: DEXTER FEDERAL, LIVE OAK, #46 INPEX, 10' UCAR, etc.

6. **AreaManagement-Areas.PNG** - Areas list showing 766 areas
   - Columns: Area, Is Active
   - Examples: Dollarhide, Tatia, TEXAS, SUNDOWN, LEVELLAND, KINGDOM, etc.

7. **AreaManagement-Locations.PNG** - Locations list showing 75,028 locations
   - Columns: Location, Customer, Lease, Type, Is Active, Ship To, Alias, API, Code, Tank Size
   - Multiple tabs: Location Search, Map
   - Shows batteries, sample sites, producing wells

8. **AreaManagement-Batteries.PNG** - Batteries list showing 4,154 batteries
   - Columns: Name, Ship To, Lease, Alias, Is Active, Polygon, Code
   - Examples: SSU BATTERY, BSB BATTERY, TSE BATTERY, etc.

9. **AreaManagement-Personnel.PNG** - Personnel list showing 743 personnel
   - Columns: Name, Type, Title, Manager, Is Active, Create date, Modify date, MobileVersion, MobileSystem
   - Shows service technicians, account managers, field technicians

10. **AreaManagement-ConsignmentLocations.PNG** - Consignment locations showing 66 locations
    - Columns: Name, Polygon
    - Examples: APA-ART-COFFEE, APA-ART-TONY, APA-ART-LEE, etc.

11. **AreaManagement-Vendors.PNG** - Vendors list (currently showing 0 vendors)
    - Columns: Name, Primary address, Secondary address, City, State, Zip, County, Country, Email, etc.

12. **AreaManagement-FieldAlerts.PNG** - Field alerts list (currently showing 0 alerts)
    - Columns: Name, Message, End date

### Distribution Section (3 screenshots)
13. **Distribution-DeliveryOrders.PNG** - Delivery Order Dashboard showing 49,114 total orders
    - Tabs: All Orders (49114), Unscheduled (10), Scheduled (144), Ready To Bill (181), Completed (47632), On Hold (34), Summary
    - Columns: Status, Type, Delivery type, Customer, Order number, Order date, Requested date, ScheduleRange, Created By, Ordered, Scheduled, Treated, Exception, Invoiced
    - Shows Consignment and Billable order types
    - Status indicators: Scheduled (yellow), Requested (blue), Invoiced (green)
    - Filter options by Priority, Status, and Batch

14. **Distribution-SalesOrders.PNG** - Sales orders list showing 22,854 total orders
    - Columns: Status, Order number, Customer, Created By, Date, Ordered, Invoiced, Approved
    - All orders showing "Ready for Billing" status
    - Examples: RILEY PERMIAN OPERATING CO, RUBICON OIL & GAS LLC, HILCORP - SUNDOWN

15. **Distribution-Treatments.PNG** - Treatments list showing 99,558 treatments (1,991,160 items)
    - Columns: Product, Location, Type, Treatment date, Delivered volume, Exception, Note, Sales order, Delivery order, Delivery Order Type, Route, Billing Route, Invoice, DeliveredBy, Created By
    - Shows bulk treatments for various products (WAW-592 G BULK, CRW-232 G BULK, etc.)
    - Locations include wells, stations, and facilities
    - Exception statuses: Shut In, Temporarily Abandoned
    - Routes tracked (SNYDER, 9017-Wildfire, 9018-Wildfire, 9018)

### LIMS (Laboratory Information Management System) (1 screenshot)
16. **LIMS-Dashboard.PNG** - LIMS Dashboard showing 223,185 total orders
    - Tabs: All Orders (223185), Requested (810), Processing (841), Completed (0), Approved (0), Reported (225079)
    - Columns: Status, Limits, Type, Sample id, Priority, Location, LocationAlias, Sample Point, Lease, Customer, Product, Requested, Personnel
    - Status indicators: Requested (blue), Processing (yellow), Invoiced (green)
    - Priority levels: Critical, Standard, Rush
    - Test types: Technical Service Request, CWA Fe/Mn/P/PO4, Heat Transfer, Amine - Residual, Polyacrylate Residual, CWA, Coolant
    - Shows requests from various customers (APACHE CORP, UNITEX OIL & GAS LLC, DIAMONDBACK E&P, VANTAGE SPECIALTIES, BOGS, KINDER MORGAN)

### Product Section (1 screenshot)
17. **Product-Inventory.PNG** - Product Inventory Dashboard
    - Total Warehouse Inventory summary:
      - Product Out of Stock: 242
      - Product Overstock: 195
      - Product Low Stock: 242
    - Tabs: Dashboard, Activity, Delivery Orders, Shipments, Calendar
    - Product Inventory grid with columns: Product name, Levels (visual indicator), Total Quantity on hand, Total Quantity on committed, Total Quantity available, Total Quantity on order
    - Examples: SCALE INHIB 1027-S, 10% Glacial Acetic Acid, 142 CLEANING SOLVENT, 2K7 GRANULAR #BULK, 2K7® BUGSTICK / SLIMSTICK 1E

### Reports Section (1 screenshot)
18. **Reports-Main.PNG** - Reports page (currently showing 0 reports)
    - Columns: Name, Creation time, Last modification time, Is deleted, Deletion time, Dialog, Description
    - "Create new report" button available

## System Information
- **System**: Atlas Tier I - 50,000 Locations
- **API Version**: v9.1.0
- **Client Version**: v9.1.0 [20251009]
- **Environment**: SANDBOX ACCOUNT (clearly marked with red banner)
- **Logged in as**: tm\admin
- **Login date**: October 15, 2025 - October 20, 2025

## Menu Structure Documented

### Main Navigation
1. **Dashboard** - Main landing page
2. **Search** - Global search functionality
3. **Area Management** (11 sub-items)
   - Customers
   - Customer projects
   - Leases
   - Areas
   - Locations
   - Location Inventory Routes
   - Batteries
   - Personnel
   - Consignment locations
   - Vendors
   - Field alerts

4. **Distribution** (8 sub-items)
   - Delivery orders
   - Order Scheduling
   - Sales orders
   - Order Tracker
   - Treatments
   - Treatment Routes
   - Treatment Approvals
   - Route Tracker

5. **Product** (10 sub-items)
   - Products
   - Product inventory
   - Location Tank Inventory
   - Purchase orders
   - Internal Purchase Orders
   - Warehouses
   - Price schedules
   - Shipments
   - Product blend batches
   - Product QC requests

6. **Billing** (sub-items identified but not fully captured)

7. **Production** - Location Productions

8. **Reports** - Report management and creation

9. **LIMS** - Laboratory Information Management System

10. **Administration** (5 main sub-items with further sub-menus)
    - Lookup
    - Location matchers
    - Schedules
    - Reports
    - System

### User Menu (Right top corner)
- Profile picture/avatar
- Username: tm\admin
- Logout option
- Manage linked accounts
- Manage authority delegations
- Change password
- Login attempts
- Change profile picture
- My settings
- Personnel View
- Download collected data

## Data Volume Summary
Based on the captured screenshots:
- **Customers**: 1,207
- **Leases**: 14,045
- **Areas**: 766
- **Locations**: 75,028
- **Batteries**: 4,154
- **Personnel**: 743
- **Consignment Locations**: 66
- **Delivery Orders**: 49,114
- **Sales Orders**: 22,854
- **Treatments**: 99,558 (1,991,160 items)
- **LIMS Orders**: 223,185
- **Product Low Stock Items**: 242
- **Product Overstock Items**: 195

## Key Features Observed
1. **Advanced filtering** on most grid pages
2. **Export to Excel** functionality
3. **Mass operations** (Mass Order, Mass Approve, etc.)
4. **Status tracking** with color-coded indicators
5. **Dashboard metrics** with charts and KPIs
6. **Map integration** for location visualization
7. **Calendar views** for scheduling
8. **Batch operations** for treatments and orders
9. **Template support** for orders and operations
10. **Multi-language support** (shown on login page)

## Next Steps - Data Masking Required
All screenshots contain sensitive information that needs to be masked:
1. **Customer names** - All company names in grids and dropdowns
2. **Usernames** - Personnel names, created by, assigned to fields
3. **Location names** - Specific well and lease names
4. **Account IDs** - Customer account numbers
5. **Email addresses** - Any visible email fields
6. **Phone numbers** - Any visible contact information
7. **Addresses** - Street addresses, coordinates

## Screenshot Naming Convention
- `[Section]-[Subsection/Feature].PNG`
- Examples:
  - `AreaManagement-Customers.PNG`
  - `Distribution-DeliveryOrders.PNG`
  - `LIMS-Dashboard.PNG`

## Documentation Files to Update
Based on the project structure, these files should be updated with the new screenshots:
- `/AreaManagement/Customers.md`
- `/AreaManagement/CustomerProjects.md`
- `/AreaManagement/Leases.md`
- `/AreaManagement/Areas.md`
- `/AreaManagement/Locations.md`
- `/AreaManagement/Batteries.md`
- `/AreaManagement/Personnel.md`
- `/AreaManagement/ConsignmentLocations.md`
- `/AreaManagement/Vendors.md`
- `/AreaManagement/FieldAlerts.md`
- `/Distribution/DeliveryOrders.md`
- `/Distribution/SalesOrders.md`
- `/Distribution/Treatments.md`
- `/LIMS/Index.md` or `/LIMS/LIMS-Management-Dashboard.md`
- `/Product/*.md` files
- `/Reports/Index.md`
- `/Dashboard/Index.md`
- `/Web/Login.md`

---
*Generated: October 20, 2025*
*Total Screenshots: 18*
*Environment: tm-sb.sourcelogicatlas.com (Sandbox)*

