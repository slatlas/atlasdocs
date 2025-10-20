# Product Receiving and Shipments

## Overview

Product receiving documents the receipt of chemical shipments from vendors and updates warehouse inventory. This workflow is used by receiving clerks and warehouse staff to receive vendor deliveries against purchase orders, verify quantities and quality, record discrepancies, and update inventory. Proper receiving ensures inventory accuracy and identifies problems with vendors or shipments.

## Prerequisites

**Required Permission:** `Pages.Shipments`

**Required Setup:**
* Purchase orders must exist and be approved
* Warehouse locations configured
* Products must be in system
* Bill of lading and packing slip available from driver

**Related Prerequisites:**
* [Purchase Order Management](PurchaseOrders.md) - PO must be created first

## Workflow Diagram

```
Shipment Arrives → Verify Paperwork → Create Shipment Receipt → Match to PO → Inspect Products
       ↓
Enter Quantities Received → Note Discrepancies → Complete Receipt → Update Inventory
       ↓
Forward Documents to Accounting → File Documentation
```

## Step-by-Step Procedure

### Receiving the Shipment

1. **Shipment Arrival**
   * Driver delivers product to warehouse
   * Obtain bill of lading (BOL) and packing slip
   * Get driver signature/stamp on delivery paperwork
   * Note time of arrival

2. **Review Shipping Documents**
   * Check BOL for: PO number, product descriptions, quantities
   * Verify shipping address is correct
   * Note carrier name and tracking number
   * Check for special handling instructions or hazmat labels

3. **Navigate to Shipments**
   * Go to main menu → Product → Shipments
   * Click "Create New Shipment" or "Receive Shipment"

4. **Create Shipment Record**
   * **Shipment Type:** Inbound, vendor delivery
   * **Shipment Date:** Date received
   * **Carrier:** Transportation company
   * **Tracking/BOL Number:** From shipping documents
   * **Receiving Warehouse:** Where product is being delivered

### Matching to Purchase Order

5. **Link to Purchase Order**
   * Enter or search for PO number
   * System displays PO details and expected products
   * Verify PO matches shipping documents

6. **Review Expected Items**
   * System shows products and quantities ordered on PO
   * Compare to packing slip and actual delivery
   * Note any immediate discrepancies (missing items, etc.)

### Physical Inspection and Counting

7. **Unload and Inspect**
   * Unload product from truck
   * Check for: damage, leaks, dented containers, torn bags
   * Verify product labels match packing slip
   * Check hazmat labels are intact
   * Take photos of any damage

8. **Count Quantities**
   * Count drums, totes, pallets, cases, etc.
   * Weigh bulk deliveries if applicable
   * Use inventory scale for verification
   * Double-check counts for accuracy

9. **Enter Received Quantities**
   * In shipment record, enter actual quantities for each product
   * Confirm unit of measure (drums, gallons, pounds, etc.)
   * System compares to PO quantities

### Handling Discrepancies

10. **Document Shortages**
    * If received less than ordered:
    * Enter actual quantity received
    * Note shortage amount
    * Mark as partial receipt
    * Document on shipping paperwork
    * Photo the packing slip showing quantity

11. **Document Overages**
    * If received more than ordered:
    * Enter actual quantity
    * Note overage
    * May need to reject excess or contact vendor
    * Don't receive more than ordered without approval

12. **Document Damage or Quality Issues**
    * Note damaged items on BOL before driver leaves
    * Take photos of damage
    * Set damaged product aside - don't put in stock
    * May need to file freight claim
    * Contact vendor about replacements

13. **Handle Incorrect Products**
    * If wrong product delivered:
    * Do not receive in system
    * Note on BOL and shipment
    * Set aside for return or rejection
    * Contact vendor immediately

### Completing the Receipt

14. **Review Receipt Totals**
    * Verify all products accounted for
    * Check that quantities entered are correct
    * Review any notes or exceptions

15. **Complete Shipment Receipt**
    * Click "Complete Receipt" or "Finalize"
    * System updates purchase order:
      * Fully received → PO closes
      * Partially received → PO remains open for balance
    * Inventory updated automatically

16. **Put Away Product**
    * Move product to designated warehouse location
    * Store per product requirements (temperature, separation, etc.)
    * Update bin locations if tracked
    * Rotate stock (older product to front - FIFO)

### Documentation and Follow-up

17. **Forward Documents to Accounting**
    * Provide copy of BOL, packing slip, receipt
    * Accounting matches to vendor invoice for payment
    * Note any discrepancies for vendor billing adjustments

18. **File Documentation**
    * Maintain copies of receiving documents
    * Attach to purchase order file
    * Photos of damage filed with freight claims

19. **Follow Up on Issues**
    * Contact vendor about shortages or damage
    * Request reshipment or credit
    * File freight claims if carrier responsible
    * Update PO if needed for reorder

## Best Practices

### For Receiving Clerks
* **Inspect immediately** - Check product as soon as it's unloaded while driver is present
* **Document everything** - Photos and detailed notes protect against disputes
* **Note on BOL** - Have driver sign for noted shortages/damage before leaving
* **Verify carefully** - Take time to count accurately - errors are costly

### For Warehouse Staff
* **Check safety** - Inspect for leaks or hazmat issues before moving product
* **Store properly** - Follow chemical storage requirements and separation rules
* **Rotate stock** - Always put new stock behind old (FIFO principle)
* **Label locations** - Keep warehouse organized and product easy to find

### Industry-Specific Tips
* **Hazmat certification:** Many chemicals require special handling - ensure staff trained
* **Temperature-sensitive:** Some products must be stored in climate control
* **Bulk deliveries:** Verify tank meters and compare to BOL volume
* **Tote tracking:** Track tote serial numbers for return/exchange programs
* **Sample retention:** Keep samples of received product for QC if disputes arise

## Troubleshooting

**Issue:** Cannot find purchase order
* **Solution:** Verify PO number from shipping documents. Check that PO was approved and sent to vendor. If emergency delivery, may need to create PO retroactively.

**Issue:** Product on delivery not on PO
* **Solution:** Verify vendor and PO number correct. Check if product is substitute for ordered item. Contact purchasing before receiving. May need to reject if not approved.

**Issue:** Quantity significantly different than ordered
* **Solution:** Verify your count is correct. Check if vendor partially shipped. Review PO terms (some allow +/- 10%). Document and contact vendor. Don't receive without resolution.

**Issue:** Inventory not updating after receipt
* **Solution:** Verify shipment was completed/finalized. Check that receiving was posted to correct warehouse. Ensure products on shipment match PO products exactly. May need IT support if technical issue.

**Issue:** Damaged product - driver won't note on BOL
* **Solution:** Take detailed photos. Note damage on your copy of BOL. Sign driver's copy but add your own notes. May file freight claim later. Document time and details.

**Where to Get Help:**
* See [Shipments documentation](../../Product/Shipments.md)
* See [Purchase Orders documentation](../../Product/PurchaseOrders.md)
* Contact warehouse manager for receiving questions
* Contact purchasing about vendor or PO issues
* Contact safety coordinator for hazmat concerns

## Related Workflows

**Upstream Processes:**
* [Purchase Order Management](PurchaseOrders.md) - PO must exist first

**Downstream Processes:**
* [Inventory Management](InventoryManagement.md) - Receiving updates inventory
* [Product Blending](ProductBlending.md) - Received materials used for blending
* Accounts payable - invoice matching and payment

**Related Documentation:**
* [Product Management Overview](../../Product/Index.md)
* [Warehouses](../../Product/Warehouses.md)

