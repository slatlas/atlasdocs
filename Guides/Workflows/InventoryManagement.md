# Inventory Management

## Overview

Inventory management provides visibility and control over chemical product quantities across all warehouse locations and service vehicles. This workflow is used by warehouse staff and inventory controllers to monitor inventory levels, track movements, identify low stock situations, and handle inventory adjustments. Accurate inventory management ensures product availability for field operations while minimizing carrying costs and waste.

## Prerequisites

**Required Permission:** `Pages.ProductInventory`

**Required Setup:**
* Warehouses must be configured
* Products must be set up with inventory tracking enabled
* Vehicles configured as mobile warehouses (if applicable)
* Inventory transaction history maintained

**Related Prerequisites:**
* [Product Setup](ProductSetup.md) - Products must be configured
* [Purchase Orders](PurchaseOrders.md) - Understanding inbound inventory

## Workflow Diagram

```
View Inventory Levels → Monitor by Location → Identify Low Stock → Create Purchase Orders
       ↓
Receive Shipments → Physical Inventory Counts → Adjust for Discrepancies → Analyze Usage
       ↓
Optimize Stock Levels → Report Inventory Value
```

## Step-by-Step Procedure

### Monitoring Inventory Levels

1. **Navigate to Product Inventory**
   * Go to main menu → Product → Product Inventory
   * View shows all products across all locations

2. **View Inventory by Product**
   * See total on-hand quantity for each product
   * View breakdown by warehouse location
   * Check quantities on service vehicles
   * Review reserved vs. available quantities

3. **Filter and Search**
   * Filter by warehouse, product category, or product type
   * Search for specific products
   * Sort by quantity (low to high) to identify shortages
   * Filter by product status (active, inactive, discontinued)

4. **Check Inventory Details**
   * Click on product to see detailed inventory
   * View inventory by warehouse/division
   * See transaction history (receipts, issues, adjustments)
   * Check reorder points and safety stock levels

### Identifying and Addressing Low Stock

5. **Review Low Stock Alerts**
   * System highlights products below minimum levels (red/yellow indicators)
   * Review reorder point settings
   * Check lead time for reordering

6. **Calculate Reorder Quantity**
   * Consider: current usage rate, lead time, minimum order quantity
   * Check for pending purchase orders
   * Account for seasonal demand fluctuations

7. **Create Purchase Order**
   * From inventory screen, click "Create PO" or navigate to Purchase Orders
   * See [Purchase Order Management](PurchaseOrders.md) workflow
   * System may auto-suggest reorder quantity

### Handling Inventory Movements

8. **Track Inbound Inventory**
   * Monitor purchase orders and expected receipts
   * See [Product Receiving and Shipments](ReceivingShipments.md)
   * Inventory updates automatically upon receipt

9. **Track Outbound Inventory**
   * Inventory depletes when field personnel complete treatments
   * Deliveries to customers reduce warehouse inventory
   * Transfers between warehouses tracked automatically

10. **Process Manual Adjustments**
    * For inventory corrections (shrinkage, damage, etc.)
    * Navigate to inventory adjustment function
    * Select product and warehouse
    * Enter adjustment quantity (positive or negative)
    * **Reason Code:** Select reason (damage, expired, physical count variance, etc.)
    * **Notes:** Document details of adjustment
    * Submit for approval if required

### Physical Inventory Counts

11. **Conduct Physical Counts**
    * Schedule regular physical inventory counts (monthly, quarterly, annually)
    * Print inventory count sheets or use mobile counting app
    * Count actual product on hand
    * Record counts in system

12. **Compare to System**
    * System compares physical count to book quantity
    * Calculate variances (overages and shortages)
    * Investigate large discrepancies

13. **Adjust Inventory to Physical**
    * Create adjustment transactions for variances
    * Update system inventory to match physical count
    * Document reasons for significant variances

### Inventory Analysis and Optimization

14. **Analyze Inventory Turns**
    * Review how quickly products move (turnover rate)
    * Identify slow-moving or obsolete inventory
    * Consider reducing stock levels for slow movers

15. **Review Usage Patterns**
    * Track consumption by product
    * Identify trends (seasonal, customer-specific)
    * Adjust reorder points based on actual usage

16. **Optimize Stock Levels**
    * Balance having enough stock vs. carrying excess
    * Adjust minimum and maximum levels
    * Consider storage costs and product shelf life

17. **Generate Inventory Reports**
    * Inventory valuation reports
    * Movement/transaction reports
    * Aging reports (identify old stock)
    * ABC analysis (high value vs. high volume products)

## Best Practices

### For Warehouse Staff
* **FIFO rotation** - Use first-in, first-out to minimize expired product (First In, First Out)
* **Organize logically** - Store products by category, usage frequency, or customer
* **Label clearly** - Ensure all product locations are clearly labeled and inventory is identifiable
* **Report issues immediately** - Notify management of damaged, leaking, or expired product

### For Inventory Controllers
* **Count regularly** - Don't wait for year-end; do cycle counts monthly or quarterly
* **Investigate variances** - Understand why inventory doesn't match books (theft, errors, leaks)
* **Set appropriate levels** - Balance availability with carrying costs
* **Monitor trends** - Track usage patterns to predict future needs

### Industry-Specific Tips
* **Chemical stability:** Monitor shelf life - some chemicals degrade over time
* **Temperature control:** Some products require climate-controlled storage
* **Hazmat storage:** Follow regulations for storing hazardous materials, including separation requirements
* **Bulk vs. packaged:** Track large bulk tanks separately from smaller packaged products
* **Emergency stock:** Maintain safety stock for critical corrosion/scale inhibitors

## Troubleshooting

**Issue:** Inventory shows negative quantity
* **Solution:** Indicates more product used than system shows available. Review recent transactions to find error. May need to adjust inventory upward or research why usage wasn't recorded correctly.

**Issue:** Physical count doesn't match system
* **Solution:** Common causes: unreported usage, receiving errors, theft/loss, product transfer not recorded. Investigate recent activity and adjust inventory to match physical count.

**Issue:** Low stock alert but product was just received
* **Solution:** Verify shipment was properly received in system. Check that receiving was posted to correct warehouse. Ensure reorder point settings are appropriate.

**Issue:** Cannot find product in inventory
* **Solution:** Product may be marked inactive. Check product status. Verify product is set up with inventory tracking enabled. Check if looking in correct warehouse.

**Issue:** Inventory value seems incorrect
* **Solution:** Check product cost in product master. Verify recent purchases are at correct cost. Run inventory revaluation if product costs have changed. May need accounting review.

**Where to Get Help:**
* See [Product Inventory documentation](../../Product/ProductInventory.md)
* See [Warehouses documentation](../../Product/Warehouses.md)
* Contact warehouse manager for physical inventory questions
* Contact purchasing for reorder and vendor questions
* Contact accounting for inventory valuation questions

## Related Workflows

**Upstream Processes:**
* [Purchase Order Management](PurchaseOrders.md) - Brings inventory in
* [Product Receiving and Shipments](ReceivingShipments.md) - Adds to inventory
* [Product Setup](ProductSetup.md) - Product configuration

**Downstream Processes:**
* [Field Treatment Execution](FieldTreatments.md) - Depletes inventory
* [Delivery Order Management](DeliveryOrders.md) - Allocates inventory
* Financial and cost accounting processes

**Related Documentation:**
* [Product Management Overview](../../Product/Index.md)
* [Location Tank Inventory](../../Product/LocationTankInventory.md) - Customer site inventory

