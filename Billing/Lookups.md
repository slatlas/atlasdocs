# Billing Lookups

This page documents the lookup tables and reference data used by the Billing module. These lookups provide configurable options for invoice generation, pricing, and billing processes.


## Billing Period and Timing

### Billing Periods
**Permission:** `Pages.Administration.BillingPeriods.Create`

Billing Periods define the timeframes for grouping billable activities (e.g., Monthly, Semi-Monthly, Weekly, By Delivery Date) for organized invoice generation.

## Invoice Configuration

### Invoice Templates
**Permission:** `Pages.InvoiceTemplates`

Invoice Templates define the layout, formatting, and content structure for generated invoices. Different templates can be used for different customers or invoice types.

### Invoice Terms
**Permission:** `Pages.InvoiceTerms`

Invoice Terms specify payment terms and conditions (e.g., Net 30, Net 60, Due on Receipt, 2/10 Net 30) that appear on invoices and affect payment tracking.

### Invoice Types
**Permission:** `Pages.Invoices.Create`

Invoice Types categorize invoices by purpose (e.g., Standard Invoice, Credit Memo, Debit Memo, Prepayment, Adjustment) for accounting and reporting.

## Pricing Configuration

### Price Schedule Calculation Types
**Permission:** `Pages.PriceScheduleCalculationTypes`

Price Schedule Calculation Types define how pricing is calculated (e.g., Fixed Price, Cost Plus Percentage, Volume Discount, Formula-Based) for flexible pricing strategies.

### Price Schedule Fee Types
**Permission:** `Pages.PriceScheduleFeeTypes`

Price Schedule Fee Types define additional fees and surcharges (e.g., Delivery Fee, Environmental Fee, Emergency Service Charge, Fuel Surcharge) that can be added to invoices.

## Tax Configuration

### Sales Tax Codes
**Permission:** `Pages.SalesTaxCodes`

Sales Tax Codes define tax rates and rules for different jurisdictions and product types, ensuring correct tax calculation on invoices.

## Sales Classification

### Sales Types
**Permission:** `Pages.Administration.SalesTypes`

Sales Types categorize sales transactions (e.g., Product Sale, Service Revenue, Rental Income, Freight Charge) for revenue classification and reporting.

