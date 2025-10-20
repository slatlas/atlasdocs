# Product Management

Product Management provides comprehensive tools for managing your product catalog, inventory, warehousing, pricing, purchasing, and shipments. This module ensures you have visibility and control over all product-related operations from procurement to delivery.

**Feature Required:** `App.ProductManagementFeature`

## Overview

The Product Management module handles all aspects of product lifecycle management including product definitions, inventory tracking across warehouses and vehicles, purchase order management, pricing schedules, and shipment coordination.

## Main Components

* [Products](Products.md) - Product catalog and specifications
* [Product Inventory](ProductInventory.md) - Track inventory across warehouses and vehicles
* [Location Tank Inventory](LocationTankInventory.md) - Monitor inventory at customer locations
* [Purchase Orders](PurchaseOrders.md) - External purchase orders from vendors
* [Internal Purchase Orders](InternalPurchaseOrders.md) - Internal transfers between warehouses
* [Warehouses](Warehouses.md) - Warehouse locations and management
* [Price Schedules](PriceSchedules.md) - Customer pricing configurations
* [Shipments](Shipments.md) - Inbound and outbound shipments
* [Product Blend Batches](ProductBlendBatchs.md) - Blended product batch tracking
* [Lab QC Requests](LabQCRequests.md) - Quality control testing requests

## Lookup Tables

For configuration and reference data used by Product Management, see [Product Lookups](Lookups.md).

## Key Workflows

### Inventory Management
1. Configure [Warehouses](Warehouses.md) and storage locations
2. Maintain [Product Inventory](ProductInventory.md) across locations
3. Monitor [Location Tank Inventory](LocationTankInventory.md) at customer sites
4. Track inventory movements through [Shipments](Shipments.md)

### Procurement
1. Create [Purchase Orders](PurchaseOrders.md) for vendor purchases
2. Receive [Shipments](Shipments.md) into warehouses
3. Perform quality control via [Lab QC Requests](LabQCRequests.md)
4. Update inventory levels automatically

### Pricing
1. Define [Products](Products.md) with base pricing
2. Create [Price Schedules](PriceSchedules.md) for customer-specific pricing
3. Apply price schedules to customers, leases, or locations
4. Automatic pricing on sales orders and invoices

