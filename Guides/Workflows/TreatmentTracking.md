# Treatment Tracking and Monitoring

## Overview

Treatment tracking and monitoring provides real-time visibility into route execution, treatment completion, and field operations. This workflow is used by operations supervisors and managers to monitor active routes, track treatment progress, identify delays or issues, and analyze treatment effectiveness. Real-time GPS tracking and status updates enable proactive management and rapid response to field problems.

## Prerequisites

**Required Permission:** `Pages.OrderTracker`

**Required Setup:**
* Field personnel must have mobile devices with GPS enabled
* Delivery orders must be dispatched
* Routes must be active with treatments in progress

**Related Prerequisites:**
* [Delivery Order Management](DeliveryOrders.md) - Orders must be dispatched
* [Field Treatment Execution](FieldTreatments.md) - Understanding field execution process

## Workflow Diagram

```
Open Tracking Dashboard → View Active Routes/Orders → Monitor GPS Locations → Track Completion Status
       ↓
Identify Delays/Issues → Contact Field Personnel → Resolve Problems → Analyze Performance
       ↓
Review Completed Treatments → Generate Reports → Continuous Improvement
```

## Step-by-Step Procedure

### Monitoring Active Operations

1. **Navigate to Route Tracker**
   * Go to main menu → Distribution → Route Tracker (or Order Tracker)
   * Dashboard displays map view of active operations

2. **View Active Routes and Personnel**
   * Map shows GPS location of field personnel in real-time
   * Different colors/icons indicate different routes or statuses
   * List view shows route details and progress

3. **Monitor Treatment Progress**
   * See which treatments are:
     * Not Started (scheduled)
     * In Progress (currently being performed)
     * Completed (finished)
     * Exception (issues occurred)
   * Progress bars show percentage complete for each route

4. **Check Individual Treatment Status**
   * Click on specific treatment or location
   * View details: arrival time, products used, quantities, notes
   * See estimated completion time
   * Check if on schedule or delayed

### Managing Issues and Exceptions

5. **Identify Delays**
   * System highlights treatments behind schedule (red/yellow indicators)
   * Compare actual progress to planned schedule
   * Look for routes with long gaps between completions

6. **Review Exception Treatments**
   * Click on exception indicators
   * Read field notes about why treatment wasn't completed
   * Reasons may include: location inaccessible, equipment down, wrong product

7. **Contact Field Personnel**
   * Use system messaging or call field tech directly
   * Verify situation and get more details
   * Provide guidance or reroute as needed
   * Send updated instructions through mobile app

8. **Reassign or Reschedule**
   * If treatment can't be completed today, reschedule for later
   * Can reassign to different personnel if needed
   * Update delivery order status and notes
   * Notify customer if significant delay

### Analyzing Performance

9. **Review Daily Completion Rates**
   * Track percentage of scheduled treatments completed
   * Monitor time per treatment (actual vs. estimated)
   * Identify routes consistently over/under time

10. **Analyze Treatment Effectiveness**
    * Review treatment history for locations
    * Track product usage trends
    * Monitor customer feedback and issues
    * Identify locations needing program adjustments

11. **Generate Performance Reports**
    * Export route completion data
    * Create reports by route, personnel, customer, or date range
    * Share with management and operations team
    * Use data for route optimization

### End-of-Day Review

12. **Verify All Treatments Processed**
    * Confirm all completed treatments synced from mobile
    * Check for any orphaned or stuck records
    * Ensure exception treatments are documented

13. **Follow Up on Issues**
    * Schedule followup for missed treatments
    * Contact customers if service was not completed
    * Address any equipment or access problems
    * Plan corrections for next service cycle

## Best Practices

### For Operations Supervisors
* **Monitor proactively** - Check route tracker every 1-2 hours during the day
* **Intervene early** - If route is falling behind, address issues before end of day
* **Track trends** - Look for patterns in delays, exceptions, or problems
* **Communicate clearly** - Keep field personnel informed of expectations and changes

### For Operations Managers
* **Review metrics weekly** - Track completion rates, time per treatment, exception rates
* **Optimize routes** - Use actual data to improve route design and sequences
* **Balance workload** - Adjust route assignments if some personnel consistently run over
* **Address systemic issues** - If certain locations or products cause repeated problems, investigate root causes

### Industry-Specific Tips
* **Weather impact:** Track how weather affects completion rates to improve forecasting
* **Seasonal patterns:** Monitor treatment needs changing with seasons (freeze protection, paraffin, etc.)
* **Production correlation:** Analyze if treatment effectiveness correlates with well production data
* **Customer satisfaction:** Track customer complaints or compliments related to service quality

## Troubleshooting

**Issue:** GPS location not showing or not updating
* **Solution:** Verify field personnel have GPS enabled on mobile device. Check cellular/data connection. GPS may be delayed in remote areas. If continues, have tech restart app or device.

**Issue:** Treatment shows in progress for too long
* **Solution:** Field personnel may have forgotten to complete. Contact them to close out the treatment. May need to manually complete if tech can't access mobile device.

**Issue:** Completed treatments not appearing
* **Solution:** Field personnel may not have synced mobile device. Remind them to sync. Check for mobile sync errors. Data will appear once successfully synced.

**Issue:** Route shows as behind schedule
* **Solution:** Review actual conditions - may need more time due to road conditions, equipment issues, etc. Contact field tech to understand cause. Adjust future estimates if consistently under-estimated.

**Issue:** Exception rate is high
* **Solution:** Investigate root causes. Common issues: access problems, wrong schedules, equipment failures. May need route adjustments, better customer communication, or equipment repairs.

**Where to Get Help:**
* See [Route Tracker documentation](../../Distribution/RouteTracker.md)
* See [Order Tracker documentation](../../Distribution/OrderTracker.md)
* See [Treatments documentation](../../Distribution/Treatments.md)
* Contact IT support for tracking system technical issues
* Contact operations manager for process improvement questions

## Related Workflows

**Upstream Processes:**
* [Treatment Scheduling](TreatmentScheduling.md) - Creates schedules to monitor
* [Delivery Order Management](DeliveryOrders.md) - Dispatches orders to track
* [Treatment Route Setup](TreatmentRoutes.md) - Route configuration affects tracking

**Downstream Processes:**
* [Invoicing Process](Invoicing.md) - Completed treatments feed billing
* Route optimization and improvement
* Performance analysis and reporting

**Related Documentation:**
* [Distribution Overview](../../Distribution/Index.md)
* [Reports](../../Reports/Index.md) - Operational reports
* [Calendar](../../Calendar/Index.md) - Calendar view of activities

