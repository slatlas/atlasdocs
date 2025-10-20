# Product Setup and Management

## Overview

Product setup creates and maintains the catalog of chemical products, equipment, and services that can be sold, delivered, and tracked in Atlas. This workflow is used by product managers and administrators to add new products, configure specifications, set categories and types, and establish base pricing. A well-maintained product catalog ensures accurate ordering, inventory tracking, and billing.

## Prerequisites

**Required Permission:** `Pages.Products`

**Required Setup:**
* Product categories should be defined
* Product types should be configured
* Units of measure available
* Tax codes configured if needed

## Workflow Diagram

```
Identify Product Need → Create Product → Configure Specifications → Set Classification
       ↓
Establish Pricing → Configure Inventory Settings → Set Billing Rules → Activate Product
```

## Step-by-Step Procedure

### Creating a New Product

1. **Navigate to Products**
   * Go to main menu → Product → Products
   * Click "Create New Product"

2. **Enter Basic Information**
   * **Product Name:** Full product name (e.g., "Corrosion Inhibitor CI-100")
   * **Product Code/SKU:** Short identifier for ordering
   * **Description:** Detailed description of product and use
   * **Manufacturer:** Producer of the chemical
   * **Status:** Active, Inactive, Discontinued

3. **Classify the Product**
   * **Product Category:** Chemicals, Equipment, Services, Supplies
   * **Product Type:** Corrosion Inhibitor, Scale Inhibitor, Biocide, Pump, etc.
   * **Treatment Type:** What problem does it address
   * Category and type help organize products and reporting

### Configuring Product Specifications

4. **Set Units of Measure**
   * **Primary UOM:** How product is sold (gallons, quarts, drums, each)
   * **Secondary UOM:** Alternate units if applicable
   * **Conversion Factor:** If multiple units (e.g., 55 gallons per drum)

5. **Enter Product Specifications**
   * **Chemical Composition:** Active ingredients, concentration
   * **Specific Gravity:** For volume/weight conversions
   * **Flash Point:** Safety information
   * **pH Level:** Chemical properties
   * **Color/Appearance:** For identification
   * **Shelf Life:** Expiration considerations

6. **Add Safety and Regulatory Information**
   * **Hazmat Classification:** DOT class if hazardous
   * **UN Number:** For shipping hazardous materials
   * **Safety Data Sheet (SDS):** Upload or link to SDS
   * **EPA Registration:** If pesticide/biocide
   * **Special Handling Requirements:** Storage, PPE needs

### Setting Pricing

7. **Establish Base Pricing**
   * **Standard Cost:** What you pay for product
   * **Standard Price:** What you charge customers (base price)
   * **Currency:** USD typically
   * **Price UOM:** Unit that price is per (e.g., per gallon)

8. **Configure Price Rules**
   * **Allow Discounts:** Yes/No - can price be discounted
   * **Minimum Price:** Floor price if discounting allowed
   * **Price Override Permission:** Who can change pricing on orders

### Configuring Inventory Settings

9. **Set Inventory Tracking**
   * **Track Inventory:** Yes/No - is this a stocked item
   * **Inventory UOM:** Unit inventory is counted in
   * **Default Warehouse:** Primary storage location
   * **Bin Location:** Specific location within warehouse

10. **Set Reorder Parameters** (if tracked)
    * **Reorder Point:** Quantity that triggers reorder alert
    * **Reorder Quantity:** How much to order when low
    * **Safety Stock:** Minimum quantity to maintain
    * **Lead Time:** Days from order to receipt

11. **Configure Inventory Valuation**
    * **Costing Method:** FIFO, LIFO, Average Cost, Standard Cost
    * **Standard Cost:** For standard cost method

### Configuring Billing and Usage

12. **Set Billing Rules**
    * **Billable:** Yes/No - does this generate charges
    * **Tax Code:** Default sales tax treatment
    * **Revenue Account:** GL account code for accounting
    * **COGS Account:** Cost of goods sold account

13. **Configure Usage Tracking**
    * **Track by Serial Number:** For equipment
    * **Track by Lot Number:** For batch-controlled chemicals
    * **Expiration Date Tracking:** For perishable products
    * **Required in Field App:** Must field personnel select this product

### Finalizing Product Setup

14. **Add Product Images and Documents**
    * Upload product photo
    * Attach technical data sheets
    * Link to SDS document
    * Add application guides

15. **Enter Additional Information**
   * **Vendor:** Primary supplier
   * **Vendor Part Number:** Supplier's SKU
   * **Notes:** Any special handling or usage notes
   * **Substitute Products:** Alternative products if not available

16. **Review and Save**
    * Verify all information is correct
    * Check pricing and costs
    * Confirm classification
    * Click "Save"

17. **Activate Product**
    * Set status to "Active"
    * Product now available for sales orders
    * Appears in product searches and dropdowns

## Best Practices

### For Product Managers
* **Consistent naming** - Use standard naming conventions for product codes
* **Complete specs** - Full specifications help field staff and customers
* **Maintain SDS** - Keep safety data sheets current and accessible
* **Regular review** - Audit product catalog quarterly to inactivate obsolete items

### For Administrators
* **Categories matter** - Proper classification improves reporting
* **Pricing accuracy** - Verify costs and prices are current
* **Inventory settings** - Don't track inventory for services or non-stocked items
* **Test before launch** - Create test order before releasing new product

### Industry-Specific Tips
* **Generic vs. branded:** Clarify if product name is brand name or generic chemical
* **Concentration:** Always specify concentration (e.g., "30% Methanol")
* **Application rate:** Note typical dosage rates in description
* **Compatibility:** Document which products can/cannot be mixed
* **Environmental:** Note if biodegradable, phosphate-free, etc.
* **Temperature range:** Specify operating temperature limits
* **Blend components:** Mark products used in blending separately

## Troubleshooting

**Issue:** Product not appearing in sales order dropdown
* **Solution:** Verify status is "Active." Check that product category allows sales. Ensure you have permissions for this product. May be filtered out by product type.

**Issue:** Inventory not tracking for product
* **Solution:** Verify "Track Inventory" setting is enabled. Check that inventory UOM is set. Ensure product has been received into at least one warehouse.

**Issue:** Wrong price appearing on orders
* **Solution:** Check product base price. Verify customer doesn't have price schedule overriding. Confirm correct UOM selected - price may be per different unit.

**Issue:** Cannot find product when searching
* **Solution:** Try searching by code instead of name. Check spelling. Verify product is active. May need to search in inactive products if was discontinued.

**Issue:** Need to change product cost
* **Solution:** Update standard cost in product master. If using average costing, cost updates automatically with receipts. Consider if price should change with cost.

**Where to Get Help:**
* See [Products documentation](../../Product/Products.md)
* See [Product Inventory documentation](../../Product/ProductInventory.md)
* Contact product manager for specifications or classification
* Contact purchasing for cost information
* Contact regulatory/safety for hazmat questions

## Related Workflows

**Upstream Processes:**
* Vendor selection and negotiation
* Product testing and approval
* Regulatory registration

**Downstream Processes:**
* [Sales Order Creation](SalesOrders.md) - Products used on orders
* [Purchase Order Management](PurchaseOrders.md) - Ordering products
* [Inventory Management](InventoryManagement.md) - Tracking product stock
* [Product Blending](ProductBlending.md) - Using products as blend components
* [Price Schedule Configuration](PriceSchedules.md) - Customer-specific pricing

**Related Documentation:**
* [Product Management Overview](../../Product/Index.md)
* [Product Lookups](../../Product/Lookups.md)

