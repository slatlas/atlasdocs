# Delivery Order Management

## Overview

Delivery orders represent scheduled deliveries of chemical products to customer well locations. This workflow is used by dispatchers and operations coordinators to generate delivery orders from sales orders, schedule delivery timing, assign orders to routes and vehicles, and dispatch to field personnel. Delivery orders track the execution status from creation through completion in the field.

## Prerequisites

**Required Permission:** `Pages.DeliveryOrders`

**Required Setup:**
* Active sales orders must exist
* Treatment routes should be configured (for routed deliveries)
* Vehicles and field personnel must be set up in the system
* Well locations must have GPS coordinates for routing

**Related Prerequisites:**
* Complete [Sales Order Creation](SalesOrders.md) first
* Complete [Treatment Route Setup](TreatmentRoutes.md) for routed operations

## Workflow Diagram

```
Active Sales Order → Generate Delivery Order → Schedule Date/Time → Assign to Route/Vehicle
       ↓
Assign Field Personnel → Dispatch to Mobile → Field Execution → Mark Complete
       ↓
Ready for Billing → Invoice Generation
```

## Step-by-Step Procedure

### Generating Delivery Orders

1. **Navigate to Delivery Orders Dashboard**
   * Go to main menu → Distribution → Delivery Orders
   * The dashboard shows all delivery orders by status

2. **Generate from Sales Orders**
   * Click "Create from Sales Orders" or similar button
   * System displays active sales orders ready for delivery
   * Select one or more sales orders to convert
   * Click "Generate Delivery Orders"
   * System creates delivery orders with products/quantities from sales orders

### Scheduling and Assigning Delivery Orders

3. **Set Delivery Date and Time**
   * Open the delivery order
   * Set "Scheduled Delivery Date"
   * Enter time window if specific timing is required
   * Consider customer availability and access restrictions

4. **Assign to Route (if using route-based delivery)**
   * Select the treatment route this delivery belongs to
   * System may auto-assign based on location and route configuration
   * Delivery order will appear in route sequence

5. **Assign Vehicle**
   * Select the service vehicle/truck for this delivery
   * System tracks vehicle inventory and capacity
   * Ensure vehicle has sufficient product loaded

6. **Assign Field Personnel**
   * Select the technician or pumper responsible
   * Can assign primary and backup personnel
   * Personnel will see assigned orders in their mobile app

### Dispatching to the Field

7. **Review Order Details**
   * Verify products, quantities, and location are correct
   * Check special instructions are included
   * Confirm authorization/PO information

8. **Change Status to Dispatched**
   * Update order status from "Scheduled" to "Dispatched"
   * This makes the order visible to field personnel on mobile devices
   * Personnel receive notification of dispatch

9. **Monitor Execution**
   * Track order status in real-time using Order Tracker
   * See GPS location of field personnel
   * Monitor completion progress throughout the day

### Handling Order Completion

10. **Receive Completion from Field**
    * Field personnel complete order via mobile app
    * System updates order status to "Completed"
    * Actual quantities used are recorded

11. **Review Completed Orders**
    * Check for exceptions or variances
    * Verify actual vs. planned quantities
    * Review any field notes or issues documented

12. **Handle Order Exceptions**
    * If location was inaccessible, mark order as "Exception"
    * Reschedule or cancel as appropriate
    * Document reason for exception

## Best Practices

### For Dispatchers
* **Batch create delivery orders** at the start of each week based on recurring sales orders and schedules
* **Group by geography** when assigning to routes to minimize drive time
* **Confirm vehicle inventory** before dispatching - ensure products are loaded on the assigned vehicle
* **Set realistic time windows** based on historical data and drive times

### For Operations Coordinators
* **Monitor in real-time** throughout the day to catch and address issues early
* **Communicate proactively** with field personnel about changes or urgent priorities
* **Review completion rates** daily to identify process improvements
* **Plan ahead** for weather, road closures, or access restrictions

### Industry-Specific Tips
* **Lease access:** Verify lease roads are passable, especially after rain or in winter
* **Customer notifications:** Some operators require advance notice before accessing locations
* **Product temperature:** For temperature-sensitive chemicals, avoid extreme weather timing
* **Tank capacity:** Check customer tank levels before delivery to avoid overfilling

## Troubleshooting

**Issue:** Cannot generate delivery order from sales order
* **Solution:** Verify sales order status is "Active" and has not already been fully delivered. Check that sales order has valid products and quantities.

**Issue:** Field personnel cannot see dispatched orders on mobile
* **Solution:** Ensure order status is "Dispatched" not just "Scheduled." Verify personnel is assigned to the order. Check that mobile sync is working.

**Issue:** Order shows as completed but quantities seem wrong
* **Solution:** Review the treatment details recorded in the field. Contact field personnel to verify actual quantities used. Make adjustments if necessary before billing.

**Issue:** Need to change assignment after dispatching
* **Solution:** Open the delivery order, change vehicle/personnel assignment, and save. Field personnel will see updated assignment after next sync.

**Issue:** Order stuck in "In Progress" status
* **Solution:** Field personnel may have started but not completed the order. Contact them to complete or close the order. Can manually update status if necessary.

**Where to Get Help:**
* See [Delivery Orders documentation](../../Distribution/DeliveryOrders.md)
* See [Order Tracker documentation](../../Distribution/OrderTracker.md) for monitoring
* Contact operations supervisor for dispatch questions
* Contact IT support for mobile sync issues

## Related Workflows

**Upstream Processes:**
* [Sales Order Creation](SalesOrders.md) - Source of delivery orders
* [Treatment Scheduling](TreatmentScheduling.md) - Determines when deliveries should occur
* [Treatment Route Setup](TreatmentRoutes.md) - Route configuration for assignments

**Downstream Processes:**
* [Field Treatment Execution](FieldTreatments.md) - How field staff complete the deliveries
* [Treatment Tracking and Monitoring](TreatmentTracking.md) - Real-time monitoring tools
* [Invoicing Process](Invoicing.md) - Billing for completed deliveries

**Related Documentation:**
* [Distribution Overview](../../Distribution/Index.md)
* [Mobile - Delivery Orders](../../Mobile/DeliveryOrders.md)
* [Order Tracker](../../Distribution/OrderTracker.md)

