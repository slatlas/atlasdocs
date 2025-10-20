# Lab Results Management

## Overview

Lab results management handles the receipt, entry, review, and approval of laboratory test results from external labs. This workflow is used by lab technicians and QC staff to import results from lab data files, manually enter results, review for accuracy and anomalies, approve results for distribution, and generate reports. Proper results management ensures accurate data for treatment optimization, regulatory compliance, and customer reporting.

## Prerequisites

**Required Permission:** `Pages.LabReports.Create`

**Required Setup:**
* Lab orders must exist with status "Submitted to Lab"
* Lab import types configured for data file formats
* Lab agencies set up with result mapping
* Fields and field types defined
* Lab result approval workflow configured (if required)

**Related Prerequisites:**
* [Lab Order Creation](LabOrders.md) - Orders must be created first

## Workflow Diagram

```
Receive Results from Lab → Import Data File OR Manual Entry → Review Results → Flag Anomalies
       ↓
Approve Results → Generate Reports → Distribute to Stakeholders → Analyze Trends
```

## Step-by-Step Procedure

### Importing Lab Results (from electronic files)

1. **Receive Results File from Lab**
   * Lab emails or uploads results file (CSV, Excel, PDF, custom format)
   * Save file to accessible location
   * Note lab agency and file format

2. **Navigate to Lab Results Import**
   * Go to main menu → LIMS → Import Lab Results
   * Or from LIMS Management Dashboard → Import Results

3. **Select Import Type**
   * Choose lab agency/import type (e.g., "ABC Labs - Water Analysis")
   * System knows how to parse that lab's file format
   * Upload or browse to select file

4. **Import and Map Results**
   * System reads file and maps to lab orders
   * Matches by sample ID, lab order number, or location
   * Verify mapping looks correct
   * System displays preview of data to import

5. **Review Import Preview**
   * Check that results matched to correct lab orders
   * Verify field values make sense (not obviously wrong)
   * Note any import errors or warnings
   * Fix mapping issues if needed

6. **Complete Import**
   * Click "Import" or "Process"
   * System creates lab result records
   * Lab order status updates to "Results Received"
   * Results now visible in LIMS dashboard

### Manual Entry of Lab Results

7. **Navigate to Lab Order**
   * Go to LIMS → Lab Orders
   * Find the lab order for manual entry
   * Click to open order details

8. **Enter Results**
   * Click "Enter Results" or similar button
   * System displays fields for each test ordered
   * Enter result values:
     * **Numeric results:** Enter number (e.g., Iron: 2.5)
     * **Text results:** Enter value (e.g., Appearance: Clear)
     * **Date results:** Select date (e.g., Sample received date)
   * Enter units if not pre-populated

9. **Enter Result Metadata**
   * **Test Date:** When lab performed test
   * **Result Date:** When results were reported
   * **Lab Technician:** Who performed test (if known)
   * **Method:** Test method used (if specified)
   * **Comments:** Any lab notes or observations

10. **Attach Lab Report** (if applicable)
    * Upload PDF of lab report
    * Scan paper reports if received via fax
    * Attach to lab order for reference

### Reviewing and Approving Results

11. **Review Results for Accuracy**
    * Navigate to LIMS Dashboard or Lab Results view
    * Filter to show "Pending Review" results
    * Compare results to:
      * Historical results for location
      * Expected ranges
      * Treatment program targets
      * Regulatory limits

12. **Identify Anomalies**
    * System may flag results outside normal ranges (red/yellow indicators)
    * Look for:
      * Extreme values (unusually high/low)
      * Impossible values (negative pH, etc.)
      * Results inconsistent with production or treatment
    * Mark results with flags or notes if questionable

13. **Investigate Issues**
    * If results seem wrong:
      * Verify sample was collected correctly
      * Check if lab made data entry error
      * Consider if production changes could explain results
      * May need to contact lab or request retest

14. **Approve Results** (if workflow requires)
    * Click "Approve Results"
    * Results status changes to "Approved"
    * Approved results can be reported to customers
    * Some results may auto-approve if within normal ranges

### Generating Reports and Analysis

15. **Generate Lab Reports**
    * Navigate to LIMS → Reporting
    * Select report type:
      * Individual sample report
      * Trend analysis (results over time)
      * Multi-location comparison
      * Regulatory compliance report
   * Select date range and locations
   * Generate report (PDF, Excel, etc.)

16. **Distribute Results**
    * Email reports to customers if applicable
    * Provide to operations for treatment program adjustments
    * File for regulatory reporting if required
    * Share with management for performance tracking

17. **Analyze Trends**
    * Review result trends over time
    * Identify patterns:
      * Increasing corrosion indicators
      * Bacteria levels trending up
      * Scale tendency changes
    * Use analysis to optimize treatment programs

18. **Update Treatment Programs** (if needed)
    * Based on results, may need to:
      * Adjust chemical dosages
      * Change treatment frequency
      * Switch to different products
      * Implement new treatments
    * Coordinate with operations team

## Best Practices

### For Lab Technicians
* **Verify immediately** - Review imported results same day received
* **Check ranges** - Question any results that seem unreasonable
* **Document issues** - Note any problems with samples or lab performance
* **Maintain standards** - Use QC samples to verify lab accuracy

### For QC Staff
* **Trend analysis** - Don't just look at individual results, analyze trends
* **Compare labs** - If using multiple labs, compare results for consistency
* **Regulatory focus** - Ensure compliance testing is prioritized and tracked
* **Turnaround time** - Monitor lab performance on result delivery

### Industry-Specific Tips
* **Iron and H2S:** High levels indicate corrosion risk - may need increased inhibitor
* **Bacteria:** Presence of SRB (sulfate-reducing bacteria) drives treatment changes
* **pH changes:** Can indicate scale issues or system upset
* **Chlorides:** High chlorides increase corrosion potential
* **Calcium/alkalinity:** Used to calculate scale tendency indices

## Troubleshooting

**Issue:** Import file not loading or failing
* **Solution:** Verify file format matches lab import type. Check that file is not corrupted. Ensure all required fields present in file. May need IT support to troubleshoot import configuration.

**Issue:** Results imported to wrong lab order
* **Solution:** Check sample ID matching. Lab may have used different identifier. May need to manually reassign results to correct lab order. Update import mapping if pattern issue.

**Issue:** Results seem obviously wrong
* **Solution:** Contact lab to verify. Check if units are correct (mg/L vs ppm, etc.). Review sample collection details - may have been contaminated. Consider retest if critical result.

**Issue:** Cannot approve results - button disabled
* **Solution:** Verify you have approval permission. Check if all required fields are populated. May need someone with higher authority to approve. Check workflow rules.

**Issue:** Historical results not showing in trends
* **Solution:** Verify date range selection. Check that historical results were properly imported/entered. Ensure location mapping is correct. May need to reprocess old imports.

**Where to Get Help:**
* See [LIMS Results documentation](../../LIMS/Create-Lab-Results.md)
* See [LIMS Import documentation](../../LIMS/Imports-Lab-Results.md)
* See [LIMS Reporting](../../LIMS/Reporting.md)
* See [LIMS Analysis](../../LIMS/Analysis.md)
* Contact lab coordinator for result interpretation
* Contact lab agency for result verification or retests

## Related Workflows

**Upstream Processes:**
* [Lab Order Creation](LabOrders.md) - Orders must be created and samples submitted first

**Downstream Processes:**
* Treatment program optimization
* Customer reporting
* Regulatory compliance reporting
* Operational decision-making

**Related Documentation:**
* [LIMS Overview](../../LIMS/Index.md)
* [LIMS Setup](../../LIMS/Setup.md)
* [LIMS Glossary](../../LIMS/Glossary.md)

