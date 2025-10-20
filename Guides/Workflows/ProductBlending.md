# Product Blending

## Overview

Product blending creates custom chemical formulations by mixing component products according to specific recipes or ratios. This workflow is used by blending operators and production staff to record blend batch creation, track component products consumed, generate finished product inventory, and request quality control testing. Proper batch tracking ensures product quality, inventory accuracy, and regulatory compliance.

## Prerequisites

**Required Permission:** `Pages.ProductBlendBatchs`

**Required Setup:**
* Component products must exist in catalog
* Finished blend product must be configured
* Warehouse for blending operations set up
* Blend formulas/recipes may be predefined
* Lab QC fields configured if testing required

**Related Prerequisites:**
* [Product Setup](ProductSetup.md) - All products must exist
* [Inventory Management](InventoryManagement.md) - Component inventory available

## Workflow Diagram

```
Select Blend Formula → Create Batch Record → Add Component Products → Enter Quantities
       ↓
Calculate Yield → Consume Component Inventory → Generate Finished Product → Request QC Testing
       ↓
Approve Batch → Update Inventory → Generate Documentation
```

## Step-by-Step Procedure

### Creating a Blend Batch

1. **Navigate to Product Blend Batches**
   * Go to main menu → Product → Product Blend Batches
   * Click "Create New Blend Batch"

2. **Enter Batch Information**
   * **Finished Product:** Select the blended product being made
   * **Batch Number:** Unique batch identifier (may auto-generate)
   * **Blend Date:** Date of blending operation
   * **Warehouse:** Where blending is performed
   * **Operator:** Person performing the blend
   * **Target Quantity:** Planned amount to produce

3. **Select Blend Formula** (if predefined)
   * Choose from saved formulas for this product
   * System pre-populates component products and ratios
   * Or manually enter components if custom blend

### Adding Component Products

4. **Add Component Products**
   * Click "Add Component"
   * Select component product from inventory
   * Enter quantity used
   * Select unit of measure
   * Repeat for all components in the blend

5. **Verify Component Availability**
   * System checks warehouse inventory for components
   * Red indicator if insufficient inventory
   * May need to receive more inventory before blending
   * See [Inventory Management](InventoryManagement.md)

6. **Record Blend Ratios**
   * Document ratio or percentage of each component
   * Example: 70% Product A, 20% Product B, 10% Product C
   * Helps validate formula and troubleshoot quality issues

### Recording Blend Production

7. **Enter Actual Quantities Consumed**
   * Record actual amount of each component used
   * May differ slightly from planned amounts
   * System tracks variances

8. **Calculate Batch Yield**
   * **Theoretical Yield:** Sum of component quantities
   * **Actual Yield:** Actual amount of finished product produced
   * **Yield Percentage:** Actual ÷ Theoretical × 100%
   * Yield loss may occur due to mixing, spillage, sampling

9. **Enter Finished Product Quantity**
   * Record actual amount of blended product produced
   * Select unit of measure (gallons, pounds, drums)
   * This quantity will be added to finished goods inventory

10. **Record Lot/Batch Numbers**
    * Finished product batch number
    * Component lot numbers (for traceability)
    * Container numbers if filling drums/totes
    * Expiration date if applicable

### Quality Control

11. **Request Quality Control Testing** (if required)
    * Click "Create QC Request"
    * Select tests to perform
    * Retain sample from batch
    * See [Lab QC Requests](../../Product/LabQCRequests.md)
    * Batch may need QC approval before release

12. **Record QC Results** (when received)
    * Enter test results
    * **Pass/Fail:** Does batch meet specifications
    * **Approval:** QC staff approves batch for use
    * Failed batches may need rework or disposal

13. **Document Blend Details**
    * Blending time and temperature if relevant
    * Mixing speed and duration
    * Equipment used
    * Any issues or deviations from standard process

### Completing the Batch

14. **Review Batch Record**
    * Verify all components are recorded
    * Check that quantities are accurate
    * Confirm QC testing complete (if required)
    * Review yield calculation

15. **Finalize Batch**
    * Click "Complete" or "Finalize"
    * **Component inventory depletes** - system removes component quantities from warehouse inventory
    * **Finished goods inventory increases** - adds finished product to inventory
    * Batch status changes to "Completed"

16. **Generate Batch Documentation**
    * Print batch record for file
    * Generate certificate of analysis if customer-facing
    * Export data for regulatory compliance
    * Attach to quality records

## Best Practices

### For Blending Operators
* **Measure carefully** - Accurate quantities ensure consistent product quality
* **Follow formula exactly** - Deviations affect performance and can create safety issues
* **Clean equipment between batches** - Prevent cross-contamination
* **Label immediately** - Mark containers with batch number, date, product name
* **Document issues** - Note any problems, deviations, or unusual observations

### For Production Staff
* **Verify ingredients** - Ensure components are correct products before adding
* **Check compatibility** - Some chemicals cannot be mixed safely
* **Safety first** - Use appropriate PPE, ventilation, and safety equipment
* **Sample retention** - Keep sample from each batch for future testing or reference
* **First In, First Out:** Use oldest components first to minimize waste from expiration

### Industry-Specific Tips
* **Hazmat considerations:** Blending may create new hazmat classification
* **Temperature control:** Some blends are exothermic or require specific temperatures
* **Mixing order:** Order of addition matters for some formulations
* **Stability testing:** Monitor blends for separation, precipitation, or degradation
* **Customer approval:** Some customers require approval of blend formula
* **Regulatory compliance:** Maintain batch records for EPA, DOT, or other agencies
* **Shelf life:** Blends may have shorter shelf life than components

## Troubleshooting

**Issue:** Insufficient component inventory to blend
* **Solution:** Check inventory levels before starting. Create purchase order for needed components. May need to adjust batch size to match available inventory. See [Purchase Order Management](PurchaseOrders.md).

**Issue:** Yield percentage is very low
* **Solution:** Investigate potential causes: spillage, inaccurate measurements, evaporation, equipment retention, sampling. Review blending process. May need equipment calibration or process improvement.

**Issue:** QC test failed - batch does not meet specifications
* **Solution:** Review component products - verify correct items used. Check measurements and ratios. Determine if batch can be reworked (add more of deficient component). May need to dispose or downgrade if cannot fix.

**Issue:** Inventory not updating after batch completion
* **Solution:** Verify batch status is "Completed" not "Draft." Check that warehouse is correctly specified. Ensure component products have inventory tracking enabled. May need IT support if technical issue.

**Issue:** Need to reverse a completed batch
* **Solution:** If batch needs to be undone (wrong formula, failed QC, etc.), may need to create reversing adjustment. Manually adjust inventory for components and finished product. Document reason. May require supervisor approval.

**Where to Get Help:**
* See [Product Blend Batches documentation](../../Product/ProductBlendBatchs.md)
* See [Lab QC Requests documentation](../../Product/LabQCRequests.md)
* See also [Blends Documentation](../../Blends/Index.md)
* Contact production supervisor for formula or process questions
* Contact QC department for testing and specifications
* Contact safety coordinator for hazmat or safety concerns

## Related Workflows

**Upstream Processes:**
* [Product Setup](ProductSetup.md) - Component and finished products must exist
* [Inventory Management](InventoryManagement.md) - Component inventory must be available
* [Purchase Order Management](PurchaseOrders.md) - Ordering components

**Downstream Processes:**
* Quality control testing
* [Inventory Management](InventoryManagement.md) - Finished product inventory
* [Sales Order Creation](SalesOrders.md) - Selling the blended product
* Regulatory reporting and compliance

**Related Documentation:**
* [Product Management Overview](../../Product/Index.md)
* [Inventory](../../Product/ProductInventory.md)

