# Product Inventory

Product Inventory provides real-time visibility into product quantities across all warehouses, vehicles, and storage locations. This module tracks inventory levels, movements, and helps prevent stockouts with alerts and dashboards.

**Permission:** `Pages.ProductInventory`

## Overview

The Product Inventory Dashboard provides comprehensive inventory visibility with multiple tabs for different views:

* **Dashboard** - Summary cards, inventory levels, and visual analytics
* **Activity** - Recent inventory transactions and movements
* **Delivery Orders** - Related delivery order information
* **Shipments** - Inbound and outbound shipment tracking
* **Calendar** - Schedule view of inventory activities

![Product Inventory Dashboard](../images/ProductInventory-Dashboard.PNG)
*Product Inventory Dashboard showing stock alerts, inventory levels, and charts*

## Dashboard Tab

The Dashboard tab provides a high-level overview of your inventory status:

### Stock Alert Cards

Three summary cards highlight critical inventory situations:

* **Product Out of Stock** - Products with zero or negative inventory (requires immediate attention)
* **Product Overstock** - Products exceeding maximum stock levels (may need redistribution)
* **Product Low Stock** - Products below minimum thresholds (reorder recommended)

Each card shows the count of affected products and lists specific product names.

### Product Inventory Table

The main inventory table displays:

* **Product name** - Expandable to view details
* **Levels** - Visual bar indicator showing current stock level relative to min/max
* **Total Quantity on hand** - Current available inventory
* **Total Quantity on committed** - Inventory allocated to orders
* **Total Quantity available** - On hand minus committed
* **Total Quantity on order** - Incoming inventory from purchase orders

Columns with negative values display in red to highlight inventory deficits.

### Visual Analytics

**Inventory On Hand Chart** - Bar chart showing total inventory quantities by product, providing quick visual comparison of stock levels across your product catalog.

**Orders Pending** - Table showing delivery orders awaiting fulfillment, including Type, Status, Delivery type, Customer, Order number, Order date, Deliver By, and Created By.

## Activity Tab

The Activity tab shows recent inventory transactions and movements across all warehouses.

![Product Inventory Activity](../images/ProductInventory-Activity-Tab.PNG)
*Activity tab showing inventory transactions with volume changes*

### Transaction History

Each transaction record displays:

* **Actions** - Menu for transaction operations
* **Product** - Product name
* **Location** - Customer location (if applicable)
* **Warehouse** - Warehouse where transaction occurred
* **Volume** - Quantity change with color coding:
  - Green (+) for inventory increases (receipts, blend production)
  - Red (-) for inventory decreases (consumption, deliveries)
* **Trans date** - Transaction date
* **Description** - Transaction type (e.g., "Blend Batch", "Shipment Receipt", "Delivery")
* **Comment** - Additional transaction details

### Transaction Types

Common inventory transactions include:

* **Blend Batch** - Inventory adjustments from product blending (components consumed, finished product added)
* **Shipment Receipt** - Inventory increases from received shipments
* **Delivery** - Inventory decreases from completed deliveries
* **Transfer** - Inventory movements between warehouses
* **Adjustment** - Manual inventory corrections

## Key Features

* View current inventory levels by product and warehouse
* Track inventory across multiple warehouses and vehicles
* Monitor inventory movements and transaction history
* Identify low stock, out of stock, and overstock situations
* View inventory history and complete audit trail
* Support for multiple units of measure
* Real-time inventory updates from field activities and production
* Visual inventory level indicators
* Generate and export inventory reports
* Filter and search across all inventory records

