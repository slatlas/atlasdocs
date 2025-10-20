# Dashboard

The Dashboard provides a centralized view of key metrics and information relevant to your role within Atlas. There are three dashboard variants available depending on your access level: Host Dashboard for system administrators, Portal Dashboard for customer portal users, and Tenant Dashboard for internal users managing operations.

## Dashboard Types

### Host Dashboard
The Host Dashboard is available to system administrators and provides high-level oversight of all tenants, system performance, and administrative metrics across the entire Atlas platform.

**Route:** `/app/admin/hostDashboard`
**Permission:** `Pages.Administration.Host.Dashboard`

### Portal Dashboard  
The Portal Dashboard is designed for customer portal users to view location data, documents, and other customer-facing information relevant to their account.

**Route:** `/app/portal/dashboard`
**Permission:** `Pages.Portal.Dashboard`

### Tenant Dashboard
The Tenant Dashboard is the main operational dashboard for internal users, displaying production metrics, orders, treatments, and day-to-day operational information.

**Route:** `/app/main/dashboard`
**Permission:** `Pages.Tenant.Dashboard`

## Customization

All dashboards can be customized to display the widgets and information most relevant to your workflow. See [Dashboard Configuration](../Web/dashboard/customizing.md) for details on customizing your dashboard layout.

