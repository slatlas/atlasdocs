# Distribution

Distribution manages the delivery of products and services to customer locations, including delivery orders, sales orders, scheduling, route planning, and treatment execution. This module coordinates all aspects of product distribution from order creation through delivery and treatment.


## Overview

The Distribution module provides comprehensive tools for managing the entire order-to-delivery workflow. From creating orders and scheduling routes to tracking deliveries and recording treatments, this module ensures efficient product distribution and service delivery.

## Main Components

* [Delivery Orders](DeliveryOrders.md) - Manage delivery orders and dispatch
* [Order Scheduling](OrderScheduling.md) - Schedule treatments and deliveries
* [Sales Orders](SalesOrders.md) - Create and manage sales orders
* [Order Tracker](OrderTracker.md) - Real-time tracking of order status and location
* [Treatments](Treatments.md) - Record and manage treatment activities
* [Treatment Routes](TreatmentRoutes.md) - Create and manage treatment routes
* [Treatment Approvals](TreatmentApprovals.md) - Approve treatment routes and schedules
* [Route Tracker](RouteTracker.md) - Track route execution and progress

## Lookup Tables

For configuration and reference data used by Distribution, see [Distribution Lookups](Lookups.md).

## Workflow Overview

1. Create [Sales Orders](SalesOrders.md) for customer products and services
2. Generate [Delivery Orders](DeliveryOrders.md) from sales orders
3. Plan [Treatment Routes](TreatmentRoutes.md) and schedules
4. Use [Order Scheduling](OrderScheduling.md) to optimize delivery timing
5. Track progress with [Order Tracker](OrderTracker.md) and [Route Tracker](RouteTracker.md)
6. Record completed [Treatments](Treatments.md) for billing

## System Capacity

The Distribution module manages high-volume operations with:
* Over 49,000 delivery orders
* 22,000+ sales orders
* 99,000+ treatment records (nearly 2 million treatment items)
* Real-time status tracking and updates
* Multi-status workflow management (Unscheduled, Scheduled, Ready To Bill, Completed, On Hold)

## Mobile Integration

Distribution features integrate with the Atlas mobile app for field execution. See [Mobile Documentation](../Mobile/Index.md) for details on:
* Recording treatments in the field
* Completing delivery orders on mobile devices
* Real-time order and route tracking

