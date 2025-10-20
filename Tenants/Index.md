# Tenants

Tenants represent separate organizations or business units within the Atlas system. Each tenant has its own isolated data, users, settings, and configurations, allowing multiple companies to use the same Atlas installation while keeping their data completely separate.

**Route:** `/app/admin/tenants`
**Permission:** `Pages.Tenants`
**Feature Required:** None (Host-level feature)

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

