# Customer Setup

## Overview

Customer setup creates and configures customer accounts in Atlas for organizations you provide chemical treatment services to. This workflow is used by account managers and administrators to enter customer information, configure billing preferences, set up customer projects, and link locations and leases. Proper customer setup is foundational for sales orders, billing, and operational management.

## Prerequisites

**Required Permission:** `Pages.Customers`

**Required Setup:**
* Customer types should be defined
* Price schedules may be configured for custom pricing
* Billing terms and payment methods available

## Workflow Diagram

```
Gather Customer Info → Create Customer Account → Enter Contact Details → Set Billing Preferences
       ↓
Create Customer Projects → Link Locations/Leases → Configure Price Schedules → Activate Account
```

## Step-by-Step Procedure

### Creating Customer Account

1. **Navigate to Customers**
   * Go to main menu → Area Management → Customers
   * Click "Create New Customer"

2. **Enter Basic Information**
   * **Customer Name:** Full legal company name
   * **Customer Code:** Short identifier (often operator code from industry records)
   * **Customer Type:** Operator, Service Company, Individual, etc.
   * **Status:** Active, Inactive, Prospect

3. **Enter Contact Information**
   * **Primary Contact:** Name and title
   * **Phone Number:** Main phone
   * **Email Address:** Primary contact email
   * **Billing Email:** Where invoices should be sent (may be different)
   * **Physical Address:** Street address, city, state, ZIP
   * **Mailing Address:** If different from physical

4. **Configure Billing Settings**
   * **Payment Terms:** Net 30, Net 60, Due on Receipt, etc.
   * **Invoice Delivery Method:** Email, mail, customer portal
   * **Billing Cycle:** Monthly, semi-monthly, by delivery date
   * **Billing Contact:** Person responsible for AP/payments
   * **Customer PO Required:** Yes/No - whether PO number needed on orders

5. **Enter Tax Information**
   * **Tax Exempt:** Yes/No
   * **Tax ID/EIN:** Federal tax ID number
   * **Sales Tax Code:** Default tax code for this customer
   * **Upload Tax Exemption Certificate:** If tax exempt

6. **Add Additional Contacts**
   * Click "Add Contact"
   * Enter name, title, phone, email
   * Specify role: Accounting, Operations, Emergency, Field Contact
   * Can add multiple contacts for different purposes

7. **Save Customer**
   * Click "Save" to create customer record
   * System assigns customer ID number

### Setting Up Customer Projects

8. **Create Customer Project** (if applicable)
   * From customer record, click "Add Project"
   * Or navigate to Area Management → Customer Projects
   * **Project Name:** Descriptive name (e.g., "North Field Development")
   * **Project Code:** Short identifier
   * **Customer:** Link to customer account
   * **Project Type:** Well Development, Maintenance, etc.
   * **Ledger Account:** Accounting code for project
   * **Start/End Dates:** Project timeline
   * **Status:** Active, Completed, On Hold

9. **Link Locations to Project**
   * Associate specific well locations with this project
   * Used for project-based billing and reporting
   * Treatments at these locations can be billed to project

### Linking Locations and Leases

10. **Associate Leases**
    * Link customer to leases they operate
    * Navigate to Leases and set customer as operator
    * Or from customer record, add lease associations

11. **Associate Locations**
    * Link customer to specific well locations
    * Set customer as operator or service recipient
    * Locations can be linked through leases or directly

### Configuring Pricing

12. **Review Default Pricing**
    * Customer initially uses standard product pricing
    * Review if custom pricing needed

13. **Create Price Schedule** (if needed)
    * See [Price Schedule Configuration](PriceSchedules.md) workflow
    * Set customer-specific pricing for products
    * Configure volume discounts, fees, surcharges

### Activating and Testing

14. **Review Customer Configuration**
    * Verify all information is correct
    * Check billing settings are appropriate
    * Confirm contacts are complete

15. **Set Status to Active**
    * Update customer status from Prospect to Active
    * Active customers appear in operational dropdowns
    * Can create sales orders for active customers

16. **Test Sales Order Creation**
    * Create a test sales order for the customer
    * Verify pricing applies correctly
    * Check that locations are available
    * Delete test order or mark as test

## Best Practices

### For Account Managers
* **Complete all fields** - More data now means fewer issues later
* **Verify billing contact** - Wrong email delays payment
* **Document agreements** - Note special terms, pricing, or service requirements
* **Set up projects early** - Easier to start with projects than retrofit later

### For Administrators
* **Consistent naming** - Use standard format for customer names and codes
* **Validate tax info** - Confirm tax exemption status and certificates
* **Link carefully** - Ensure locations and leases are properly associated
* **Security** - Consider data access if customer is also a competitor

### Industry-Specific Tips
* **Operator vs. service recipient:** Customer may operate lease or may be service company treating on behalf of operator
* **AFE tracking:** Some customers require Authorization for Expenditure (AFE) numbers for cost tracking
* **Joint interest billing:** In some cases, costs split between multiple parties
* **Regulatory compliance:** Maintain accurate customer data for regulatory reporting
* **Merger/acquisition:** Track parent/subsidiary relationships for consolidated billing

## Troubleshooting

**Issue:** Cannot create customer - duplicate name error
* **Solution:** Customer may already exist in system. Search carefully by name and code. If truly duplicate, add differentiator (location, division) to name. If existing record, update it rather than create new.

**Issue:** Billing email bouncing
* **Solution:** Verify email address is correct. Check for typos. Test by sending test email. May need to contact customer for correct address.

**Issue:** Customer not appearing in sales order dropdown
* **Solution:** Verify customer status is "Active" not "Prospect" or "Inactive." Check that you have appropriate permissions to access this customer.

**Issue:** Locations can't be linked to customer
* **Solution:** Verify locations exist and are active. Check that locations aren't already exclusively assigned to another customer. May need to update location operator field.

**Issue:** Tax exemption not applying to invoices
* **Solution:** Verify "Tax Exempt" flag is checked on customer. Confirm tax exemption certificate is current and uploaded. Check that customer's tax code is set correctly.

**Where to Get Help:**
* See [Customers documentation](../../AreaManagement/Customers.md)
* See [Customer Projects documentation](../../AreaManagement/CustomerProjects.md)
* Contact account manager for customer relationship questions
* Contact accounting for billing and tax questions
* Contact system administrator for system access issues

## Related Workflows

**Upstream Processes:**
* Sales and contracting process (outside system)
* Credit approval (outside system)

**Downstream Processes:**
* [Location Management](LocationSetup.md) - Link locations to customer
* [Price Schedule Configuration](PriceSchedules.md) - Set customer pricing
* [Sales Order Creation](SalesOrders.md) - Create orders for customer
* [Invoicing Process](Invoicing.md) - Bill the customer

**Related Documentation:**
* [Area Management Overview](../../AreaManagement/Index.md)
* [Imports - Customers](../../Imports/Customers.md) - Bulk customer import

