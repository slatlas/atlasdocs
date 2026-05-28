# Lab Information Management System (LIMS)

## Reporting

LIMS Reporting produces the documents that communicate test results — internal lab reports for technicians and customer-facing reports for the requesting field personnel and clients.  Reports can be generated from recorded results or uploaded when an outside lab returns a finished file.

<br>

## Report Types

Each [Lab Type](Setup.md) is linked to the reports it produces:

* **Internal Report** — the standard PDF generated from the order's results, used by lab staff.
* **External Report** — the customer-facing version, used when results are reported to the requester or client.

Generated reports are stored with the order and listed in the LIMS reports history.

<br>

## Generating Reports

Reporting actions are available from the [LIMS Management Dashboard](LIMS-Management-Dashboard.md) grid:

| Action | Permission | Description |
|--------|------------|-------------|
| **Create Lab Report** | `Pages.LabReports.Create` | Enter or import results for an order, producing a result report.  See [Create Lab Results](Create-Lab-Results.md). |
| **Upload Lab Results** | `Pages.LabReports.Create` | Attach an external PDF report to one or more orders. |
| **Create Lab Results Report** | `Pages.LabReports.Create` | Produce a combined customer-facing results report for selected orders. |
| **Regenerate Reports** | `Pages.LabReports.Create` | Re-run report generation for selected orders after data changes. |
| **Export Lab Reports (CSV)** | `Pages.LabReports` | Export the report list to CSV. |

> When an order is marked **Reported**, its result reports become available and are distributed to the requesting Service Tech and Account Manager.

<br>

## Uploading an External Report

When a laboratory returns a finished PDF, use **Upload Lab Results** to attach it directly to the relevant orders.

#### Fields
  * **Report Type** is the kind of report being uploaded.
  * **Name** is a label for the report. *(Required.)*
  * **Description** is optional notes.
  * **File** is the PDF (or PDFs) to upload.
  * **Lab Orders** is the grid of orders the report is attached to (showing File, Sample Id, Type, Priority, Location, and Requested date).

<br>

## Export Templates

For data exports (rather than PDF reports), **Lab Export Templates** define which fields are exported and in what order.  Templates are configured in [Setup](Setup.md) and map columns to field types, mirroring the way import types map incoming files.

**Permission:** `Pages.LabExportTemplates`

<br>

## Analytics & Dashboards

Aggregated reporting is also available through the LIMS [Analysis](Analysis.md) views and the [User Dashboard](../Tutorials/User-Dashboard-Edit.md) widgets, which summarize results, turnaround, failure rates, and other metrics across the operation.

<br>

## Permissions

Access to LIMS Reporting features requires the following permissions:

| Display Name | Description |
|--------------|-------------|
| Lab Reports | View lab reports |
| Create Lab Reports | Generate, upload, and regenerate reports |
| Edit Lab Reports | Modify existing reports |
| Delete Lab Reports | Remove reports |
| Lab Export Templates | Configure export formats |
| Report Lab Orders | Mark orders as reported |

## Related Documentation

* [Create Lab Results](Create-Lab-Results.md) - Entering results that feed reports
* [Analysis](Analysis.md) - Result review and dashboards
* [Setup](Setup.md) - Configuring report and export formats
* [LIMS Management Dashboard](LIMS-Management-Dashboard.md) - Order and report management

![image-logo](../images/sllogo.PNG)
