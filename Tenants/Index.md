# Tenants

Tenants represent separate organizations or business units within the Atlas system. Each tenant has its own isolated data, users, settings, and configurations, allowing multiple companies to use the same Atlas installation while keeping their data completely separate.

## Overview

The Tenants page allows host administrators to create, manage, and configure tenant organizations. Each tenant operates as an independent entity with its own database, users, and settings.

## Managing Tenants

### Creating a Tenant
Create a new tenant organization by providing a tenant name, admin email, and database configuration. Each tenant is assigned a unique identifier and can have its own custom subdomain.

### Editing Tenants
Modify tenant settings including name, connection string, edition assignment, and activation status. You can also manage subscription details and feature assignments for each tenant.

### Tenant Features
* Isolated data storage per tenant
* Individual user management
* Custom branding and settings
* Edition-based feature access
* Subscription management

## Permissions

Access to Tenants features requires the following permissions:

| Display Name | Description |
|--------------|-------------|
| Tenants | View tenant records |
| Create Tenants | Create new tenant organizations |
| Edit Tenants | Modify tenant settings |
| Delete Tenants | Remove tenant organizations |
| Manage Features | Manage tenant feature assignments |
| Impersonation | Impersonate tenant users for support |

> **Note:** Tenant management is restricted to host administrators only.

**Related Permissions:**

| Display Name | Description |
|--------------|-------------|
| [Editions](../Editions/Index.md) | Manage editions (assigned to tenants) |
| [Subscription](../System/Subscription.md) | Manage subscription settings |
| [Audit Logs](../System/AuditLogs.md) | View tenant activity logs |

## Related Documentation

* [Editions](../Editions/Index.md) - Feature packages for tenants
* [Subscription](../System/Subscription.md) - Subscription management

