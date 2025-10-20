# Price Schedule Configuration

## Overview

Price schedules define customer-specific pricing for chemical products and services that override standard catalog pricing. This workflow is used by pricing analysts and managers to create customer-specific pricing, set up volume discounts, configure fees and surcharges, and apply schedules to customers or specific locations. Price schedules enable flexible pricing strategies while ensuring accurate billing.

## Prerequisites

**Required Permission:** `Pages.PriceSchedules`

**Required Setup:**
* Products must exist with base pricing
* Customers must be configured
* Locations may be set up for location-specific pricing
* Price schedule calculation types and fee types defined

**Related Prerequisites:**
* [Product Setup](ProductSetup.md) - Products must exist
* [Customer Setup](CustomerSetup.md) - Customer must exist

## Workflow Diagram

```
Determine Pricing Need → Create Price Schedule → Add Products with Prices → Configure Calculation Method
       ↓
Set Effective Dates → Apply Volume Tiers (if applicable) → Add Fees/Surcharges → Assign to Customer/Location
```

## Step-by-Step Procedure

### Creating a Price Schedule

1. **Navigate to Price Schedules**
   * Go to main menu → Product → Price Schedules
   * Click "Create New Price Schedule"

2. **Enter Schedule Information**
   * **Schedule Name:** Descriptive name (e.g., "ABC Energy - 2025 Contract Pricing")
   * **Schedule Code:** Short identifier
   * **Customer:** Select customer this pricing applies to
   * **Effective Date:** When pricing becomes active
   * **Expiration Date:** When pricing ends (or leave open)
   * **Priority:** If multiple schedules could apply, highest priority wins

3. **Select Calculation Type**
   * **Fixed Price:** Set specific price per unit
   * **Cost Plus Percentage:** Base cost + markup %
   * **Volume Discount:** Tiered pricing based on quantity
   * **Formula-Based:** Complex calculation
   * Choose method that matches customer agreement

### Adding Products to Price Schedule

4. **Add Products**
   * Click "Add Product" or "Add Line"
   * Select product from catalog
   * Repeat for all products in this pricing agreement

5. **Set Product Pricing** (for each product)
   * **Base Price:** Price per unit
   * **Unit of Measure:** Gallon, quart, drum, etc.
   * **Minimum Quantity:** Order minimums if applicable
   * **Maximum Quantity:** Order limits if applicable

### Configuring Volume-Based Pricing (if applicable)

6. **Set Up Price Tiers**
   * Click "Add Tier" for volume-based pricing
   * **Tier 1:** 0-100 gallons @ $10/gallon
   * **Tier 2:** 101-500 gallons @ $9/gallon
   * **Tier 3:** 501+ gallons @ $8/gallon
   * System automatically applies correct tier based on quantity

7. **Configure Tier Calculation**
   * **Tiered:** Each unit priced at its tier rate
   * **All Units:** Once threshold met, all units at lower price
   * Choose method per customer agreement

### Adding Fees and Surcharges

8. **Configure Fees**
   * Click "Add Fee"
   * **Fee Type:** Delivery fee, environmental fee, fuel surcharge, etc.
   * **Calculation Method:**
     * Fixed amount per order
     * Percentage of order value
     * Per unit/gallon
     * Distance-based (for delivery fees)
   * **Amount:** Dollar amount or percentage

9. **Set Fee Conditions**
   * **Apply When:** Always, above threshold, specific products, etc.
   * **Maximum Fee:** Cap if applicable
   * **Minimum Fee:** Floor if applicable

### Applying the Price Schedule

10. **Assign to Customer**
    * Price schedule automatically applies to assigned customer
    * All orders for this customer use this pricing
    * Effective during the specified date range

11. **Assign to Specific Locations** (optional)
    * Can apply schedule only to certain locations
    * Click "Add Locations"
    * Select specific well locations
    * Location-specific pricing overrides customer-level pricing

12. **Assign to Leases** (optional)
    * Can apply to all locations on specific leases
    * Select leases from list
    * All locations on those leases use this pricing

### Finalizing and Testing

13. **Review Price Schedule**
    * Verify all products included
    * Check pricing is correct per agreement
    * Confirm fees are configured properly
    * Verify effective dates

14. **Activate Price Schedule**
    * Status changes to "Active"
    * System begins applying pricing to new orders
    * Effective date must have passed for pricing to apply

15. **Test Pricing**
    * Create test sales order for customer
    * Verify correct pricing applies
    * Check that volume discounts calculate correctly
    * Test fees and surcharges
    * Delete test order after verification

## Best Practices

### For Pricing Analysts
* **Document agreements** - Keep copy of customer pricing agreement with schedule
* **Effective dates** - Set up new schedules before old ones expire to avoid gaps
* **Version control** - Name schedules with version or year for tracking
* **Test thoroughly** - Always test before going live

### For Managers
* **Approval workflow** - Require management approval for price schedule changes
* **Competitive intelligence** - Track competitor pricing and market rates
* **Margin analysis** - Ensure pricing maintains acceptable margins
* **Contract alignment** - Ensure schedules match signed agreements exactly

### Industry-Specific Tips
* **Contract pricing:** Many oil and gas operators negotiate annual contracts
* **Cost recovery:** Some agreements are cost-plus with documentation requirements
* **Volume commitments:** Discounts often tied to minimum volume commitments
* **Index-based pricing:** Some contracts tie pricing to commodity indices
* **Geographic differentials:** Pricing may vary by field or region due to logistics costs
* **Product bundling:** Discounts for purchasing multiple products together

## Troubleshooting

**Issue:** Price schedule not applying to sales order
* **Solution:** Verify schedule is "Active" status. Check that current date is within effective date range. Ensure schedule is assigned to this customer. Verify priority if multiple schedules could apply.

**Issue:** Wrong pricing applied - not using price schedule
* **Solution:** Check that price schedule includes this specific product. Verify customer is correctly assigned to schedule. If location-specific, confirm order is for that location. Check effective dates.

**Issue:** Volume discount not calculating correctly
* **Solution:** Review tier configuration and calculation method. Verify quantity on order meets tier threshold. Check if "All Units" vs "Tiered" setting is correct per agreement.

**Issue:** Fee not appearing on invoice
* **Solution:** Verify fee is active and configured. Check fee conditions - may only apply in certain situations. Confirm fee calculation method is correct. Review if fee was manually removed from order.

**Issue:** Need to update pricing mid-contract
* **Solution:** Create new version of price schedule with new effective date. Keep old schedule active until new date. Or modify existing schedule if agreement allows mid-term changes. Document approval for audit.

**Where to Get Help:**
* See [Price Schedules documentation](../../Product/PriceSchedules.md)
* See [Sales Orders documentation](../../Distribution/SalesOrders.md)
* Contact pricing manager for approval questions
* Contact account manager for customer agreement interpretation
* Contact accounting for margin and cost questions

## Related Workflows

**Upstream Processes:**
* [Customer Setup](CustomerSetup.md) - Customer must exist
* [Product Setup](ProductSetup.md) - Products must be configured
* Contract negotiation (outside system)

**Downstream Processes:**
* [Sales Order Creation](SalesOrders.md) - Pricing applied to orders
* [Invoicing Process](Invoicing.md) - Pricing flows to invoices
* Margin analysis and reporting

**Related Documentation:**
* [Product Management Overview](../../Product/Index.md)
* [Distribution Overview](../../Distribution/Index.md)
* [Billing Overview](../../Billing/Index.md)

