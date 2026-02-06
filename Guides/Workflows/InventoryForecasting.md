# Inventory Forecasting

## Overview

Inventory forecasting helps you anticipate demand, identify stockout risks, and plan reorders before shortages occur. The Product Inventory Forecasting tab uses historical usage, treatment schedules, and delivery orders to predict demand, classify risk (Critical, High, Medium, Low), and recommend reorder quantities. Use this workflow when planning purchases, reviewing inventory health, or preparing for peak demand periods.

## Prerequisites

**Required Permission:** `Pages.ProductInventory`

**Required Setup:**
* Warehouses must be configured
* Products must be set up with inventory tracking enabled
* Sufficient transaction history for usage calculations (recommended)
* Reorder point and preferred stock level configured on product inventory (for risk and reorder recommendations)

**Related Prerequisites:**
* [Inventory Management](InventoryManagement.md) - Core inventory concepts
* [Product Setup](ProductSetup.md) - Product and inventory settings
* [Purchase Orders](PurchaseOrders.md) - Creating reorders

## Workflow Diagram

```
Open Product Inventory → Select Forecasting Tab → Choose Risk Analysis or Warehouse Forecast
       ↓
Review Summary Cards / Set Date Range → Apply Filters (days, at-risk, warehouse)
       ↓
Review Forecast Grid → Expand Rows for Detail → Act on Reorder Alerts
       ↓
Export to Excel (optional) → Create Purchase Orders for At-Risk Items
```

## Step-by-Step Procedure

### Accessing the Forecasting Tab

1. **Navigate to Product Inventory**
   * Go to main menu → Product → Product Inventory
   * Select the **Forecasting** tab (Tab 7)

2. **Choose a Sub-tab**
   * **Risk Analysis** - Demand forecasting, stockout prediction, and risk classification by product/warehouse
   * **Warehouse Forecast** - Delivery order demand vs. current inventory by warehouse and delivery date

### Using Risk Analysis

3. **Review Summary Cards**
   * **Critical Risk** - Products out of stock, stockout within 7 days, or unable to fulfill 7-day committed demand
   * **High Risk** - Stockout within 14 days, below reorder point, or insufficient for 30-day committed demand
   * **Stockout within 7 days** - Count of products expected to run out within a week
   * **Need Reorder Now** - Products that should be reordered immediately

4. **Review Alert Summary Panel**
   * See active inventory alerts by severity
   * Use this to prioritize which products to address first

5. **Use the Forecast Grid**
   * Each row is a product/warehouse combination
   * Key columns: Risk Level (color-coded), Current Quantity Available, Average Daily Usage, Estimated Days Until Stockout, Predicted Stockout Date, Forecasted Demand (7/14/30/60/90 days), Scheduled Demand, Delivery Order Demand, Total Committed Demand, Pending Supply, Recommended Reorder Quantity, Velocity Trend, Risk Reason
   * **Velocity Trend** - Percentage change in usage (7-day vs 30-day average). An alert appears when the change exceeds 25% (usage increasing or decreasing sharply)

6. **Apply Filters**
   * **Forecast days** - 30, 60, or 90 days for demand projections
   * **Only At-Risk** - Show only products with elevated risk (hide Low risk)
   * **Warehouse** - Limit to one or more warehouses

7. **Expand Rows for Detail**
   * Expand a row to see: Current State (On Hand, Available, Reorder Point, Preferred Level), Usage Analysis (7-day and 30-day averages, variance, velocity trend), Forecasted Demand by period, and Committed Demand breakdown (Treatment Schedule and Delivery Orders)

8. **Act on Reorder Alerts**
   * Use the Reorder Alerts section for products needing immediate reorder
   * Note the **Recommended Reorder Quantity**
   * Create a purchase order (see [Purchase Orders](PurchaseOrders.md)) or internal transfer as needed

9. **Export Risk Analysis**
   * Use the Excel export to share with purchasing or for offline analysis

### Using Warehouse Forecast

10. **Set Date Range**
    * **Start Date** - Default is one month back
    * **End Date** - Optional; leave blank to include all future demand

11. **Review the Grid**
    * Rows show warehouse, product, delivery date, quantity needed (from delivery orders), quantity on hand, quantity available, **difference** (on hand minus needed; negative = shortfall), on order, committed
    * Use **Difference** to see which product/date combinations are short

12. **Review Product Totals Summary**
    * Aggregated totals by product across the selected date range
    * Helps identify which products need the most attention overall

13. **Export Warehouse Forecast**
    * Export to Excel for planning or reporting

### Understanding Risk Levels

| Risk Level | Meaning |
|------------|---------|
| **Critical** | Out of stock, stockout within 7 days, or cannot fulfill 7-day committed demand. Act immediately. |
| **High** | Stockout within 14 days, below reorder point, or insufficient for 30-day committed demand. Plan reorder soon. |
| **Medium** | Stockout within 30 days, or usage velocity increasing more than 25%. Monitor and consider reordering. |
| **Low** | Adequate stock levels. No immediate action required. |

## Best Practices

### For Demand Planning
* **Review forecasting weekly** - Catch emerging shortages before they become critical
* **Compare scheduled vs. historical demand** - Treatment schedules and delivery orders drive "committed" demand; historical usage drives "forecasted" demand. Use both when deciding reorder quantities
* **Account for lead time** - Order so that **Predicted Stockout Date** is after expected receipt date

### For Reorder Decisions
* **Use Recommended Reorder Quantity as a starting point** - Adjust for minimum order quantities, promotions, or known upcoming demand
* **Check Pending Supply** - Avoid over-ordering when purchase orders are already in place
* **Watch velocity trends** - A sharp increase in usage may warrant higher safety stock or earlier reorder

### For Reporting
* **Export Risk Analysis** before key meetings to discuss at-risk products
* **Export Warehouse Forecast** to align warehouse and delivery schedules with inventory availability

## Troubleshooting

**Issue:** No data or empty forecast grid
* **Solution:** Ensure products have inventory records and transaction history. Risk Analysis uses historical usage; Warehouse Forecast uses delivery orders. Check date range and warehouse filters.

**Issue:** Risk level seems wrong for a product
* **Solution:** Risk is based on current quantity, reorder point, preferred level, average daily usage, and committed demand. Verify reorder point and preferred stock level on the product inventory record. Check that treatment schedules and delivery orders are up to date.

**Issue:** Recommended reorder quantity is zero or very small
* **Solution:** Recommendation considers current stock, reorder point, preferred level, and pending supply. If already near or above preferred level, or if pending purchase orders cover demand, the recommendation may be low. Review the detail panel for the full picture.

**Issue:** Velocity trend shows large percentage but usage is stable
* **Solution:** Velocity compares 7-day average to 30-day average. A short spike or dip in the last 7 days can cause a large percentage change. Use the expanded row Usage Analysis to see actual 7-day and 30-day averages.

**Where to Get Help:**
* See [Product Inventory](../../Product/ProductInventory.md) - Forecasting tab reference
* See [Inventory Management](InventoryManagement.md) - Day-to-day inventory workflow
* See [Purchase Orders](PurchaseOrders.md) - Creating reorders

## Related Workflows

**Upstream / Supporting:**
* [Inventory Management](InventoryManagement.md) - Monitoring levels, adjustments, and inventory setup
* [Product Setup](ProductSetup.md) - Product and reorder point configuration
* [Treatment Scheduling](TreatmentScheduling.md) - Scheduled demand feeds into forecasting

**Downstream:**
* [Purchase Orders](PurchaseOrders.md) - Create POs from reorder recommendations
* [Receiving Shipments](ReceivingShipments.md) - Inbound supply that reduces future risk

**Related Documentation:**
* [Product Inventory](../../Product/ProductInventory.md) - Full Forecasting tab documentation
* [Warehouses](../../Product/Warehouses.md) - Warehouse configuration
* [Delivery Orders](../../Distribution/DeliveryOrders.md) - Source of delivery order demand in Warehouse Forecast
