# Area Management Lookups

This page documents the lookup tables and reference data used by the Area Management module. These lookups provide configurable options for categorizing, classifying, and managing area-related entities.

**Feature Required:** `App.LeaseManagementFeature`

## Customer Lookups

### Customer Types
**Route:** `/app/main/management/customerTypes`  
**Permission:** `Pages.CustomerTypes.Create`

Customer Types categorize customer organizations (e.g., Operator, Service Company, Individual). This classification helps organize customers and can affect default settings and workflows.

### Customer Project Ledger Accounts
**Route:** `/app/admin/management/customerProjectLedgerAccounts`  
**Permission:** `Pages.Administration.CustomerProjectLedgerAccounts`

Customer Project Ledger Accounts define the accounting codes and general ledger accounts used for project-based billing and cost tracking.

### Customer Project Types
**Route:** `/app/admin/management/customerProjectTypes`  
**Permission:** `Pages.Administration.CustomerProjectTypes`

Customer Project Types categorize projects (e.g., Well Development, Maintenance Program, Special Project) for organizational and reporting purposes.

## Location Lookups

### Location Types
**Route:** `/app/admin/management/locationTypes`  
**Permission:** `Pages.Administration.LocationTypes.Edit`

Location Types define categories of locations (e.g., Well, Tank Battery, Facility, Pipeline) used to classify sites and determine available features for each location.

### Location Lift Types
**Route:** `/app/main/management/locationLiftTypes`  
**Permission:** `Pages.LocationLiftTypes`

Location Lift Types specify the artificial lift method used at a location (e.g., Pumping Unit, Gas Lift, ESP, Plunger) for production tracking and equipment management.

### Location Injection Points
**Route:** `/app/main/management/locationInjectionPoints`  
**Permission:** `Pages.LocationInjectionPoints`

Location Injection Points define where chemical treatment is applied at a location (e.g., Wellhead, Flowline, Sales Line) for treatment tracking and reporting.

### Location Event Types
**Route:** `/app/admin/management/locationEventTypes`  
**Permission:** `Pages.Administration.LocationEventTypes.Create`

Location Event Types categorize events and activities that occur at locations (e.g., Well Test, Pump Change, Downhole Work) for historical tracking.

### Location Status Types
**Route:** `/app/main/management/locationStatusTypes`  
**Permission:** `Pages.LocationStatusTypes.Create`

Location Status Types define the operational status of locations (e.g., Active, Shut-In, Abandoned, New) used to filter locations and track production status.

### Location Orientations
**Route:** `/app/main/management/locationOrientations`  
**Permission:** `Pages.LocationOrientations`

Location Orientations specify the wellbore orientation (e.g., Vertical, Horizontal, Directional) for production analysis and treatment planning.

## Personnel Lookups

### Personnel Types
**Route:** `/app/admin/management/personnelTypes`  
**Permission:** `Pages.Administration.PersonnelTypes.Create`

Personnel Types categorize field staff and employees by role (e.g., Field Technician, Pumper, Supervisor, Lab Technician) for assignment and reporting purposes.

## Field Alert Lookups

### Field Alert Types
**Route:** `/app/main/management/fieldAlertTypes`  
**Permission:** `Pages.FieldAlertTypes`

Field Alert Types categorize alerts by issue or condition (e.g., Equipment Failure, Low Tank Level, Safety Concern, Production Issue) for prioritization and routing.

## Pump Lookups

### Pumps
**Route:** `/app/main/management/pumps`  
**Permission:** `Pages.Pumps`

Pumps maintains a catalog of pump equipment used at locations, including pump specifications, maintenance history, and current assignments.

### Pump Issue Types
**Route:** `/app/main/management/pumpIssueTypes`  
**Permission:** `Pages.PumpIssueTypes`

Pump Issue Types categorize pump problems and maintenance issues (e.g., Fluid Pound, Gas Lock, Rod Failure) for tracking and analysis.

### Pump Statuses
**Route:** `/app/main/management/pumpStatuses`  
**Permission:** `Pages.PumpStatuses`

Pump Statuses define the operational state of pump equipment (e.g., Running, Down, Standby) for monitoring and reporting.

### Pump Types
**Route:** `/app/main/management/pumpTypes`  
**Permission:** `Pages.PumpTypes`

Pump Types categorize pumps by design and application (e.g., Beam Pump, Progressive Cavity, Submersible) for equipment management.

