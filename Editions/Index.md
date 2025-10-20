# Editions

Editions define feature packages that can be assigned to tenants, controlling which functionality is available to each organization. Editions enable a tiered subscription model where different tenants can have access to different features based on their subscription level.

## Overview

The Editions page allows host administrators to create and manage feature packages. Each edition defines which features are enabled and can include usage limits for certain functionality.

## Managing Editions

### Creating an Edition
Create a new edition by providing a name, display order, and selecting which features should be included. You can configure features such as:
* Customer Management
* Lease Management  
* Billing Management
* Product Management
* LIMS (Lab Information Management System)
* FracJobs
* Reports

### Assigning Editions
Editions are assigned to tenants to control their available features. When a tenant's edition is changed, their feature access is updated immediately.

### Edition Features
* Feature-based access control
* Usage limit configuration
* Flexible subscription tiers
* Easy feature rollout management

## Permissions

Access to Editions features requires the following permissions:

| Display Name | Description |
|--------------|-------------|
| Editions | View edition definitions |
| Create Editions | Create new editions |
| Edit Editions | Modify existing editions |
| Delete Editions | Remove editions |
| Manage Edition Features | Configure features within editions |

> **Note:** Edition management is restricted to host administrators only.

**Related Permissions:**

| Display Name | Description |
|--------------|-------------|
| [Tenants](../Tenants/Index.md) | Assign editions to tenants |

## Related Documentation

* [Tenants](../Tenants/Index.md) - Tenant management and edition assignment

