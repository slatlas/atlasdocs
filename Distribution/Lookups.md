# Distribution Lookups

This page documents the lookup tables and reference data used by the Distribution module. These lookups provide configurable options for categorizing orders, treatments, routes, and related activities.


## Delivery and Order Lookups

### Delivery Types
**Permission:** `Pages.Administration.DeliveryTypes.Create`

Delivery Types categorize different kinds of deliveries (e.g., Bulk Delivery, Tank Fill, Drum Drop, Chemical Treatment) for operational planning and reporting.

### Order Service Types
**Permission:** `Pages.Administration.OrderServiceTypes.Create`

Order Service Types define the types of services provided on orders (e.g., Regular Treatment, Emergency Service, Equipment Installation, Testing) for categorization and billing.

### Order Status
**Permission:** `Pages.Administration.OrderStatus.Create`

Order Status values track the lifecycle of orders from creation through completion (e.g., Pending, Scheduled, In Progress, Completed, Cancelled).

### Order Authorization Types
**Permission:** `Pages.Administration.OrderAuthorizationTypes.Create`

Order Authorization Types specify how orders are authorized (e.g., Standing Authorization, Phone Approval, Work Order, Emergency) for compliance and billing purposes.

## Treatment Lookups

### Treatment Types
**Permission:** `Pages.Administration.TreatmentTypes.Create`

Treatment Types categorize treatments by purpose (e.g., Corrosion Inhibitor, Scale Inhibitor, Paraffin Treatment, Biocide) for product selection and reporting.

### Treatment Routes (Lookup)
**Permission:** `Pages.TreatmentRoutes.Create`

Treatment Routes lookup table maintains the master list of route definitions that can be referenced when scheduling and planning treatments.

### Treatment Route Types
**Permission:** `Pages.Administration.TreatmentRouteTypes`

Treatment Route Types categorize routes by purpose or frequency (e.g., Daily Route, Weekly Route, Monthly Route, Special Service) for organization and scheduling.

### Treatment Schedule Frequencies
**Permission:** `Pages.TreatmentScheduleFrequencies.Create`

Treatment Schedule Frequencies define how often locations should be treated (e.g., Daily, Weekly, Bi-Weekly, Monthly, Quarterly, As Needed) for scheduling automation.

### Treatment Exception Types
**Permission:** `Pages.Administration.TreatmentExceptionTypes.Create`

Treatment Exception Types categorize reasons why scheduled treatments were not completed (e.g., Location Inaccessible, Equipment Down, Weather, No Product) for tracking and analysis.

## Shipment and Vehicle Lookups

### Shipment Containers
**Permission:** `Pages.Administration.ShipmentContainers`

Shipment Containers define container types for product shipments (e.g., Tote, Drum, Pail, Bulk Tank) for inventory and logistics tracking.

### Shipment Types
**Permission:** `Pages.Administration.ShipmentTypes`

Shipment Types categorize different shipment methods (e.g., Truck, Rail, Pipeline, Courier) for logistics planning and tracking.

### Vehicles
**Permission:** `Pages.Administration.Vehicles`

Vehicles maintains the fleet of trucks, service vehicles, and equipment used for deliveries and treatments, including vehicle specifications and maintenance records.

