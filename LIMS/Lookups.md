# LIMS Lookups

This page documents the lookup tables and reference data used by the LIMS (Lab Information Management System) module. These lookups provide configurable options for lab testing, sample management, and results tracking.


## Field and Test Configuration

### Field Types
**Permission:** `Pages.FieldTypes.Create`

Field Types define the data types and input methods for test result fields (e.g., Numeric, Text, Date, Picklist, Boolean) controlling how lab results are captured and validated.

### Fields
**Permission:** `Pages.Fields.Create`

Fields define the individual test parameters and measurements tracked in lab results (e.g., Iron, Chloride, pH, Water Content) with specifications and acceptable ranges.

## Lab Configuration

### Lab Agencies
**Permission:** `Pages.LabAgencies.Create`

Lab Agencies maintain the list of external laboratories that perform testing services, including contact information, capabilities, and turnaround times.

### Lab Types
**Permission:** `Pages.LabTypes.Create`

Lab Types categorize different kinds of laboratory tests (e.g., Water Analysis, Chemical Analysis, Microbiology, Product QC) for organizing test offerings and results.

## Lab Order Management

### Lab Order Status
**Permission:** `Pages.Administration.LabOrderStatus.Create`

Lab Order Status values track the lifecycle of lab orders from sample collection through result reporting (e.g., Draft, Submitted, In Progress, Completed, Cancelled).

### Lab Order Priorities
**Permission:** `Pages.Administration.LabOrderPriorities.Create`

Lab Order Priorities define urgency levels for test requests (e.g., Routine, Rush, Stat, Same Day) affecting turnaround time and cost.

### Lab Collection Points
**Permission:** `Pages.Administration.LabCollectionPoints.Create`

Lab Collection Points specify where samples are collected at a location (e.g., Wellhead, Flowline, Separator, Tank, Sales Line) for tracking sample source.

## Import and Export

### Lab Import Types
**Permission:** `Pages.LabImportTypes.Create`

Lab Import Types define formats for importing lab results from external laboratories, specifying data mapping and validation rules for each lab's result format.

### Lab Export Templates
**Permission:** `Pages.LabExportTemplates`

Lab Export Templates define the format and content for exporting lab order information to external laboratories or for generating submission documents.

## Product-Lab Linkage

### Lab Type Products
**Permission:** `Pages.LabTypeProducts.Create`

Lab Type Products link products to the types of lab tests required or available, specifying which tests are applicable for each product category.

## Related Documentation

* [LIMS Index](Index.md) - Main LIMS documentation
* [Create Lab Order](Create-Lab-Order.md) - Creating lab test orders
* [Import Lab Results](Imports-Lab-Results.md) - Importing results from external labs

