# Sales Order Creation

## Overview

Sales orders document customer purchases of chemical products and services for delivery to well locations. This workflow is used by sales staff and customer service representatives to create orders for products and services. Sales orders are the starting point for the order-to-cash process and drive delivery scheduling and invoicing. Note: Sales orders themselves are one-time orders; recurring service is managed through treatment schedules configured on locations.

## Prerequisites

**Required Permission:** `Pages.SalesOrders`

**Required Setup:**
* Customer account must exist in the system
* Products must be configured in the product catalog
* Price schedules should be established for the customer (if using custom pricing)
* Well locations should be set up and linked to the customer

**Related Prerequisites:**
* Complete [Customer Setup](CustomerSetup.md) first
* Complete [Product Setup](ProductSetup.md) first

## Workflow Diagram

```
Customer Request → Create Sales Order → Add Products → Configure Pricing/Quantities
       ↓
Set Delivery Location → Review & Save → Activate Sales Order
       ↓
Generate Delivery Orders (from Sales Order + Treatment Schedules)
```

## Step-by-Step Procedure

### Creating a New Sales Order

1. **Navigate to Sales Orders**
   * Go to main menu → Distribution → Sales Orders
   * Click "Create New" or "Add Sales Order"

2. **Select Customer and Project**
   * Choose the customer from the dropdown
   * Select associated customer project (if applicable)
   * Select the lease or location for delivery

3. **Add Products to the Order**
   * Click "Add Product" or "Add Line Item"
   * Select the chemical product from the catalog
   * Enter quantity and unit of measure
   * System will apply pricing based on customer's price schedule
   * Override pricing if needed (requires appropriate permissions)
   * Add multiple products as needed

4. **Configure Order Details**
   * **Order Type:** Select standard or contract-based
   * **Service Type:** Choose treatment type or delivery service
   * **Authorization:** Enter customer PO number or authorization code
   * **Special Instructions:** Add any delivery or product application notes
   * **Note:** For ongoing treatment services, the sales order authorizes service, while treatment schedules (configured on locations) control when treatments occur

5. **Review and Validate**
   * Check that all products are correct
   * Verify pricing matches customer agreement
   * Confirm delivery location is accurate
   * Review total order value

6. **Save the Sales Order**
   * Click "Save" to create the order
   * Order status will be set to "Active" or "Pending Approval" based on your workflow
   * Note the sales order number for reference

### Generating Delivery Orders from Sales Orders

7. **Create Delivery Orders** (if not automated)
   * From the sales order, click "Create Delivery Order"
   * OR navigate to Delivery Orders and generate from active sales orders
   * See [Delivery Order Management](DeliveryOrders.md) for details

## Best Practices

### For Sales Staff
* **Always verify pricing** before finalizing the order, especially for new customers or special pricing arrangements
* **Link to the correct location** - Confirm the specific well location, not just the lease or customer
* **Document authorization** - Always enter the customer PO number or verbal authorization details
* **Set up treatment schedules** - For ongoing treatment services, ensure treatment schedules are configured on the locations (see Treatment Route Setup)

### For Customer Service
* **Check inventory availability** before promising delivery dates, especially for bulk orders
* **Clarify treatment frequencies** with customers upfront - these are configured in treatment schedules on locations
* **Note special instructions** clearly - field technicians rely on these for proper product application

### Industry-Specific Tips
* **Chemical compatibility:** When adding multiple products, ensure they are compatible for the same location/system
* **Seasonal adjustments:** Consider seasonal treatment needs (e.g., increased corrosion inhibitor in winter)
* **Regulatory compliance:** Ensure products are approved for use in the specific jurisdiction

## Troubleshooting

**Issue:** Product pricing doesn't match customer agreement
* **Solution:** Check that the correct price schedule is assigned to the customer. Navigate to Price Schedules to verify or create customer-specific pricing.

**Issue:** Cannot select desired location
* **Solution:** Verify the location is active and linked to the customer. Check Location Management to update customer/location relationships.

**Issue:** Treatments not generating automatically
* **Solution:** Sales orders don't generate treatments automatically. Treatments are generated from treatment schedules configured on locations. See Treatment Scheduling workflow. Ensure the location has a treatment schedule and treatment route assigned.

**Issue:** Need to modify an existing sales order
* **Solution:** Open the sales order, make changes, and save. If delivery orders have already been generated, you may need to adjust those separately.

**Where to Get Help:**
* See [Sales Orders documentation](../../Distribution/SalesOrders.md) for detailed feature information
* Contact your supervisor for pricing approval issues
* Contact IT support for system access or technical problems

## Related Workflows

**Upstream Processes:**
* [Customer Setup](CustomerSetup.md) - Must have customer account before creating orders
* [Product Setup](ProductSetup.md) - Products must exist in catalog
* [Price Schedule Configuration](PriceSchedules.md) - Set up customer pricing

**Downstream Processes:**
* [Delivery Order Management](DeliveryOrders.md) - Next step: schedule and dispatch deliveries
* [Field Treatment Execution](FieldTreatments.md) - How field staff execute the orders
* [Invoicing Process](Invoicing.md) - Final step: bill the customer for completed work

**Related Documentation:**
* [Distribution Overview](../../Distribution/Index.md)
* [Billing Overview](../../Billing/Index.md)

