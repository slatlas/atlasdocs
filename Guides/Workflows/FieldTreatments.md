# Field Treatment Execution

## Overview

Field treatment execution is the process of performing chemical treatments at well locations using the Atlas mobile application. This workflow is used by field technicians and pumpers to view assigned treatments, navigate to locations, record products applied and quantities used, document observations, and handle exceptions. Mobile execution ensures accurate real-time data capture and enables offline operation in areas with poor cellular coverage.

## Prerequisites

**Required Permission:** Mobile app access with treatment permissions

**Required Setup:**
* Mobile app installed and configured on device
* User account synced to mobile device
* Delivery orders assigned and dispatched
* Vehicle inventory loaded with required products

**Related Prerequisites:**
* [Mobile App Setup and Sync](MobileSetup.md) - Initial mobile setup
* [Delivery Order Management](DeliveryOrders.md) - Orders must be dispatched

## Workflow Diagram

```
Sync Mobile App → View Assigned Orders → Navigate to Location → Arrive at Location
       ↓
Select Treatment Order → Record Products Used → Enter Quantities → Add Notes/Photos
       ↓
Handle Exceptions (if any) → Complete Treatment → Sync Data to Server
```

## Step-by-Step Procedure

### Starting the Day

1. **Sync Mobile Device**
   * Open Atlas mobile app
   * Ensure Wi-Fi or cellular connection
   * Tap "Sync" to download today's assignments
   * Wait for sync to complete
   * See [Mobile Setup and Sync](MobileSetup.md) for details

2. **Review Assigned Treatments**
   * Tap "Treatments" or "Delivery Orders"
   * View list of treatments assigned to you
   * Check route sequence and locations
   * Note any special instructions

3. **Check Vehicle Inventory**
   * Verify all required products are loaded
   * Check quantities available
   * Report any shortages to dispatcher before leaving yard

### Executing Treatments in the Field

4. **Navigate to First Location**
   * Tap on first treatment in sequence
   * Tap "Navigate" to open GPS navigation
   * Drive to location using GPS directions
   * Note any road conditions or access issues

5. **Arrive at Location**
   * Tap "Arrive" when you reach the location
   * System records arrival time and GPS coordinates
   * Take safety precautions before approaching equipment

6. **Start Treatment**
   * Tap "Start Treatment"
   * System enters "Treatment Mode"
   * Timer starts tracking time on location

### Recording Treatment Details

7. **Select Products Used**
   * Products pre-populate from delivery order
   * Verify products are correct
   * Add additional products if needed
   * Specify injection point (wellhead, flowline, etc.)

8. **Enter Quantities**
   * Enter actual quantity of each product applied
   * Select unit of measure (gallons, quarts, ounces)
   * System deducts from vehicle inventory
   * Mark if tank was refilled/replenished

9. **Record Tank Readings** (if applicable)
   * Enter current tank level
   * Record gauge reading
   * Note if tank needs replenishment
   * Take photo of gauge if required

10. **Add Observations and Notes**
    * Document equipment condition
    * Note any leaks, failures, or issues
    * Record production status (running, down, etc.)
    * Add weather conditions if relevant

11. **Capture Photos**
    * Take photos of treated equipment
    * Photo tank gauges or fill levels
    * Document any problems or damage
    * Photos attach to treatment record

### Completing the Treatment

12. **Handle Exceptions**
    * **Location inaccessible:** Mark as "Cannot Access" and document reason (locked gate, road washed out, etc.)
    * **Wrong product needed:** Contact dispatcher, document, and request correct product
    * **Equipment down:** Note in observations, may skip treatment
    * **Customer not present:** Document if customer presence required

13. **Complete Treatment**
    * Review all information for accuracy
    * Tap "Complete Treatment"
    * System records completion time
    * Treatment marked complete in system

14. **Move to Next Location**
    * Return to treatment list
    * Select next location in route
    * Repeat process for each assigned treatment

### End of Day Process

15. **Complete Final Treatments**
    * Finish all assigned locations
    * Handle any remaining exceptions

16. **Sync Data to Server**
    * Find Wi-Fi or good cellular connection
    * Tap "Sync" to upload completed treatments
    * Verify all treatments synced successfully
    * Check for any sync errors

17. **Report Vehicle Inventory**
    * Mobile app shows remaining inventory
    * Report needs for next day's load
    * Note any product shortages

## Best Practices

### For Field Technicians
* **Sync morning and evening** - Download assignments in AM, upload completions in PM
* **Take photos of everything** - Photos help resolve disputes and provide documentation
* **Be accurate with quantities** - Billing depends on accurate quantity reporting
* **Document exceptions thoroughly** - Explain why location wasn't treated or work was different than planned

### Safety and Quality
* **Follow safety procedures** - Wear PPE, follow chemical handling protocols
* **Verify tank capacity** - Don't overfill customer tanks
* **Check compatibility** - Ensure mixing chemicals is approved
* **Inspect equipment** - Report leaks or equipment issues immediately

### Industry-Specific Tips
* **Lease access:** Call ahead if operator escort required
* **Tank inspection:** Check for overflow, leaks, or corrosion
* **Production equipment:** Don't treat if well is shut in unless instructed
* **Weather considerations:** Be cautious with icy equipment and slippery locations
* **Product rotation:** Follow treatment program - don't skip or substitute products without approval

## Troubleshooting

**Issue:** Cannot see assigned treatments in mobile app
* **Solution:** Ensure you've synced recently. Check that treatments are in "Dispatched" status. Verify you're assigned to the treatments. Check mobile app login.

**Issue:** GPS not working or inaccurate
* **Solution:** Enable location services for Atlas app. Try moving to open area away from buildings/trees. Restart app if GPS doesn't initialize.

**Issue:** Cannot complete treatment - button grayed out
* **Solution:** Verify all required fields are filled (products, quantities). Check that you've tapped "Start Treatment" first. If error persists, save as draft and sync later.

**Issue:** Mobile app running slow or freezing
* **Solution:** Close other apps to free memory. Restart the mobile app. If problem continues, restart device. May need to reinstall app.

**Issue:** Sync failing or incomplete
* **Solution:** Check cellular/Wi-Fi connection. Try syncing in area with better signal. If partial sync, try again later. Contact IT if repeatedly failing.

**Issue:** Wrong product on truck
* **Solution:** Contact dispatcher immediately. Document the situation. May need to return to yard or get product from another truck. Don't substitute without approval.

**Where to Get Help:**
* See [Mobile - Treating Mode documentation](../../Mobile/Treating.md)
* See [Mobile - Treatments](../../Mobile/Treatments.md)
* Contact dispatcher for assignment or product questions
* Contact IT support for mobile app technical issues
* Contact safety coordinator for chemical handling questions

## Related Workflows

**Upstream Processes:**
* [Delivery Order Management](DeliveryOrders.md) - Orders must be dispatched
* [Treatment Scheduling](TreatmentScheduling.md) - Schedule drives assignments
* [Mobile App Setup and Sync](MobileSetup.md) - Mobile must be configured

**Downstream Processes:**
* [Treatment Tracking and Monitoring](TreatmentTracking.md) - Supervisors monitor your progress
* [Invoicing Process](Invoicing.md) - Your completed treatments get invoiced
* [Inventory Management](InventoryManagement.md) - Product usage updates inventory

**Related Documentation:**
* [Mobile Application Overview](../../Mobile/Intro.md)
* [Mobile Treating Mode](../../Mobile/Treating.md)
* [Mobile Sync](../../Mobile/Sync.md)

