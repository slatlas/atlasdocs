# LIMS Lookups

This page documents the lookup tables and reference data used by the LIMS (Lab Information Management System) module. These lookups provide configurable options for lab testing, sample management, and results tracking.

**Feature Required:** `App.LabInformationManagementSystemFeature`

## Field and Test Configuration

### Field Types
**Route:** `/app/main/lims/fieldTypes`  
**Permission:** `Pages.FieldTypes.Create`

Field Types define the data types and input methods for test result fields (e.g., Numeric, Text, Date, Picklist, Boolean) controlling how lab results are captured and validated.

### Fields
**Route:** `/app/main/lims/fields`  
**Permission:** `Pages.Fields.Create`

Fields define the individual test parameters and measurements tracked in lab results (e.g., Iron, Chloride, pH, Water Content) with specifications and acceptable ranges.

## Lab Configuration

### Lab Agencies
**Route:** `/app/main/management/labAgencies`  
**Permission:** `Pages.LabAgencies.Create`

Lab Agencies maintain the list of external laboratories that perform testing services, including contact information, capabilities, and turnaround times.

### Lab Types
**Route:** `/app/main/lims/labTypes`  
**Permission:** `Pages.LabTypes.Create`

Lab Types categorize different kinds of laboratory tests (e.g., Water Analysis, Chemical Analysis, Microbiology, Product QC) for organizing test offerings and results.

## Lab Order Management

### Lab Order Status
**Route:** `/app/admin/lims/labOrderStatus`  
**Permission:** `Pages.Administration.LabOrderStatus.Create`

Lab Order Status values track the lifecycle of lab orders from sample collection through result reporting (e.g., Draft, Submitted, In Progress, Completed, Cancelled).

### Lab Order Priorities
**Route:** `/app/admin/lims/labOrderPriorities`  
**Permission:** `Pages.Administration.LabOrderPriorities.Create`

Lab Order Priorities define urgency levels for test requests (e.g., Routine, Rush, Stat, Same Day) affecting turnaround time and cost.

### Lab Collection Points
**Route:** `/app/admin/lims/labCollectionPoints`  
**Permission:** `Pages.Administration.LabCollectionPoints.Create`

Lab Collection Points specify where samples are collected at a location (e.g., Wellhead, Flowline, Separator, Tank, Sales Line) for tracking sample source.

## Import and Export

### Lab Import Types
**Route:** `/app/main/lims/labImportTypes`  
**Permission:** `Pages.LabImportTypes.Create`

Lab Import Types define formats for importing lab results from external laboratories, specifying data mapping and validation rules for each lab's result format.

### Lab Export Templates
**Route:** `/app/main/lims/labExportTemplates`  
**Permission:** `Pages.LabExportTemplates`

Lab Export Templates define the format and content for exporting lab order information to external laboratories or for generating submission documents.

## Product-Lab Linkage

### Lab Type Products
**Route:** `/app/main/lims/labTypeProducts`  
**Permission:** `Pages.LabTypeProducts.Create`

Lab Type Products link products to the types of lab tests required or available, specifying which tests are applicable for each product category.

## Related Documentation

* [LIMS Index](Index.md) - Main LIMS documentation
* [Create Lab Order](Create-Lab-Order.md) - Creating lab test orders
* [Import Lab Results](Imports-Lab-Results.md) - Importing results from external labs

