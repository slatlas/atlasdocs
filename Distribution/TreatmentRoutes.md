# Treatment Routes

Treatment Routes organize locations into logical sequences for efficient service delivery. Routes group locations by geography, service frequency, or operational area to optimize field personnel productivity.

## Overview

The Treatment Routes page allows you to create and manage route configurations. Each route includes a sequence of locations, assigned personnel, schedule frequencies, and route-specific settings.

![Treatment Routes Interface](../images/TreatmentRoutes.PNG)

## Key Features

* Create and configure treatment routes
* Add locations to routes in optimized sequence
* Assign routes to field personnel or vehicles
* Set route schedules and frequencies
* Configure route-specific products and settings
* Manage route exceptions and variations
* Optimize routes for travel time and efficiency
* Batch edit dates and schedules
* Track treatment completion percentages
* View and manage route calendar

## Main Interface

### Route Selection Panel (Left Sidebar)

The left sidebar provides quick navigation between routes:

* **Route List** - Shows all available routes with treatment progress percentage
* **Select Driver** - Filter routes by assigned driver
* **Search** - Quick search to find specific routes

### Route Management Toolbar

The top toolbar provides access to key route management functions:

* **Requests 0** - View and manage route change requests
* **Approve Routes** - Approve pending route changes
* **Save** - Save route changes
* **New Schedule** - Create a new route schedule
* **Create new treatment route** - Add a new treatment route

### Route Tabs

The interface includes multiple tabs for comprehensive route management:

* **Routes** - Main view showing treatment schedule and locations
* **Personnel** - Manage personnel assigned to the route
* **Daily Setup** - Configure daily route parameters
* **Map** - Geographic view of route locations
* **Missed Treatments** - Track and manage missed service visits
* **Missing Dates** - Identify gaps in treatment schedules
* **Exceptions** - Handle special cases and variations

### Route Details

Each route displays:

* **Route Name** - With edit and download options
* **Total Count** - Number of treatments on the route
* **Active Count** - Number of currently active treatments
* **Date Range Selector** - Choose month and week view
* **Treated Progress** - Percentage of completed treatments

### Route Actions

The toolbar provides several batch actions:

* **Refresh** - Reload route data
* **Mark Treatments** - Mark multiple treatments as completed
* **Add Treatment** - Add a new treatment to the route
* **Dates** - Manage treatment dates
* **Show Duplicates Only** - Filter to show duplicate entries
* **Hide All Completed** - Filter out completed treatments
* **Save** - Save changes
* **Batch Edit Dates** - Update dates for multiple treatments
* **Batch Edit Schedules** - Modify schedules in bulk
* **Adjust From Treatment** - Adjust schedule based on a treatment
* **Delete All** - Remove all selected treatments

### Treatment Grid

The main grid displays treatment details with the following columns:

* **Actions** - Edit or delete individual treatments
* **Location** - Location identifier (e.g., SSU 7027)
* **Product** - Product name (e.g., FEDD-255, Hot Water)
* **Volume** - Treatment volume amount
* **Freq** - Frequency value (e.g., 7.00, 14.00)
* **Freq Name** - Frequency description
* **Ship To** - Shipping destination
* **Flush** - Flush indicator
* **%** - Completion percentage
* **End Date** - Treatment end date
* **Calendar Dates** - Daily columns showing treatment schedule (10/01, 10/02, etc.)

Treatments are organized by customer with collapsible sections for easy navigation.

## Additional Features

### Set Cycle Dates

Define the start and end dates for treatment cycles across the route.

### Re-Assign

Reassign treatments or entire routes to different personnel or drivers.

### Map View

View route locations geographically to optimize travel sequences and identify coverage areas.

### Search Functionality

Use the search box in the top right to quickly find specific treatments, locations, or products within the route.

## Permissions

Access to Treatment Routes features requires the following permissions:

| Display Name | Description |
|--------------|-------------|
| Treatment Routes | View treatment route records |
| Create Treatment Routes | Create new treatment routes |
| Edit Treatment Routes | Modify existing treatment routes |
| Delete Treatment Routes | Remove treatment route records |

**Related Permissions:**

| Display Name | Description |
|--------------|-------------|
| [Locations](../AreaManagement/Locations.md) | View locations (added to routes) |
| [Personnel](../AreaManagement/Personnel.md) | View personnel (assigned to routes) |
| Treatment Schedules | View schedules (route-based scheduling) |
| [Delivery Orders](DeliveryOrders.md) | View delivery orders (generated from routes) |
| [Route Tracker](RouteTracker.md) | Track route execution in real-time |

## Related Documentation

* [Treatment Schedules](../AreaManagement/Locations.md) - Location scheduling
* [Route Tracker](RouteTracker.md) - Real-time route tracking
* [Delivery Orders](DeliveryOrders.md) - Orders created from routes

