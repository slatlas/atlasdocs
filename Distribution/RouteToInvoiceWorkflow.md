# Route to Invoice Workflow

This page describes the consignment and usage-billing cycle in Atlas — from product arriving at a customer's tank, through taking a reading of what the customer consumed, to producing the invoice. It explains each stage, how the pieces connect, and — most importantly — **how usage is calculated** so operations and billing staff can trust the numbers on a sales order.

## Overview

Atlas's consignment billing model is built around tanks at customer locations. Product is delivered to the tank, the customer uses some of it, and the customer is billed for the **usage** (not the delivery). To bill correctly, Atlas needs very little:

> **The only required path for billing is:**
>
> 1. Product is **delivered** to a location (a treatment record, or a consignment delivery order).
> 2. A **usage treatment** (tank-level reading) is recorded.
> 3. A **billing period** covering the treatment date exists.
>
> Atlas computes the consumption automatically and the result becomes a **sales order**, which is approved and turned into an **invoice**.
>
> **Routes, schedules, inventory routes, and BOLs are optional operational aids** — they make dispatching and paperwork easier, but they are *not* required for the usage calculation or for billing. You can skip all of them and the numbers will still come out right.

### The Minimum Path (no route, no schedule, no BOL)

The smallest workflow that produces a correctly-billed sales order is:

1. A **Location** exists with a **Product** (a tank).
2. A **Billing Period** covering the dates of the activity is configured.
3. Something gets **into** the tank. This can be:
   - A treatment with `IsUsage = No` and a delivered volume, **or**
   - A consignment delivery order recorded against the location.
   (If there is no delivery between readings, the calculation simply uses the difference between readings.)
4. A **usage treatment** (`IsUsage = Yes`) is recorded with the observed tank level. This can be entered three ways — all equivalent for billing:
   - From a driver's field reading.
   - By setting a **Starting Volume** when the tank is first created.
   - By using **Adjust Level** on the Tanks page at any time.
5. Atlas automatically creates or updates the **Location Usage** bucket and computes Monthly Usage.
6. When usage is positive, the row appears on the **Usage** grid — click **Create sales order** to generate it. Approve it. Invoice it.

### The Extended Path (routes, schedules, BOLs)

Everything below is *additional* — it organizes and automates the work of getting product to the tank and driving the route, but it does not change how usage is calculated:

- A **Treatment Route** groups tanks into a recurring driver run.
- A **Schedule** binds each tank to a route on a cadence.
- An **Inventory Route / Route Request** lays out the physical run and expands to per-tank stops.
- A **Bill of Lading (BOL)** documents the load on the truck.

Use these when they fit your operation. Skip them when they don't.

### What a Billing Period Is For

This is the one prerequisite that is *not* optional. Every usage treatment must fall inside an open billing period — if no matching period is configured when the reading is saved, Atlas rejects the save with **"No Billing Period Setup."** Make sure billing periods are configured in advance.

## Key Terms

| Term | Meaning |
|------|---------|
| **Route** | A driver's recurring run — truck, driver, warehouse, and a list of scheduled stops. Managed on the **Treatment Routes** page. |
| **Schedule** | "This product at this location is serviced by this route on this cadence." One schedule row = one stop on a route. |
| **Tank** | A location/product pair with a configured tank size. Managed on the **Location Products (Tanks)** page. |
| **Inventory Route / Route Request** | A saved list of locations used to dispatch driver inventory runs (different from a Treatment Route — see note below). Managed on the **Inventory Route Setup** page. |
| **Bill of Lading (BOL)** | The paperwork generated for the product that goes on the truck. |
| **Delivery Treatment** | A treatment record with `IsUsage = No` representing product added to the tank. |
| **Usage Treatment** | A treatment record with `IsUsage = Yes` representing a tank-level reading. |
| **Billing Period** | A date range (usually a calendar month). A billing period covering the treatment date **must exist** for usage to process. |
| **Location Usage** | The rolled-up summary of consumption for one tank in one billing period. This is the row that becomes a sales-order line. |

> **Note on terminology.** The word "Route" appears in two distinct places in Atlas. **Treatment Routes** (under Distribution) are the driver/truck/schedule records. **Inventory Routes** (under Inventory Route Setup) are saved location lists used for driver inventory runs. The two are coordinated by driver assignment and shared locations, but they are separate records.

---

## The Workflow at a Glance

```
┌──────────────────────────── REQUIRED ────────────────────────────┐
│                                                                   │
│   A Billing Period covering the treatment dates must exist        │
│                                                                   │
│   Tank (Location + Product)                                       │
│         │                                                         │
│         ▼                                                         │
│   Delivery to the tank                                            │
│     (a non-usage treatment or a consignment delivery order)       │
│         │                                                         │
│         ▼                                                         │
│   Usage Treatment (reading of tank level)                         │
│     • Field reading, OR                                           │
│     • Starting Volume when a tank is created, OR                  │
│     • Adjust Level from the Tanks page                            │
│         │                                                         │
│         ▼                                                         │
│   CheckUsage runs automatically                                   │
│     • Finds the billing period                                    │
│     • Computes Monthly Usage                                      │
│     • Creates/updates the Location Usage bucket                   │
│         │                                                         │
│         ▼                                                         │
│   Sales Order created from the Usage grid (status = Requested)    │
│         │                                                         │
│         ▼                                                         │
│   Approval (status = Ready For Billing)                           │
│         │                                                         │
│         ▼                                                         │
│   Invoice (Sales Order status = Invoiced)                         │
│                                                                   │
└───────────────────────────────────────────────────────────────────┘

┌──────────────────────── OPTIONAL (operational) ───────────────────┐
│                                                                   │
│   Treatment Route  →  Schedule  →  Inventory Route / Request      │
│                                 →  BOL from schedule              │
│                                                                   │
│   These organize dispatching and paperwork but do NOT change      │
│   how usage is calculated. Skip any of them if they don't fit     │
│   your operation.                                                 │
│                                                                   │
└───────────────────────────────────────────────────────────────────┘
```

---

## 1. Set Up the Route *(optional)*

> Routes are an operational convenience for organizing recurring driver work. **If your operation does not need them, skip to section 3 (Tank) and section 6 (Treatments).** Usage still calculates and sales orders still generate without any route in place.

A **Treatment Route** is the header for a driver's recurring run. It holds the driver, vehicle, source warehouse, and route type.

**To create a route:**
1. Navigate to **Distribution → Treatment Routes**.
2. Click **Create new treatment route**.
3. Enter a name, select the personnel (driver), vehicle, warehouse, and route type.
4. Save.

A new route starts empty. You attach tanks to it by creating schedules in the next step.

> **Tip.** The Treatment Routes grid only shows routes that have at least one schedule attached. A brand-new route with no schedules will not appear in the list until you add at least one.

See [Treatment Routes](TreatmentRoutes.md) for full page documentation.

## 2. Attach Tanks to the Route (Schedules) *(optional)*

A **schedule** binds a tank (location + product) to a route on a cadence. Each schedule row is effectively one recurring stop.

Key information on a schedule:
- Location and product — the tank being serviced.
- The route it belongs to.
- Planned delivery volume per visit.
- Recurrence rule (RRule), start date, optional end date.
- Whether it is a **special request** (a one-off visit, not recurring).

**Special requests** are single-use schedules. When a treatment is executed against a special schedule, the schedule is automatically ended, and (if tenant settings allow) a delivery order may be generated in the background.

## 3. The Tank (Location Product)

A **Location Product** record represents the physical tank at a customer location. It holds the **tank size**, which drives inventory and billing guardrails.

From the Tanks page you can:

- **Set a starting volume** when creating a new tank. Atlas automatically creates a starting-volume reading (a usage treatment with `CloseVolume = starting volume`) so the tank reflects the correct on-hand level immediately.
- **Adjust Level** at any time via the row action on the Tanks grid. This opens a modal that captures the date, the new level, and a note; it creates an `IsUsage = Yes` treatment so the change flows through the usage cycle just like a driver's field reading.

**Smart guardrails apply on both flows:**

| Rule | Enforced |
|------|----------|
| Volume cannot be negative | ✅ |
| Volume cannot exceed the tank size | ✅ |
| Treatment date cannot be in the future | ✅ |
| Treatment date cannot be earlier than the most recent reading on the tank | ✅ |
| Product must be selected before a starting volume can be supplied | ✅ |

The back-dating rule is critical — inserting a reading dated before the latest existing reading would corrupt subsequent usage calculations, so Atlas blocks it.

## 4. Set Up the Inventory Route / Request *(optional)*

Under **Inventory Route Setup** you create and manage the driver's inventory runs. There are two levels:

- **Inventory Route** — a saved, named list of location IDs for a default driver. Create this once and reuse it.
- **Route Request** — one execution of that inventory route (a driver, a day, a set of locations). Each request automatically expands into **stops** — one stop per tank (location + product) where tanks have been defined, otherwise one stop per location.

Each stop tracks its own status — **Pending**, **In Progress**, **Completed**, or **Skipped** — and can be linked to a BOL, a delivery order, and the eventual usage treatment.

The **Inventory Route Setup** grid supports click-through navigation: clicking the blue Customer, Lease, Location, or Product cells opens the respective entity in a new browser tab, so the dispatcher can quickly drill into any row without losing their place.

## 5. Create the Bill of Lading *(optional)*

When the truck is loaded, Atlas creates a **Bill of Lading (BOL)** from the selected schedules. This is a separate, consignment-specific flow from the standard order-based BOL.

**What the schedule BOL captures:**
- Header information: driver, vehicle, BOL date, truck number, consignee/origin/destination addresses.
- Line items — one line per product, where the quantity is the sum of the planned volumes of every schedule selected for that product.
- Back-linking: the BOL number is written onto every matching inventory-request stop, and those stops are marked **Completed**. Parent request counts are recalculated.

> **Important.** BOLs created from a schedule are **not** tied to a Shipment record. This is by design — the load is planned and signed out before there is any sales order to bill against. This has a downstream implication during sales-order approval (see step 8).

## 6. Record Treatments — the Required Step

Every change at a tank is a **Treatment** record. You don't need to be on a route to record one; treatments can come from field entry, from a driver's mobile device, from Adjust Level on the Tanks page, or from background processing of a delivery order.

### Delivery treatments (`IsUsage = No`)

- Represent product going **into** the tank.
- `Delivered Volume` = gallons added.
- Can be linked to a delivery order.
- **For delivery volume to count in the usage math, the treatment must be linked to a delivery order whose type is Consignment.** A treatment that is not tied to a consignment delivery order is still recorded, but the usage calculation treats the tank as if the product simply appeared between readings — which means Atlas will back-compute the entire difference as consumption. In most setups consignment deliveries are the right way to get product onto the tank.
- If you never deliver between readings and the tank simply draws down, no delivery treatment is needed; Atlas just compares the two readings.

### Usage treatments (`IsUsage = Yes`) — the step that triggers billing

- A tank-level **reading**, not a pour.
- `Close Volume` = the level observed now.
- Delivered volume is cleared — delivery amounts belong on delivery rows, not on readings.
- Validation (the smart guardrails from section 3) applies on every insert.
- **Saving a usage treatment is what actually produces the billable quantity.** The moment the reading is saved, Atlas runs the CheckUsage calculation (section 7) and the resulting Monthly Usage lands in the Location Usage bucket, which then appears on the Usage grid as *ready to bill*.

A usage treatment can be created three ways, all equivalent for billing:

1. A driver or field rep enters a reading (including on the mobile app).
2. A **Starting Volume** supplied when a tank is first created — Atlas writes an initial usage treatment for you.
3. **Adjust Level** on the Tanks page — Atlas creates a usage treatment dated and valued as you specify.

None of these require a route, a schedule, or a BOL.

## 7. How Usage Is Calculated

**This is the step that drives the sales order, so it matters most.** Every time a usage treatment (any tank-level reading) is saved, Atlas runs an automatic calculation to:

1. Assign the treatment to a billing period.
2. Compute the **Monthly Usage** (gallons consumed) on that treatment.
3. Find or create the **Location Usage** bucket — the summary for this tank, this product, this period.
4. Roll up the bucket's totals.

### Step 1 — Locate the Billing Period

Atlas looks up the billing period whose date range contains the treatment date. **If none exists, the save is rejected with "No Billing Period Setup."** Operations must ensure billing periods are configured in advance.

### Step 2 — Clear Delivered Volume on the Reading

A reading is not a delivery. Atlas sets `Delivered Volume = null` on the incoming usage treatment to keep the data clean.

### Step 3 — Find or Create the Location Usage Bucket

For this (location, product, billing period):
- If a bucket already exists, Atlas reuses it and points the new treatment at it.
- Otherwise, Atlas creates a fresh bucket with:
  - **Opening Date** = the reading's date.
  - **Opening Volume** — preferred in this order:
    1. The **closing volume of the previous period's bucket** (so month-to-month continuity is preserved).
    2. The opening volume of the earliest unattached consignment delivery in the period.
    3. The reading's own open/close volume as a last resort.
  - If the bucket has `Is Manual Open Volume = Yes`, Atlas keeps the operator-set opening value unchanged.

### Step 4 — Compute Monthly Usage (Two Branches)

Atlas looks for the **last prior usage reading** on this tank in the *same* billing period (exceptions excluded).

**Branch A — A prior reading exists in this period (this is the normal case).**

1. Atlas sums all **consignment delivery** gallons between the prior reading's date and the new reading's date.
2. Those deliveries are attached to the current Location Usage bucket so the math is traceable.
3. The formula:

   ```
   Monthly Usage = Deliveries since last reading
                 + Last Reading Close Volume
                 − New Reading Close Volume
   ```

   In words: *"The tank had the old closing level plus whatever was delivered since; whatever is left over compared to the new reading is what got consumed."*

**Branch B — No prior reading exists in this period (the first reading of a new period).**

1. Atlas finds the most recent treatment in the period (delivery or usage).
2. The formula:

   ```
   Monthly Usage = Last Treatment Close Volume − New Reading Close Volume
   ```

   This simpler formula applies because the first reading of a period has no sealed baseline to extend from.

### Step 5 — Roll Up the Bucket

- **Bucket Monthly Usage** = sum of Monthly Usage across all unbilled usage treatments in the bucket, including the new one.
- **Final Monthly Usage** = Monthly Usage + any manual Adjustment Amount on the bucket.
- **Closing Volume** on the bucket = the new reading's Close Volume.

### Worked Example

A tank of methanol with a 2,000-gallon size has the following activity in April:

| Date | Event | Close Volume | Delivered | Monthly Usage calculated |
|------|-------|-------------:|----------:|-------------------------:|
| Apr 1 | Tank created with Starting Volume = 1,500 | 1,500 | — | 0 (first reading) |
| Apr 10 | Consignment delivery of 500 gallons | — | 500 | (not a reading) |
| Apr 20 | Driver reads the tank | 1,200 | — | 500 + 1,500 − 1,200 = **800** |

On April 20, Atlas ran Branch A:
- Prior reading's Close Volume = 1,500.
- Deliveries between Apr 1 and Apr 20 = 500.
- New reading's Close Volume = 1,200.
- **Monthly Usage = 800 gallons** — the amount consumed between the two readings.

The April Location Usage bucket for that tank now holds:
- Opening Volume = 1,500 (set when the bucket was created on Apr 1).
- Closing Volume = 1,200 (the latest reading).
- Monthly Usage = 800.
- Final Monthly Usage = 800 (assuming no adjustment).

That **800** is what becomes the quantity on the sales order.

### Edge Cases Worth Knowing

- **Negative monthly usage.** If the new reading's level is higher than the implied pre-reading level (prior close + deliveries), the formula yields a negative number. Atlas does **not** clamp this — it surfaces the anomaly so operations can investigate (usually an undocumented delivery or a data-entry error).
- **Treatment exceptions.** Readings marked with an exception type are skipped when Atlas looks for the "last reading" and are kept out of the Location Usage rollup.
- **Crossing billing periods.** The new bucket's Opening Volume is pulled from the previous bucket's Closing Volume, so month-to-month continuity is automatic.
- **Recalculation.** When historical data is corrected (for example, a back-dated reading is inserted through an administrative action, or an exception is added later), a full recalculation walks every treatment in the period in date order and reapplies the math.

## 8. Create the Sales Order

When at least one Location Usage bucket has `Final Monthly Usage > 0`, no Sales Order yet, and no Invoice yet, it appears on the **Usage** grid as *ready to bill*.

**To create a sales order from usage:**
1. Open the **Usage** grid (under Treatments).
2. Select one or more rows belonging to the **same customer**.
3. Click **Create sales order**.
4. The Create/Edit Sales Order modal opens, preloaded with:
   - One line per selected Location Usage row.
   - **Quantity = Final Monthly Usage** of the bucket.
   - Location, product, and (optionally) opening volume from the bucket.
   - Customer resolved from the location automatically if not already set.
   - Sales Type defaulted to the **Sales** type (seed convention — this type should have `Requires Shipment = No` so usage sales orders approve without prompting for a BOL).
5. Save. The new order is created with status **Requested**.

Behind the scenes, Atlas also:
- Stamps every treatment in the bucket with the new Sales Order Item ID so the billing lineage is traceable.
- Sets each linked treatment's `Close Date` to now.
- Writes the **Closing Volume**, **Closing Date**, and **Sales Order ID** back onto the Location Usage bucket.

From this point the bucket is claimed — it will no longer appear on the ready-to-bill list.

See [Sales Orders](SalesOrders.md) for full sales-order page documentation.

## 9. Approve the Sales Order

Approval flips the order to **Ready For Billing** status, which is the gate for invoicing.

**Normal path.** For sales types with `Requires Shipment = No` (the usual case for consignment usage), clicking **Approve** moves the order straight to Ready For Billing.

**BOL prompt path.** For sales types with `Requires Shipment = Yes`, Atlas checks whether any Shipment record is already linked to this sales order. If none exists, the approval button opens the **Create BOL from Orders** modal instead of approving directly. That modal creates both a Shipment record and a BOL tied to the order; once that's saved, the order can be approved normally.

> **Consignment gotcha.** BOLs created earlier in the workflow from a schedule (step 5) **do not** link to a Shipment. So a sales type with `Requires Shipment = Yes` will prompt for a BOL at approval time even if a schedule-based BOL already exists for the same product. Two resolutions:
>
> 1. Configure the sales type used for consignment usage to set `Requires Shipment = No`. This is the recommended approach and is documented in the Consignment Sales Order Approval guide.
> 2. Let the approval flow create a new Shipment+BOL via the modal.
>
> **Mass Approve** bypasses the shipment check entirely and approves every order in Requested status — handle consignment sales types accordingly.

### Status Codes in This Workflow

| Code | Name | When |
|------|------|------|
| Req | Requested | Sales order just created |
| RFB | Ready For Billing | After approval |
| INV | Invoiced | After every line has been invoiced |
| CX | Cancelled | Manual |
| PD | Paid | External/ledger |

## 10. Generate the Invoice

**To invoice:**
1. Navigate to **Billing → Invoices → Create**.
2. Select approved sales order items (status = Ready For Billing, no invoice yet).
3. Choose the grouping strategy — per location, per lease, per sales order, or combined into one invoice.
4. Save.

Atlas splits the selection into as many invoice headers as the grouping requires, and for each line:
- Inserts an **Invoice Item**.
- Sets the Sales Order Item's `Invoice Item ID` so the line is marked billed.
- Links any treatments that fed the sales order item to the invoice item as well (for full traceability from invoice back to individual field readings).
- When **every** line on a sales order has been invoiced, moves that sales order's status to **Invoiced** and stamps the matching Location Usage buckets with the invoice item ID.

Customer, lease, and well information on the invoice is pulled from the sales order item and its linked location, so each line carries the correct billing account and integration IDs.

> **Period closure.** Editing an invoice that falls into a closed billing period is blocked — once a period is closed, its invoices are sealed.

See [Invoices](../Billing/Invoices.md) for full invoice-page documentation.

---

## Permissions

Access to the Route to Invoice workflow requires permissions from several modules:

| Display Name | Description |
|--------------|-------------|
| [Treatment Routes](TreatmentRoutes.md) | Create and manage routes |
| Treatment Schedules | Link tanks to routes on a cadence |
| Location Products (Tanks) | Manage tanks, starting volume, adjust level |
| Location Inventory Requests | Manage inventory routes and route requests |
| Bill of Ladings | Create BOLs from schedules |
| [Treatments](Treatments.md) | Record delivery and usage treatments |
| Location Usages | View the usage-billing rollups |
| Location Usages Recalculation | Run full recalculation of a period |
| Billing Periods | Configure the periods that contain treatments |
| [Sales Orders](SalesOrders.md) | Create, edit, and approve sales orders |
| [Invoices](../Billing/Invoices.md) | Generate invoices from approved orders |
| Sales Types | Configure `Requires Shipment` on the sales type used for consignment usage |

## Related Documentation

* [Treatment Routes](TreatmentRoutes.md) — Route header setup
* [Treatments](Treatments.md) — Field and office treatment records
* [Treatment Approvals](TreatmentApprovals.md) — Review and approve treatment activity
* [Sales Orders](SalesOrders.md) — Sales order creation and management
* [Invoices](../Billing/Invoices.md) — Invoicing approved sales orders
* [Ready To Bill](../Billing/ReadyToBill.md) — Review billable activity before invoicing
* [Location Tank Inventory](../Product/LocationTankInventory.md) — Tank-level inventory overview
