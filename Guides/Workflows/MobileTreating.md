# Mobile Treatment Mode

## Overview

Mobile treatment mode is the mobile app's specialized interface for executing chemical treatments at well locations in the field. This workflow is used by field technicians to switch to treatment mode, use optimized treatment screens, quickly record products and quantities, capture treatment-specific data, and efficiently move through route sequences. Treatment mode streamlines field data entry for faster, more accurate treatment recording.

## Prerequisites

**Required Permission:** Mobile app access with treatment permissions

**Required Setup:**
* Mobile app installed and synced
* Treatment/delivery orders assigned and dispatched
* User familiar with basic mobile app operation

**Related Prerequisites:**
* [Mobile App Setup and Sync](MobileSetup.md) - Mobile must be configured
* [Field Treatment Execution](FieldTreatments.md) - Understanding treatment process

## Workflow Diagram

```
Open App → Switch to Treatment Mode → View Route → Select Location → Navigate
       ↓
Arrive → Start Treatment → Quick Product Entry → Record Observations → Photos
       ↓
Complete → Move to Next → Repeat → Switch Out of Treatment Mode → Sync
```

## Step-by-Step Procedure

### Entering Treatment Mode

1. **Open Atlas Mobile App**
   * Launch app from device home screen
   * Ensure you've synced recently (see "Last Synced" time)

2. **Access Treatment Mode**
   * Tap "Treatment Mode" or "Treating" from main menu
   * OR tap "Start Route" if assigned to specific route
   * Screen changes to treatment-focused interface

3. **View Today's Route**
   * Treatment mode displays locations in route sequence
   * Color coding shows status:
     * **Gray:** Not started
     * **Yellow:** In progress
     * **Green:** Completed
     * **Red:** Exception/problem
   * See total locations and estimated time

### Navigating to Location

4. **Select Next Location**
   * Tap on first/next location in sequence
   * Location details appear
   * Review any special instructions or notes

5. **Navigate to Location**
   * Tap "Navigate" or "Directions"
   * App opens device's GPS navigation (Google Maps, Apple Maps)
   * Follow directions to location
   * GPS shows distance and estimated time

6. **Arrive at Location**
   * When you reach the location, return to Atlas app
   * Tap "Arrive" or "I'm Here"
   * System records arrival time and GPS coordinates
   * Treatment screen opens

### Recording Treatment (Treatment Mode Interface)

7. **Start Treatment**
   * Tap "Start Treatment" button
   * Timer starts (tracks time on location)
   * Product list appears

8. **Quick Product Entry**
   * Treatment mode shows simplified product entry:
   * **Pre-loaded Products:** Common products appear as large buttons
   * **Tap product** to add to treatment
   * **Enter quantity** using number pad
   * **Tap checkmark** to confirm
   * Much faster than standard form entry

9. **Use Quick Add Features**
   * **Favorite Products:** Your most-used products at top
   * **Route Products:** Products assigned to this route pre-populated
   * **Recent Products:** Products used at this location before
   * **Quick Quantities:** Common quantities (5 gal, 10 gal) as buttons

10. **Record Tank Readings** (if applicable)
    * Treatment mode shows dedicated tank reading section
    * Tap tank type (inhibitor tank, chemical tank, production tank)
    * Enter gauge reading quickly
    * Photo button right next to field for instant photo

### Treatment-Specific Features

11. **Capture Photos Quickly**
    * Tap camera icon (large, accessible)
    * Take photo of:
      * Treated equipment
      * Tank gauges
      * Chemical injection pump
      * Any issues or problems
    * Photos automatically attach to treatment

12. **Use Voice Notes** (if enabled)
    * Tap microphone icon
    * Speak observations (e.g., "pump running good, no leaks")
    * System transcribes to text
    * Saves time vs. typing in field

13. **Quick Status Indicators**
    * Tap status buttons for common conditions:
      * "Running" / "Down" / "Pumping"
      * "No Issues" / "Leak Detected" / "Needs Service"
      * Pre-set options vs. typing notes

14. **Handle Exceptions Quickly**
    * If location can't be treated:
    * Tap "Exception" button
    * Select reason from quick list:
      * "Locked Gate"
      * "Road Impassable"
      * "Equipment Down"
      * "Customer Request"
    * Add photo if needed
    * Complete exception - moves to next location

### Completing and Moving On

15. **Complete Treatment**
    * Review: products, quantities, photos, notes
    * Tap "Complete Treatment" (large button)
    * System records completion time
    * Treatment status updates to complete
    * Auto-advances to next location

16. **Move to Next Location**
    * Treatment mode automatically shows next location
    * Tap "Navigate" to get directions
    * Repeat process for each location on route
    * Progress bar shows route completion

### End of Route

17. **Complete Final Location**
    * Finish last treatment on route
    * Treatment mode shows "Route Complete"
    * Review: shows all locations completed

18. **Review Exception List**
    * See any locations marked as exceptions
    * Decide if any can be attempted again
    * Or leave for rescheduling

19. **Exit Treatment Mode**
    * Tap "Exit Treatment Mode" or "Done"
    * Returns to normal mobile app interface
    * Can review completed treatments in treatment history

20. **Sync Completed Work**
    * Find Wi-Fi or good cellular signal
    * Tap "Sync" to upload all completed treatments
    * Verify sync completes successfully
    * Check that no sync errors

## Best Practices

### For Field Technicians Using Treatment Mode
* **Use treatment mode all day** - Designed for speed and efficiency
* **Follow route sequence** - Optimized for drive time
* **Complete as you go** - Don't wait to end of day to record data
* **Use quick buttons** - Faster than typing or searching
* **Photo everything** - Photos are documentation and protection

### Efficiency Tips
* **Pre-load products** - Set up your favorite products in settings
* **Use voice notes** - Much faster than typing in truck
* **Batch photos** - Take all photos at once while at location
* **Review before complete** - Easier to fix now than later

### Safety and Quality
* **Don't rush safety** - Speed is good, but safety is first
* **Verify products** - Quick entry is fast, but double-check product selection
* **Complete data** - Missing data causes billing and compliance issues
* **Document problems** - Use exception codes and photos

## Troubleshooting

**Issue:** Treatment mode not available or grayed out
* **Solution:** Verify you have treatments/orders assigned. Check that orders are in "Dispatched" status. Sync to download latest assignments. May need treatment permission enabled.

**Issue:** Products not appearing in quick add list
* **Solution:** Check that products are assigned to route or location. Verify products are active. May need to search for product manually. Can add products to favorites in settings.

**Issue:** Can't complete treatment - button disabled
* **Solution:** Check that all required fields have data (products, quantities). Verify you tapped "Start Treatment" first. Must be at location (arrival recorded). Try scrolling - may be validation error below.

**Issue:** GPS navigation not opening from treatment mode
* **Solution:** Verify device GPS enabled. Check that location has GPS coordinates in system. May need to manually open navigation app. Try tapping "Navigate" again.

**Issue:** Photos not attaching to treatment
* **Solution:** Check camera permissions for app. Verify storage space available. Try taking photo again. May need to add photo manually after treatment saved.

**Issue:** Treatment mode too slow or laggy
* **Solution:** Close other apps. Reduce number of days synced. Clear old completed treatments from device. Restart app. May need device with more memory.

**Where to Get Help:**
* See [Mobile Treating Mode documentation](../../Mobile/Treating.md)
* See [Mobile Treatments documentation](../../Mobile/Treatments.md)
* See [Field Treatment Execution](FieldTreatments.md) for detailed treatment process
* Contact dispatcher for route or assignment questions
* Contact IT support for app technical issues

## Related Workflows

**Upstream Processes:**
* [Delivery Order Management](DeliveryOrders.md) - Orders must be dispatched
* [Treatment Scheduling](TreatmentScheduling.md) - Schedule creates assignments
* [Mobile App Setup and Sync](MobileSetup.md) - Mobile must be configured

**Downstream Processes:**
* [Treatment Tracking and Monitoring](TreatmentTracking.md) - Office monitors your progress
* [Invoicing Process](Invoicing.md) - Your treatments get billed
* Data analysis and reporting

**Related Documentation:**
* [Mobile Overview](../../Mobile/Intro.md)
* [Field Treatment Execution](FieldTreatments.md) - Detailed treatment workflow
* [Mobile Sync](../../Mobile/Sync.md)

