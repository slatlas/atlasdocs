# Miscellaneous Lookup Tables

This page documents general-purpose lookup tables used across multiple modules in Atlas.

**Feature Required:** `App.LeaseManagementFeature`

## Document and Note Lookups

### Document Types
**Route:** `/app/admin/management/documentTypes`  
**Permission:** `Pages.Administration.DocumentTypes.Create`

Document Types categorize documents and files attached to records (e.g., Contracts, Photos, Reports, Certificates, Correspondence) for organization and retrieval.

### Note Types
**Route:** `/app/admin/management/noteTypes`  
**Permission:** `Pages.Administration.NoteTypes.Create`

Note Types categorize notes and comments added to records (e.g., General Note, Phone Call, Meeting, Field Observation, Issue) for filtering and reporting.

## Query and Analytics Lookups

### Query Types
**Route:** `/app/admin/analytics/queryTypes`  
**Permission:** `Pages.Administration.QueryTypes.Create`

Query Types categorize custom data queries (e.g., Reporting, Export, Audit, Analysis) for organization and access control.

## Schedule Lookups

### Schedule Field Types
**Route:** `/app/main/jobs/scheduleFieldTypes`  
**Permission:** `Pages.ScheduleFieldTypes.Create`

Schedule Field Types define custom fields that can be added to schedule configurations for capturing job-specific information.

## Sales Lookups

### Sales Types
**Route:** `/app/admin/billing/salesTypes`  
**Permission:** `Pages.Administration.SalesTypes.Create`

Sales Types categorize sales transactions (e.g., Product Sale, Service Revenue, Rental Income, Freight Charge) for revenue classification and reporting. This lookup appears in both Billing and Miscellaneous sections.

