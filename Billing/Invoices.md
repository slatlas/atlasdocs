# Invoices

Invoices document charges for products and services provided to customers. This module manages invoice creation, formatting, delivery, and payment tracking.

## Overview

The Invoices page manages all customer invoices from creation through payment. Invoices can be generated automatically from completed work or created manually, and support various formats and delivery methods.

## Key Features

* Generate invoices from delivery orders and treatments
* Create manual invoices for services or adjustments
* Apply customer-specific pricing and terms
* Use customizable invoice templates
* Preview invoices before finalizing
* Export invoices to PDF
* Email invoices to customers
* Track invoice status (Draft, Sent, Paid, Overdue)
* Record payments and adjustments
* Integrate with accounting systems (QuickBooks, etc.)
* Generate billing reports
* Support for recurring billing

## Invoice Components

* Customer and billing information
* Line items with descriptions, quantities, and prices
* Taxes and surcharges
* Payment terms
* Invoice notes and attachments
* Custom fields based on invoice type

## Permissions

Access to Invoices features requires the following permissions:

| Display Name | Description |
|--------------|-------------|
| Invoices | View invoice records |
| Create Invoices | Create new invoices |
| Edit Invoices | Modify existing invoices |
| Delete Invoices | Remove invoice records |
| Ready To Bill | View unbilled activities ready for invoicing |
| Invoice Items | View invoice line items |
| Create Invoice Items | Add line items to invoices |
| Edit Invoice Items | Modify invoice line items |
| Delete Invoice Items | Remove line items from invoices |

**Related Permissions:**

| Display Name | Description |
|--------------|-------------|
| [Customers](../AreaManagement/Customers.md) | View customers (invoice recipients) |
| [Delivery Orders](../Distribution/DeliveryOrders.md) | View completed deliveries (billing source) |
| [Treatments](../Distribution/Treatments.md) | View completed treatments (billing source) |
| [Sales Orders](../Distribution/SalesOrders.md) | View orders (billing reference) |
| [Price Schedules](../Product/PriceSchedules.md) | View pricing (invoice rates) |

## Related Documentation

* [Ready To Bill](ReadyToBill.md) - Review billable activities before invoicing
* [Settings - Invoice](../Web/admin/settings.md) - Configure invoice settings and templates

