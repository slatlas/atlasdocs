# Treatment Route Setup

## Overview

Treatment routes organize customer well locations into logical sequences for efficient chemical treatment delivery. This workflow is used by operations managers and route planners to create routes, add locations in optimized order, set treatment frequencies, and assign products and personnel. Well-configured routes minimize drive time, ensure consistent service, and improve field productivity.

## Prerequisites

**Required Permission:** `Pages.TreatmentRoutes.Create`

**Required Setup:**
* Well locations must be configured with GPS coordinates
* Products for treatment must be in the system
* Field personnel must be set up
* Vehicles/service trucks should be configured
* Treatment types and frequencies should be defined

**Related Prerequisites:**
* [Location Management](LocationSetup.md) - Locations must exist first
* [Customer Setup](CustomerSetup.md) - Customers must be established

## Workflow Diagram

```
Identify Service Area → Create Route → Name and Configure Route → Add Locations
       ↓
Optimize Sequence → Assign Products → Set Treatment Frequencies → Assign Personnel/Vehicle
       ↓
Activate Route → Generate Treatment Schedules → Monitor Performance
```

## Step-by-Step Procedure

### Creating a New Treatment Route

1. **Navigate to Treatment Routes**
   * Go to main menu → Distribution → Treatment Routes
   * Click "Create New Route"

2. **Configure Basic Route Information**
   * **Route Name:** Give descriptive name (e.g., "North Field Daily Route" or "Smith Lease Weekly")
   * **Route Code:** Short identifier for reporting
   * **Route Type:** Daily, Weekly, Bi-Weekly, Monthly, or As-Needed
   * **Description:** Add notes about the route purpose or coverage area

3. **Set Route Schedule**
   * Select days of week route runs (Mon, Tue, Wed, etc.)
   * Set preferred start time
   * Estimate total route duration
   * Configure frequency (every week, every other week, etc.)

### Adding Locations to the Route

4. **Add Well Locations**
   * Click "Add Locations" or "Add Stops"
   * Search for locations by name, lease, customer, or area
   * Select multiple locations to add to route
   * Click "Add Selected"

5. **Optimize Location Sequence**
   * Use "Auto-Optimize" to arrange by GPS coordinates for shortest drive
   * Or manually drag and drop locations to reorder
   * Consider factors: road conditions, customer preferences, tank access times
   * View map to visualize the route path

6. **Configure Stop Details**
   * For each location on the route, set:
   * **Treatment Type:** Corrosion inhibitor, scale inhibitor, biocide, etc.
   * **Treatment Frequency:** Every visit, every other visit, etc.
   * **Estimated Time:** How long treatment typically takes
   * **Special Instructions:** Access codes, contact info, specific procedures

### Assigning Products and Resources

7. **Assign Default Products**
   * Set which chemical products are used on this route
   * Specify default dosage or volume per location
   * Products will pre-populate on treatment records
   * Field staff can adjust quantities as needed

8. **Assign Field Personnel**
   * Select primary technician or pumper for the route
   * Optionally assign backup personnel
   * Personnel see their assigned routes in mobile app

9. **Assign Service Vehicle**
   * Select the truck/vehicle typically used
   * System tracks vehicle inventory for the route
   * Helps with load planning and inventory management

### Activating and Managing the Route

10. **Review Route Configuration**
    * Verify all locations are included
    * Check that sequence is logical
    * Confirm products and frequencies are correct
    * Review total estimated time and distance

11. **Activate the Route**
    * Change route status from "Draft" to "Active"
    * Active routes generate scheduled treatments automatically
    * Inactive routes don't appear in scheduling

12. **Submit for Approval** (if required)
    * Some organizations require route approval
    * See [Treatment Approvals](TreatmentScheduling.md) workflow
    * Route can't be used until approved

## Best Practices

### For Operations Managers
* **Group by geography** - Keep routes within a reasonable drive radius (typically 50-75 miles)
* **Balance workload** - Aim for 6-10 locations per route for 8-hour day, depending on drive time
* **Consider access** - Group locations with similar access restrictions (locked gates, operator escort required)
* **Plan for growth** - Leave room on routes for new locations

### For Route Planners
* **Use GPS optimization** as starting point, then fine-tune based on road conditions and local knowledge
* **Coordinate with customers** - Some operators have preferred service windows or days
* **Seasonal adjustments** - May need different routes in winter when some roads are impassable
* **Review regularly** - Optimize routes quarterly as locations are added/removed or production changes

### Industry-Specific Tips
* **Lease access protocols:** Note if operator escort or advance call is required
* **Tank configurations:** Document which tanks to treat and access points
* **Chemical rotation:** Some locations may rotate between different treatment types
* **Production status:** Update routes when wells go down or change status
* **Road conditions:** Note seasonal access issues (washouts, snow, mud)

## Troubleshooting

**Issue:** Auto-optimize creates illogical sequence
* **Solution:** GPS optimization doesn't know about one-way roads, locked gates, or terrain. Use as starting point, then manually adjust based on field knowledge.

**Issue:** Route takes longer than estimated
* **Solution:** Review actual vs. estimated times from completed treatments. Adjust time estimates and possibly split route into two routes.

**Issue:** Location not appearing in search when adding to route
* **Solution:** Verify location is active and has valid GPS coordinates. Check that location isn't already on another route if exclusive assignments are required.

**Issue:** Treatment schedule not generating automatically
* **Solution:** Verify route status is "Active." Check that route frequency and days are configured. Ensure treatment schedule automation is enabled in system settings.

**Issue:** Need to temporarily skip a location
* **Solution:** Don't remove from route. Instead, mark location as "Temporarily Inactive" or use treatment exceptions when scheduling.

**Where to Get Help:**
* See [Treatment Routes documentation](../../Distribution/TreatmentRoutes.md)
* See [Treatment Scheduling documentation](../../Distribution/OrderScheduling.md)
* Contact operations supervisor for route design questions
* Contact field personnel for local knowledge and optimization

## Related Workflows

**Upstream Processes:**
* [Location Management](LocationSetup.md) - Must have locations configured
* [Customer Setup](CustomerSetup.md) - Customer relationships established
* [Product Setup](ProductSetup.md) - Products must exist

**Downstream Processes:**
* [Treatment Scheduling](TreatmentScheduling.md) - Routes drive treatment schedules
* [Delivery Order Management](DeliveryOrders.md) - Delivery orders assigned to routes
* [Field Treatment Execution](FieldTreatments.md) - Field staff execute routes
* [Treatment Tracking and Monitoring](TreatmentTracking.md) - Monitor route performance

**Related Documentation:**
* [Distribution Overview](../../Distribution/Index.md)
* [Treatment Routes Lookup](../../Distribution/Lookups.md)

