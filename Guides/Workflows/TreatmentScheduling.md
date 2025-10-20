# Treatment Scheduling

## Overview

Treatment scheduling determines when well locations should be treated based on configured frequencies, last treatment dates, and route configurations. This workflow is used by schedulers and operations coordinators to plan treatments, optimize timing, handle exceptions, and approve schedules for field execution. Effective scheduling ensures customers receive consistent chemical treatments while maximizing field efficiency.

## Prerequisites

**Required Permission:** `Pages.Scheduler`

**Required Setup:**
* Treatment routes must be configured and active
* Locations must have treatment frequencies set
* Field personnel assigned to routes
* Calendar dates and blackout periods configured

**Related Prerequisites:**
* [Treatment Route Setup](TreatmentRoutes.md) must be completed first

## Workflow Diagram

```
View Treatment Schedule → Identify Due/Overdue Locations → Review Route Schedules
       ↓
Adjust Timing for Exceptions → Optimize Daily Schedules → Generate Delivery Orders
       ↓
Submit for Approval (if required) → Approve Schedules → Dispatch to Field
```

## Step-by-Step Procedure

### Viewing and Planning Treatments

1. **Navigate to Order Scheduling**
   * Go to main menu → Distribution → Order Scheduling
   * View shows treatment schedules by date range

2. **Select Date Range**
   * Choose week, month, or custom date range
   * System displays locations due for treatment in that period
   * Color coding shows: Due, Overdue, Scheduled, Completed

3. **Review Locations Due for Treatment**
   * System calculates based on last treatment date + frequency
   * Filter by route, customer, area, or product
   * Review overdue treatments first (highlighted in red)
   * Check upcoming treatments for next 7-14 days

### Planning and Optimizing Schedules

4. **Group by Route**
   * View treatments organized by treatment route
   * See which routes are due to run on which days
   * Verify route frequency matches schedule (daily, weekly, etc.)

5. **Adjust for Exceptions**
   * **Locations with access issues:** Defer or reschedule
   * **Weather delays:** Push schedule out if roads impassable
   * **Customer requests:** Adjust timing per customer needs
   * **Personnel availability:** Adjust if assigned tech is unavailable
   * Document exception reason

6. **Balance Daily Workload**
   * Review estimated time for each day's treatments
   * Avoid overloading field personnel (typically 6-10 locations/day)
   * Move treatments between days if needed
   * Consider drive time and geographic clustering

### Generating and Approving Schedules

7. **Generate Delivery Orders from Schedule**
   * Select treatments ready to schedule
   * Click "Generate Delivery Orders"
   * System creates delivery orders for selected treatments
   * Orders are created in "Scheduled" status

8. **Review Generated Orders**
   * Verify products and quantities are correct
   * Check assignments (route, personnel, vehicle)
   * Confirm scheduled dates
   * Make adjustments if needed

9. **Submit for Approval** (if workflow requires)
   * Click "Submit for Approval"
   * Route goes to supervisor or operations manager
   * See [Treatment Approvals](TreatmentScheduling.md) process
   * Cannot dispatch until approved

10. **Approve Schedule** (for approvers)
    * Review submitted schedules
    * Verify workload is reasonable
    * Check for conflicts or issues
    * Approve or return for revision

### Handling Ongoing Scheduling

11. **Monitor Schedule Execution**
    * Track which treatments are completed
    * Follow up on incomplete or exception treatments
    * Reschedule missed treatments

12. **Adjust for Changes**
    * Handle emergency treatments (add to schedule)
    * Remove treatments for shut-in wells
    * Adjust for customer cancellations
    * Rebalance as needed

## Best Practices

### For Schedulers
* **Plan 1-2 weeks ahead** to allow time for adjustments and approvals
* **Review Monday mornings** - Finalize the week's schedules on Monday AM
* **Check overdue list daily** - Address overdue treatments promptly to avoid customer issues
* **Consider drive time** - Don't just count locations, factor actual drive time between sites

### For Operations Coordinators
* **Communicate proactively** - Notify customers of schedule changes
* **Buffer for weather** - In winter/rainy seasons, add flexibility to schedules
* **Track completion rates** - Monitor on-time completion percentage and improve
* **Optimize continuously** - Review routes monthly for efficiency improvements

### Industry-Specific Tips
* **Production schedules:** Coordinate with operator production activities (well testing, maintenance)
* **Freeze protection:** In winter, prioritize freeze protection chemical treatments
* **Regulatory timing:** Some treatments must occur within specific timeframes for compliance
* **Tank levels:** Consider customer tank levels when scheduling - don't overfill
* **Road conditions:** Check lease road status, especially after heavy rain

## Troubleshooting

**Issue:** Location shows as due but was recently treated
* **Solution:** Verify the last treatment was properly recorded and marked complete. Check that the treatment date is correct in the system. May need to manually update last treatment date.

**Issue:** Treatment schedule not auto-generating
* **Solution:** Check that treatment route is "Active" status. Verify frequency settings on locations. Ensure scheduling automation is enabled in system configuration.

**Issue:** Too many locations showing as overdue
* **Solution:** This may indicate route frequencies need adjustment or insufficient field capacity. Review actual completion rates and adjust route configurations or add personnel.

**Issue:** Cannot generate delivery order from scheduled treatment
* **Solution:** Verify that a valid sales order exists for the location. Check that products are configured. Ensure location is active and assigned to customer.

**Issue:** Field personnel not seeing scheduled treatments
* **Solution:** Verify delivery orders are in "Dispatched" status, not just "Scheduled." Check personnel assignment. Ensure mobile sync is working.

**Where to Get Help:**
* See [Order Scheduling documentation](../../Distribution/OrderScheduling.md)
* See [Treatment Schedules documentation](../../Distribution/Index.md)
* Contact operations supervisor for scheduling questions
* Contact field personnel for feedback on workload and timing

## Related Workflows

**Upstream Processes:**
* [Treatment Route Setup](TreatmentRoutes.md) - Routes must be configured first
* [Sales Order Creation](SalesOrders.md) - Sales orders drive treatment authorization

**Downstream Processes:**
* [Delivery Order Management](DeliveryOrders.md) - Schedules create delivery orders
* [Field Treatment Execution](FieldTreatments.md) - Field staff execute scheduled treatments
* [Treatment Tracking and Monitoring](TreatmentTracking.md) - Monitor schedule execution

**Related Documentation:**
* [Distribution Overview](../../Distribution/Index.md)
* [Calendar](../../Calendar/Index.md) - Calendar view of schedules

