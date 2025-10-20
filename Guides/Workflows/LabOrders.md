# Lab Order Creation and Sample Collection

## Overview

Lab orders document requests for laboratory testing of produced water, chemical products, or other samples from field locations. This workflow is used by field personnel and lab coordinators to create lab test orders, collect samples in the field using mobile devices, track sample chain of custody, and submit samples to external or internal laboratories. Proper sample collection and tracking ensures accurate test results for production optimization and regulatory compliance.

## Prerequisites

**Required Permission:** `Pages.LabOrders.Create`

**Required Setup:**
* Lab agencies (testing laboratories) configured
* Lab types and test fields defined
* Locations must be set up
* Sample collection points configured
* Mobile device for field sample collection

**Related Prerequisites:**
* [Mobile App Setup](MobileSetup.md) - For field sample collection
* [Location Management](LocationSetup.md) - Locations must exist

## Workflow Diagram

```
Identify Testing Need → Create Lab Order → Specify Tests Required → Collect Sample in Field
       ↓
Record Sample Details → Label Sample → Submit to Lab → Track Status → Receive Results
```

## Step-by-Step Procedure

### Creating a Lab Order (Office)

1. **Navigate to Lab Orders**
   * Go to main menu → LIMS → Lab Orders (or Lab Dashboard)
   * Click "Create New Lab Order"

2. **Enter Order Details**
   * **Customer/Location:** Select well location for sampling
   * **Lab Agency:** Choose which lab will perform testing
   * **Lab Type:** Water analysis, chemical analysis, microbiology, etc.
   * **Priority:** Routine, rush, stat (affects turnaround time and cost)
   * **Requested By:** Person requesting the test
   * **Order Date:** Date order created

3. **Select Tests/Fields**
   * Choose which tests should be performed
   * Common tests: Iron, chloride, bacteria, pH, H2S, CO2, etc.
   * Can select individual tests or test packages
   * System may recommend tests based on location history or treatment program

4. **Set Sample Collection Details**
   * **Collection Point:** Wellhead, flowline, separator, tank, sales line
   * **Collection Date/Time:** When sample will be collected
   * **Assigned To:** Field personnel responsible for collecting sample
   * **Special Instructions:** Any specific collection requirements

5. **Save Lab Order**
   * Click "Save" - order status is "Draft" or "Pending Collection"
   * Order appears in field personnel's mobile app for sample collection

### Collecting Sample in the Field (Mobile)

6. **Access Lab Order on Mobile**
   * Open Atlas mobile app
   * Navigate to "Lab Samples" or "Lab Orders"
   * Select the lab order assigned to you
   * Review collection instructions

7. **Prepare for Sample Collection**
   * Gather required sampling equipment:
     * Clean sample bottles (provided by lab)
     * Labels with lab order number
     * Gloves and safety equipment
     * Cooler with ice if required
   * Verify you're at correct location and collection point

8. **Collect the Sample**
   * Follow proper sampling procedures:
     * Flush lines before collecting
     * Avoid contamination
     * Fill bottle per lab instructions (headspace, preservatives, etc.)
     * Collect from active flow if possible
   * Take sample at specified collection point

9. **Record Sample Details in Mobile App**
   * **Collection Time:** System records timestamp
   * **Collection Point:** Confirm or update
   * **Sample Appearance:** Note color, clarity, odor, presence of solids
   * **Production Status:** Well producing, shut-in, gas lift on/off
   * **GPS Location:** System captures coordinates
   * **Photos:** Take photo of sample and collection point

10. **Label Sample**
    * Write on bottle label:
      * Lab order number
      * Location name/ID
      * Collection date and time
      * Your initials
      * Collection point
    * Ensure label is legible and won't wash off

11. **Complete Sample Collection**
    * Tap "Complete Collection" in mobile app
    * Lab order status updates to "Sample Collected"
    * Data syncs to server

### Preparing and Submitting to Lab

12. **Store Sample Properly**
    * Place in cooler with ice if temperature control required
    * Protect from freezing
    * Keep upright to prevent leaks
    * Store away from direct sunlight

13. **Submit Sample to Lab**
    * Deliver samples to lab or arrange pickup
    * Include chain of custody form if required
    * Provide lab order number to lab
    * Update lab order status to "Submitted to Lab"
    * Note submission date and time

### Tracking Lab Order

14. **Monitor Lab Order Status**
    * Track in LIMS dashboard
    * Statuses: Draft → Collected → Submitted → In Progress → Completed
    * Follow up with lab if not receiving updates
    * Check expected turnaround time

15. **Receive Results**
    * Lab uploads results or results are imported
    * See [Lab Results Management](LabResults.md) workflow
    * Notification sent when results available

## Best Practices

### For Field Personnel
* **Collect carefully** - Contaminated samples give false results
* **Follow procedures** - Each test type may have specific collection requirements
* **Label immediately** - Don't wait - label as soon as sample is collected
* **Protect samples** - Keep cool and out of sunlight
* **Document thoroughly** - Good notes help interpret results later

### For Lab Coordinators
* **Plan ahead** - Schedule routine testing in advance
* **Batch samples** - Combine samples going to same lab to reduce costs
* **Track turnaround** - Monitor lab performance and follow up on delays
* **Review results** - Check results for anomalies before distributing

### Industry-Specific Tips
* **Regulatory requirements:** Some jurisdictions require specific testing frequencies
* **Bacteria samples:** Must be kept cool and tested within 24 hours
* **Preservatives:** Some tests require chemical preservatives added to sample bottles
* **Chain of custody:** For regulatory or legal samples, maintain strict documentation
* **Background production data:** Record current production rates with sample for context

## Troubleshooting

**Issue:** Cannot create lab order - location not found
* **Solution:** Verify location is active and set up in system. Location may need lab collection points configured. Contact administrator.

**Issue:** Don't have proper sample bottles
* **Solution:** Lab typically provides specific bottles for each test type. Contact lab to obtain proper bottles before collecting samples.

**Issue:** Sample collected but order not showing as collected
* **Solution:** Check mobile app sync - may not have uploaded yet. Ensure "Complete Collection" was tapped. Try syncing again. May need to manually update if sync failing.

**Issue:** Lab doesn't have record of sample
* **Solution:** Verify lab order number. Check that sample was properly labeled. Confirm sample was delivered to correct lab. May need to recollect if sample lost.

**Issue:** Results taking longer than expected
* **Solution:** Check lab order priority - routine samples take longer. Contact lab to check status. Some tests (bacteria, metals) take longer than others. May need to mark rush if urgent.

**Where to Get Help:**
* See [LIMS Overview](../../LIMS/Index.md)
* See [Create Lab Order documentation](../../LIMS/Create-Lab-Order.md)
* See [Mobile - Lab Samples](../../Mobile/Samples.md)
* Contact lab coordinator for testing questions
* Contact lab agency for result status or technical questions

## Related Workflows

**Upstream Processes:**
* [Location Management](LocationSetup.md) - Locations must be configured
* [Customer Setup](CustomerSetup.md) - Customer relationships established

**Downstream Processes:**
* [Lab Results Management](LabResults.md) - Next step: receive and manage results
* Treatment program adjustments based on results
* Regulatory reporting if applicable

**Related Documentation:**
* [LIMS Overview](../../LIMS/Index.md)
* [LIMS Setup](../../LIMS/Setup.md)
* [Mobile - Sampling Mode](../../Mobile/Sampling.md)

