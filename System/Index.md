# System

System provides core configuration and administration functions for Atlas including settings, user management, security, integrations, and system maintenance.

## Overview

The System section contains essential administrative tools for configuring Atlas, managing users and permissions, monitoring system health, and integrating with external systems.

## Main Components

### Settings
* [Host Settings](../Web/admin/settings.md) - System-wide settings for host administrators
* [Tenant Settings](../Web/admin/settings.md) - Tenant-specific configuration settings

### User and Access Management
* [Roles](../Roles/Index.md) - Role definitions and permission management
* [Users](Users.md) - User account management
* [Organization Units](OrganizationUnits.md) - Organizational hierarchy and structure

### System Configuration
* [Visual Settings](VisualSettings.md) - UI customization and branding
* [Languages](Languages.md) - Multi-language and localization settings
* [Email Templates](EmailTemplates.md) - Email template management
* [Invoice Statuses](InvoiceStatuses.md) - Invoice workflow configuration

### Integrations
* [Integrations](Integrations.md) - External system connections
* [QuickBooks Authentication](QBAuthenticationSessions.md) - QuickBooks integration management

### Monitoring and Maintenance
* [Mobile Logs](MobileLogs.md) - Mobile device activity and error logs
* [Audit Logs](AuditLogs.md) - System audit trail and compliance
* [Maintenance](Maintenance.md) - System maintenance tools (Host only)

### Advanced Features
* [Subscription Management](Subscription.md) - Tenant subscription management
* [Dynamic Extensions](DynamicExtensions.md) - Custom field extensions

## Common Administrative Tasks

### User Management
See the [User Management Guide](../Web/admin/usermanagement.md) for detailed procedures on creating and managing users.

### System Configuration
See the [Settings Guide](../Web/admin/settings.md) for information on configuring system-wide settings.

### Security
* Configure password policies
* Enable two-factor authentication
* Manage user lockout settings
* Review audit logs

### Monitoring
* Monitor mobile device activity
* Review system audit logs
* Check integration status
* Track user login history

## System Settings

System settings page is used to configure global settings.

### General

Under the general tab, you can configure default time zone setting for users of that tenant. Each user of the tenant can also change this setting for their own account. 

### Appearance

Under the appearance tab, each tenant can upload a logo file and upload a custom css file. In this way, each tenant can change the look of the application only for their account. Uploaded logo and css files can be easily removed by using the clear button.

### User Management

Under the user management tab, each tenant can configure some user management settings related to their account. Each tenant can enable/disable user registration for their account. Tenants can also make newly registered users for their account active or passive by default.

Admins can also enable/disable captcha on user registration and login page for your system.

Admins can also enable/disable session timeout control for users. If it is enable and the user does not provide any input to the site during the timeout period, a countdown modal will be displayed to user. If the user still does not provide any input to the site during the modal countdown period, user will be log out.

Also, Admins can enable/disable cookie consent so Atlas shows a cookie consent bar for the users to accept cookie policy of the application.

Admins can force email confirmation for login.

Admins can allow users to use Gravatar profile picture or not.

### Security

Security tab contains password complexity settings. Each tenant can define password complexity settings in this tab for their account. Admins can also configure user lock out settings.
