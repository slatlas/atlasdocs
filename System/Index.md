# System

System provides core configuration and administration functions for Atlas including settings, user management, security, integrations, and system maintenance.

## Overview

The System section contains essential administrative tools for configuring Atlas, managing users and permissions, monitoring system health, and integrating with external systems.

## Main Components

### Settings
* [Settings](../Web/admin/settings.md) - System-wide settings and configuration

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
* [Subscription Management](Subscription.md) - Subscription management
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

Under the general tab, you can configure default time zone settings for users. Each user can also change this setting for their own account. 

### Appearance

Under the appearance tab, you can upload a logo file and upload a custom css file to customize the look of the application. Uploaded logo and css files can be easily removed by using the clear button.

### User Management

Under the user management tab, you can configure user management settings. You can enable/disable user registration and make newly registered users active or passive by default.

Admins can also enable/disable captcha on user registration and login pages.

Admins can also enable/disable session timeout control for users. If enabled and the user does not provide any input to the site during the timeout period, a countdown modal will be displayed to the user. If the user still does not provide any input to the site during the modal countdown period, the user will be logged out.

Admins can enable/disable cookie consent so Atlas shows a cookie consent bar for users to accept the cookie policy of the application.

Admins can force email confirmation for login.

Admins can allow users to use Gravatar profile pictures.

### Security

Security tab contains password complexity settings. Admins can define password complexity settings and configure user lock out settings.
