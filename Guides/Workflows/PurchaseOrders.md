# Purchase Order Management

## Overview

Purchase orders document requests to purchase chemical products and materials from external vendors or transfer inventory between internal warehouses. This workflow is used by purchasing staff and warehouse managers to create purchase orders, track approval and delivery, receive shipments, and update inventory. Proper PO management ensures adequate product availability while controlling costs and maintaining accurate inventory records.

## Prerequisites

**Required Permission:** `Pages.PurchaseOrders`

**Required Setup:**
* Vendors must be configured in the system
* Products must exist in catalog
* Warehouses must be set up
* Approval workflows configured (if required)

**Related Prerequisites:**
* [Product Setup](ProductSetup.md) - Products must be defined
* [Inventory Management](InventoryManagement.md) - Understanding inventory tracking

## Workflow Diagram

```
Identify Need → Create PO (External or Internal) → Add Products/Quantities → Set Delivery Details
       ↓
Submit for Approval → Approve PO → Send to Vendor → Track Delivery
       ↓
Receive Shipment → Match to PO → Update Inventory → Close PO
```

## Step-by-Step Procedure

### Creating External Purchase Orders (from Vendors)

1. **Navigate to Purchase Orders**
   * Go to main menu → Product → Purchase Orders
   * Filter view to "External" purchase orders

2. **Create New Purchase Order**
   * Click "Create New" or "Add Purchase Order"
   * **PO Type:** Select "External" (vendor purchase)
   * **Vendor:** Select the vendor/supplier from dropdown
   * **Delivery Warehouse:** Choose destination warehouse
   * **Expected Delivery Date:** Enter estimated arrival date

3. **Add Products to PO**
   * Click "Add Product Line"
   * Select product from catalog
   * Enter quantity to order
   * Enter unit cost (or verify pre-populated cost)
   * Specify unit of measure
   * Add multiple products as needed

4. **Configure PO Details**
   * **Vendor PO Number:** Enter vendor's reference number if provided
   * **Freight Terms:** FOB, prepaid, collect, etc.
   * **Payment Terms:** Net 30, Net 60, etc.
   * **Special Instructions:** Delivery requirements, packaging notes
   * **Ship To Address:** Verify warehouse address is correct

### Creating Internal Purchase Orders (Transfers)

5. **Create Internal Transfer PO**
   * Click "Create New Purchase Order"
   * **PO Type:** Select "Internal" (inter-warehouse transfer)
   * **Source Warehouse:** Where inventory will come from
   * **Destination Warehouse:** Where inventory will go
   * **Transfer Date:** When transfer will occur

6. **Add Products to Transfer**
   * Select products to transfer
   * Enter quantities
   * System checks source warehouse has sufficient inventory
   * Cost is typically standard cost (no vendor pricing)

### Approval and Processing

7. **Review PO Totals**
   * Verify product quantities and costs
   * Check extended totals and PO grand total
   * Confirm freight and other charges if applicable

8. **Submit for Approval** (if required)
   * Click "Submit for Approval"
   * PO routes to purchasing manager or appropriate approver
   * Approval may be automatic for POs under certain dollar threshold

9. **Approve Purchase Order** (for approvers)
   * Review PO details for accuracy
   * Verify budget availability
   * Check vendor and pricing
   * Approve or reject with comments

10. **Send PO to Vendor** (for external POs)
    * Once approved, generate PO document (PDF)
    * Email or fax to vendor
    * OR use electronic PO transmission if integrated
    * Update PO status to "Sent" or "Ordered"

### Receiving and Completing

11. **Track PO Status**
    * Monitor PO list for expected deliveries
    * Follow up with vendor if delayed
    * Update expected delivery date if changed

12. **Receive Shipment**
    * When product arrives, navigate to PO
    * Click "Receive Shipment" or similar
    * See [Product Receiving and Shipments](ReceivingShipments.md) for detailed receiving process

13. **Match Receipt to PO**
    * Verify products received match PO
    * Enter actual quantities received (may differ from ordered)
    * Note any discrepancies, shortages, or damage
    * System updates inventory automatically

14. **Close Purchase Order**
    * Once fully received, mark PO as "Closed" or "Complete"
    * Partially received POs remain "Open" with outstanding balance
    * Can close with partial receipt if vendor can't fulfill completely

## Best Practices

### For Purchasing Staff
* **Monitor inventory levels** - Create POs proactively before stockouts occur
* **Consolidate orders** - Combine products when possible to reduce freight costs
* **Negotiate pricing** - Establish volume discounts and favorable terms with key vendors
* **Track lead times** - Know typical delivery timeframes for each vendor and product

### For Warehouse Managers
* **Plan storage space** - Ensure warehouse capacity for incoming shipments
* **Coordinate timing** - Schedule large deliveries when staff available to receive and stock
* **Verify quality** - Inspect products on receipt for quality and correctness
* **Maintain accuracy** - Ensure PO receiving updates inventory correctly

### Industry-Specific Tips
* **Bulk chemical orders:** Coordinate with tank capacity and storage requirements
* **Hazmat regulations:** Ensure proper placarding, documentation, and storage for hazardous materials
* **Shelf life:** Consider product expiration dates, especially for biocides and other chemicals
* **Seasonal demand:** Order ahead for high-demand seasons (freeze protection in winter, etc.)
* **Minimum orders:** Many chemical suppliers have minimum order quantities or delivery fees

## Troubleshooting

**Issue:** Cannot create PO - insufficient permissions
* **Solution:** Verify you have `Pages.PurchaseOrders` permission. May need higher approval authority for large PO amounts. Contact system administrator.

**Issue:** Vendor not in dropdown list
* **Solution:** Vendor may need to be added to system first. Navigate to Vendors to create vendor record, then return to create PO.

**Issue:** Product cost seems incorrect
* **Solution:** Check product master for standard cost. If vendor pricing is different, override the cost on PO line. May need to update product master if cost has changed permanently.

**Issue:** Cannot receive shipment - PO not showing
* **Solution:** Verify PO status is "Approved" or "Ordered," not "Draft." Check that PO was sent to vendor. If internal transfer, verify PO was properly created.

**Issue:** Received quantity doesn't match PO
* **Solution:** Document the discrepancy. Receive actual quantity received. Contact vendor about shortage or overage. May need to adjust PO, return excess, or place new order for shortage.

**Issue:** Internal transfer not reducing source warehouse inventory
* **Solution:** Verify receiving process was completed at destination warehouse. Check that internal PO type is correct. Both shipment and receipt must be recorded for inventory to update correctly.

**Where to Get Help:**
* See [Purchase Orders documentation](../../Product/PurchaseOrders.md)
* See [Internal Purchase Orders documentation](../../Product/InternalPurchaseOrders.md)
* Contact purchasing manager for vendor or approval questions
* Contact accounting for payment terms or invoice matching issues

## Related Workflows

**Upstream Processes:**
* [Product Setup](ProductSetup.md) - Products must exist in catalog
* [Inventory Management](InventoryManagement.md) - Inventory levels trigger PO need

**Downstream Processes:**
* [Product Receiving and Shipments](ReceivingShipments.md) - Next step: receive the shipment
* [Inventory Management](InventoryManagement.md) - Receiving updates inventory
* Accounts payable and vendor payment processing

**Related Documentation:**
* [Product Management Overview](../../Product/Index.md)
* [Warehouses](../../Product/Warehouses.md)
* [Vendors](../../AreaManagement/Vendors.md)

