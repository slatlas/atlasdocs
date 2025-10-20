# Location Management

## Overview

Location management creates and configures well locations and facilities in Atlas where chemical treatment and services are performed. This workflow is used by data coordinators and field supervisors to add new well locations, enter GPS coordinates and details, set up treatment schedules, and link to leases and areas. Accurate location data is essential for field navigation, treatment tracking, and operational reporting.

## Prerequisites

**Required Permission:** `Pages.Locations`

**Required Setup:**
* Customers must exist
* Leases and areas should be configured
* Batteries may be set up for grouping
* Location types defined

**Related Prerequisites:**
* [Customer Setup](CustomerSetup.md) - Customer must exist first

## Workflow Diagram

```
Gather Location Info → Create Location → Enter GPS Coordinates → Configure Details
       ↓
Link to Lease/Area/Battery → Set Treatment Schedule → Configure Equipment → Activate Location
```

## Step-by-Step Procedure

### Creating a New Location

1. **Navigate to Locations**
   * Go to main menu → Area Management → Locations
   * Click "Create New Location" or use map view "Add Location"

2. **Enter Basic Information**
   * **Location Name:** Well name or facility name
   * **Location Code/API:** Unique identifier (often API well number)
   * **Location Type:** Well, Tank Battery, Facility, Pipeline, etc.
   * **Customer:** Select customer/operator
   * **Status:** Active, Inactive, Shut-in, Abandoned

3. **Enter GPS Coordinates**
   * **Latitude:** Decimal degrees (e.g., 35.12345)
   * **Longitude:** Decimal degrees (e.g., -101.12345)
   * **How to obtain:**
     * Use mobile app in field to capture GPS
     * Look up coordinates in mapping service
     * Import from data file
   * **Verify on map:** Location should appear in correct geographical area

4. **Enter Location Address**
   * **Physical Address:** Access directions or nearest address
   * **County:** County where located
   * **State:** State
   * **GPS Directions:** Specific driving directions to reach location

### Configuring Location Details

5. **Link Organizational Structure**
   * **Lease:** Select lease this location belongs to
   * **Area:** Geographic area (often auto-fills from lease)
   * **Battery:** If part of battery grouping
   * **Customer Project:** Link to specific project if applicable

6. **Configure Production Information**
   * **Production Type:** Oil, gas, water disposal, CO2, etc.
   * **Lift Type:** Pumping unit, gas lift, ESP, flowing, etc.
   * **Formation:** Producing formation name
   * **Completion Date:** When well was completed
   * **Current Production:** Approximate daily rates (used for treatment planning)

7. **Set Up Treatment Details**
   * **Treatment Frequency:** Daily, weekly, bi-weekly, monthly, as-needed
   * **Treatment Type:** Default treatment (corrosion inhibitor, scale inhibitor, etc.)
   * **Treatment Route:** Assign to specific route
   * **Injection Point:** Where chemical is applied (wellhead, flowline, etc.)
   * **Special Instructions:** Access codes, contact requirements, specific procedures

8. **Configure Equipment Details**
   * **Tank Information:**
     * Number of tanks
     * Tank capacities
     * Product stored in each tank
   * **Pumps/Compressors:** Equipment present
   * **Chemical Injection Equipment:** Pumps, meters installed
   * **Monitoring Equipment:** SCADA, RTUs, etc.

9. **Enter Contact Information**
   * **Field Contact:** Person to call for access
   * **Emergency Contact:** For urgent issues
   * **Phone Numbers:** Contact numbers
   * **Access Requirements:** Gate codes, escort needs

### Finalizing Location Setup

10. **Upload Documents** (optional)
    * Lease agreement
    * Plat map
    * Equipment diagrams
    * Photos of location
    * Regulatory permits

11. **Add Notes**
    * Document any special considerations:
      * Road conditions
      * Seasonal access issues
      * Equipment quirks
      * Customer preferences
      * Safety hazards

12. **Review and Save**
    * Verify all information is correct
    * Check GPS coordinates place location correctly on map
    * Confirm organizational links (lease, area, customer)
    * Click "Save"

13. **Set Status to Active**
    * Update status from Draft to Active
    * Active locations appear in treatment schedules
    * Can create sales orders and treatments for active locations

### Post-Creation Tasks

14. **Add to Treatment Route** (if applicable)
    * Navigate to Treatment Routes
    * Add new location to appropriate route
    * See [Treatment Route Setup](TreatmentRoutes.md)

15. **Create Sales Order** (if ongoing service)
    * Set up recurring sales order for regular treatment
    * See [Sales Order Creation](SalesOrders.md)

16. **Configure Price Schedule** (if custom pricing)
    * Set location-specific pricing if needed
    * See [Price Schedule Configuration](PriceSchedules.md)

## Best Practices

### For Data Coordinators
* **Accurate GPS is critical** - Field personnel use GPS to navigate
* **Complete details** - More information prevents field delays
* **Consistent naming** - Use standard format for location names
* **Link correctly** - Ensure customer, lease, area relationships are accurate

### For Field Supervisors
* **Update from field** - Use mobile app to add/update locations during field visits
* **Photo documentation** - Take photos of equipment and access points
* **Test navigation** - Verify GPS coordinates actually get you to the location
* **Document access** - Note gate codes, lock combinations, contact requirements

### Industry-Specific Tips
* **API numbers:** Use standard API well numbering for regulatory tracking
* **Lease naming:** Follow company conventions for lease and well naming
* **Legal descriptions:** Record legal description (Section-Township-Range) for regulatory compliance
* **Permit numbers:** Track injection permits, disposal well permits, etc.
* **Directional wells:** Note if horizontal well and pad location vs. bottomhole location
* **Access restrictions:** Document seasonal restrictions (winter roads, hunting season, etc.)

## Troubleshooting

**Issue:** GPS coordinates not working - location appears in wrong place
* **Solution:** Verify decimal degrees format, not degrees-minutes-seconds. Check that latitude is positive (northern hemisphere) and longitude is negative (western U.S.). Swap lat/long if backwards.

**Issue:** Location not appearing in treatment schedules
* **Solution:** Verify status is "Active." Check that treatment frequency is set. Ensure location is assigned to a treatment route if using route-based scheduling.

**Issue:** Cannot link to lease - lease not in dropdown
* **Solution:** Verify lease exists and is active. Check that you have permissions to access this lease. May need to create lease first.

**Issue:** Field personnel can't find location
* **Solution:** Verify GPS coordinates are accurate. Add detailed driving directions. Consider having field personnel update coordinates from actual location. Add photos of access roads and location.

**Issue:** Duplicate location error
* **Solution:** Location may already exist. Search by API number, location name, or lease. If truly separate, add differentiator to name. If duplicate, update existing record instead.

**Where to Get Help:**
* See [Locations documentation](../../AreaManagement/Locations.md)
* See [Mobile - Location Add](../../Mobile/NewLocation.md)
* See [Mobile - Location View](../../Mobile/Location.md)
* Contact field supervisor for operational questions
* Contact GIS/mapping specialist for GPS issues
* See [Imports - Locations](../../Imports/Locations.md) for bulk imports

## Related Workflows

**Upstream Processes:**
* [Customer Setup](CustomerSetup.md) - Customer must exist
* Lease and area configuration

**Downstream Processes:**
* [Treatment Route Setup](TreatmentRoutes.md) - Add location to routes
* [Sales Order Creation](SalesOrders.md) - Create orders for location
* [Lab Order Creation](LabOrders.md) - Collect samples from location
* [Field Treatment Execution](FieldTreatments.md) - Perform treatments at location

**Related Documentation:**
* [Area Management Overview](../../AreaManagement/Index.md)
* [Mobile - New Location](../../Mobile/NewLocation.md)

