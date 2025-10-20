# Product Management Lookups

This page documents the lookup tables and reference data used by the Product Management module. These lookups provide configurable options for categorizing products, inventory, and related entities.

**Feature Required:** `App.ProductManagementFeature`

## Product Classification Lookups

### Product Categories
**Route:** `/app/main/production/productCategories`  
**Permission:** `Pages.ProductCategories.Create`

Product Categories provide high-level groupings of products (e.g., Chemicals, Equipment, Services, Supplies) for organization and reporting.

### Product Types
**Route:** `/app/main/production/productTypes`  
**Permission:** `Pages.ProductTypes.Create`

Product Types provide detailed classification within categories (e.g., Corrosion Inhibitor, Scale Inhibitor, Biocide, Pump, Rental Equipment) for specific product management.

## Vehicle Lookups

### Vehicles
**Route:** `/app/admin/management/vehicles`  
**Permission:** `Pages.Administration.Vehicles.Create`

Vehicles maintains the fleet of trucks and service vehicles used for deliveries, treatments, and mobile inventory storage.

### Vehicle Types
**Route:** `/app/admin/management/vehicleTypes`  
**Permission:** `Pages.Administration.VehicleTypes.Create`

Vehicle Types categorize vehicles by purpose and configuration (e.g., Bulk Truck, Service Truck, Pickup, Tanker) for fleet management.

## Warehouse Lookups

### Warehouses
**Route:** `/app/admin/billing/warehouses`  
**Permission:** `Pages.Administration.Warehouses.Create`

Warehouses defines storage facilities and locations where inventory is maintained. This is both a functional module and a lookup for warehouse selection.

### Warehouse Divisions
**Route:** `/app/admin/billing/warehouseDivisions`  
**Permission:** `Pages.Administration.WarehouseDivisions.Create`

Warehouse Divisions define organizational or physical divisions within warehouses (e.g., Main Warehouse, Yard Storage, Hazmat Area, Cold Storage) for inventory organization.

## Quality Control Lookups

### Product QC Fields
**Route:** `/app/main/lims/labQCFieldTypes`  
**Permission:** `Pages.LabQCFieldTypes`  
**Feature Required:** `App.LabInformationManagementSystemFeature`

Product QC Fields define the test parameters and specifications measured during quality control testing (e.g., pH, Specific Gravity, Active Ingredient %, Appearance, Color).

