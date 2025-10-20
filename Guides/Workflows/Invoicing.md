# Invoicing Process

## Overview

The invoicing process converts completed delivery orders and treatments into customer invoices for payment. This workflow is used by billing staff and accounting personnel to review unbilled work, generate invoices with appropriate pricing, and track payment status. Invoices can be sent to customers electronically and integrated with accounting systems like QuickBooks.

## Prerequisites

**Required Permission:** `Pages.Invoices`

**Required Setup:**
* Completed delivery orders or treatments must exist
* Customer billing settings and terms configured
* Invoice templates set up
* Price schedules properly applied to customers

**Related Prerequisites:**
* [Delivery Order Management](DeliveryOrders.md) must be completed
* [Sales Order Creation](SalesOrders.md) establishes pricing

## Workflow Diagram

```
Completed Work → Ready to Bill Dashboard → Review Unbilled Items → Select Items for Invoice
       ↓
Generate Invoice → Apply Pricing/Terms → Review Invoice → Approve
       ↓
Send to Customer (PDF/Email) → Track Payment Status → Record Payment
       ↓
Export to Accounting System (if integrated)
```

## Step-by-Step Procedure

### Reviewing Unbilled Work

1. **Navigate to Ready to Bill Dashboard**
   * Go to main menu → Billing → Ready To Bill
   * Dashboard shows all completed work not yet invoiced

2. **Filter Unbilled Items**
   * Filter by customer, date range, or billing period
   * Filter by location, product, or service type
   * System displays delivery orders, treatments, and other billable activities

3. **Review for Accuracy**
   * Verify quantities and products are correct
   * Check that pricing matches customer agreements
   * Identify any items with missing or incorrect data
   * Resolve any issues before invoicing

### Generating Customer Invoices

4. **Select Items to Invoice**
   * Check boxes for items to include on the invoice
   * Can select multiple items for a single customer
   * Items are typically grouped by customer and billing period

5. **Create Invoice**
   * Click "Generate Invoice" or "Create Invoice"
   * Select the customer (if not already filtered)
   * Choose invoice template (standard, detailed, summary)
   * Set invoice date and due date

6. **Review Invoice Details**
   * Verify customer name, address, and billing contact
   * Check line items: products, quantities, prices, totals
   * Review taxes and surcharges applied
   * Verify payment terms are correct (Net 30, etc.)

7. **Apply Adjustments (if needed)**
   * Add manual line items for fees or adjustments
   * Apply discounts if approved
   * Add invoice notes or special instructions
   * Attach supporting documents if required

8. **Finalize Invoice**
   * Click "Save" to save as draft
   * Or click "Approve" to finalize the invoice
   * Approved invoices are locked and assigned an invoice number
   * Invoice status changes from "Draft" to "Approved"

### Sending Invoices to Customers

9. **Generate PDF**
   * Open the approved invoice
   * Click "Export to PDF" or "Print"
   * Review PDF for accuracy and formatting

10. **Email Invoice**
    * Click "Email Invoice" from the invoice screen
    * System uses customer's billing email address
    * Invoice PDF is automatically attached
    * Edit email message if needed
    * Click "Send"

11. **Update Invoice Status**
    * After sending, status updates to "Sent"
    * System records the date sent
    * Customer can also access via customer portal if enabled

### Tracking Payment

12. **Monitor Payment Status**
    * Navigate to Invoices dashboard
    * Filter by status: Sent, Overdue, Partially Paid, Paid
    * System highlights overdue invoices

13. **Record Payments**
    * Open invoice when payment is received
    * Click "Record Payment"
    * Enter payment amount, date, and method
    * Enter check number or reference
    * Click "Save"

14. **Handle Partial Payments**
    * Enter partial payment amount
    * Invoice status becomes "Partially Paid"
    * Remaining balance is calculated automatically
    * Record additional payments as received

15. **Export to Accounting System** (if integrated)
    * Invoices can sync to QuickBooks or other systems
    * Navigate to Integrations to manage sync
    * See [QuickBooks Integration](../../System/QBAuthenticationSessions.md)

## Best Practices

### For Billing Staff
* **Invoice promptly** - Generate invoices within 1-2 days of work completion to improve cash flow
* **Review carefully** - Double-check pricing and quantities before sending to customers
* **Batch by period** - Invoice all work for a customer in one billing period on a single invoice when possible
* **Document adjustments** - Always note the reason for any manual adjustments or discounts

### For Accounting Personnel
* **Reconcile regularly** - Match payments to invoices daily
* **Follow up on overdue** - Contact customers with invoices past due date
* **Track aging** - Monitor accounts receivable aging reports
* **Maintain audit trail** - Keep records of all invoice changes and payment history

### Industry-Specific Tips
* **Monthly billing cycles** are common - many operators expect monthly invoicing
* **AFE numbers** - Track customer Authorization for Expenditure (AFE) numbers for cost tracking
* **Lease-level billing** - Some customers require separate invoices per lease or well
* **Volume discounts** - Be aware of tiered pricing or volume commitments in customer contracts

## Troubleshooting

**Issue:** Completed work not appearing in Ready to Bill
* **Solution:** Verify delivery orders are marked "Completed" not "In Progress." Check date filters on the Ready to Bill screen. Ensure items haven't already been invoiced.

**Issue:** Pricing on invoice doesn't match customer agreement
* **Solution:** Check customer's assigned price schedule. Verify the effective dates on pricing. May need to manually override pricing with approval.

**Issue:** Cannot send email - no billing contact
* **Solution:** Update customer record with billing email address. Navigate to Customer management to add contact information.

**Issue:** Customer disputes invoice quantities
* **Solution:** Review the delivery order and treatment details. Check field notes and photos if available. Consult with field personnel who performed the work. Make adjustments and issue credit memo if warranted.

**Issue:** Need to void or cancel an invoice
* **Solution:** Open the invoice and change status to "Void." Add reason in notes. If payment was received, process refund first. Consider issuing credit memo instead for audit trail.

**Where to Get Help:**
* See [Invoices documentation](../../Billing/Invoices.md)
* See [Ready to Bill documentation](../../Billing/ReadyToBill.md)
* Contact accounting supervisor for pricing or payment questions
* Contact IT support for QuickBooks integration issues

## Related Workflows

**Upstream Processes:**
* [Sales Order Creation](SalesOrders.md) - Establishes pricing and terms
* [Delivery Order Management](DeliveryOrders.md) - Source of billable work
* [Field Treatment Execution](FieldTreatments.md) - Creates completed work to bill

**Downstream Processes:**
* Payment tracking in accounting system
* Accounts receivable management
* Financial reporting

**Related Documentation:**
* [Billing Overview](../../Billing/Index.md)
* [Distribution Overview](../../Distribution/Index.md)
* [Settings - Invoice](../../Web/admin/settings.md)

