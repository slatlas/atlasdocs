# Treatments

Treatments are records of chemical applications and services performed at customer locations. Treatment records document what was done, products used, quantities applied, and results observed.

## Overview

The Treatments page displays all treatment records across locations and timeframes. Treatments can be created manually or recorded via mobile devices in the field, capturing detailed information about each service visit.

![Treatments List](../images/Distribution-Treatments.PNG)

The Treatments grid displays all treatment records with:
* **Product** - Chemical or product applied (e.g., ELLIS GRAY BULK, WAW-592 G BULK, etc.)
* **Location** - Well or facility where treatment occurred
* **Type** - Treatment type (Oil treatments shown)
* **Treatment date** - Date of application
* **Delivered volume** - Quantity delivered/applied
* **Exception** - Special conditions (Shut In, Temporarily Abandoned, etc.)
* **Note** - Additional treatment notes
* **Sales order** - Associated sales order number
* **Delivery order** - Associated delivery order number
* **Delivery Order Type** - Consignment or Billable
* **Route** - Treatment route identifier
* **Billing Route** - Billing route code
* **Invoice** - Invoice number
* **DeliveredBy** - Personnel who performed the treatment
* **Created By** - User who created the record

The system manages 99,558 treatments with nearly 2 million individual treatment items. The interface supports:
* Creating Treatment Exceptions
* Creating new Treatments
* Exporting to Excel
* Advanced filtering and search

## Key Features

* View and search treatment history
* Record treatment details and observations
* Track products used and quantities applied
* Document treatment results and conditions
* Link treatments to delivery orders
* Capture photos and notes in the field
* Generate treatment reports
* Use treatment data for billing and analysis

## Inventory Impact

Creating a treatment can automatically deduct product from warehouse inventory. This keeps warehouse stock in sync with field usage when treatments are recorded before or without a shipment (e.g., from a truck or tank that is not yet tied to a shipment/BOL).

**When warehouse inventory is deducted**

The system deducts warehouse inventory when all of the following are true:

* The treatment is **not** a usage-type treatment
* **No shipment/BOL** exists for the treatment (no shipment item is linked)
* A **warehouse** is associated with the treatment
* **Volume** is greater than zero
* The treatment is linked to an **order or schedule** (e.g., delivery order, treatment schedule)

The deduction appears as a **Treatment Deduction** transaction in [Product Inventory](../Product/ProductInventory.md) (Activity tab).

**Smart reversal when a shipment is added**

If a shipment (and shipment item) is later created for the same treatment (e.g., when a BOL is entered), the system reverses the earlier treatment-based deduction before applying the shipment deduction. This prevents double-counting so inventory is only reduced once.

## Permissions

Access to Treatments features requires the following permissions:

| Display Name | Description |
|--------------|-------------|
| Treatments | View treatment records |
| Create Treatments | Create new treatment records |
| Edit Treatments | Modify existing treatment records |
| Delete Treatments | Remove treatment records |
| Duplicates | View and manage duplicate treatments |
| Approvals | Approve treatment records for billing |

**Related Permissions:**

| Display Name | Description |
|--------------|-------------|
| [Locations](../AreaManagement/Locations.md) | View locations (where treatments occur) |
| [Products](../Product/Products.md) | View products (used in treatments) |
| [Delivery Orders](DeliveryOrders.md) | View delivery orders (linked to treatments) |
| [Treatment Routes](TreatmentRoutes.md) | View routes (treatment organization) |
| [Invoices](../Billing/Invoices.md) | View invoices (treatments generate billing) |

## Related Documentation

* [Product Inventory](../Product/ProductInventory.md) - Inventory levels and transaction history (including treatment deductions)
* [Mobile - Treating](../Mobile/Treating.md) - Record treatments on mobile devices
* [Mobile - Treatments](../Mobile/Treatments.md) - View treatment history on mobile

