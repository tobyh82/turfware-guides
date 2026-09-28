---
title: "What goes on the invoice"
---

# What goes on the invoice

When Turfware raises an invoice for an order, it builds the invoice line by line from the order and sends it to Sawfish. This page shows exactly which field ends up where — so you know what the customer will read, and which record to fix if a line looks wrong.

## The invoice header

| On the invoice | Comes from |
| --- | --- |
| Invoice number | The order's invoice number |
| Reference | The customer's PO number if one was entered on the order, otherwise the order number |
| Invoice date | The day the invoice is raised, unless a custom issue date is chosen |
| Due date | The customer's payment terms, unless a custom due date is chosen |
| GST | Lines are tax-inclusive or tax-exclusive according to the order's *rate includes GST* setting |
| Tracking category | The customer's Segment, on each turf line |

## The lines, in the order they appear

**1. Turf — one line per turf item on the order.**

- **Description** — the variety's **Full Name**. If Full Name is blank, its Short Name is used instead; if the variety can't be found, the line reads *N/A*. Nothing else from the turf record appears.
- **Quantity** — the line's square metres. **Unit price** — the line's rate. So a line reads, for example, *Sir Walter DNA Certified Buffalo Grass · 500 m² · $12.32*.
- **Discount** — the line's own percentage or dollar discount, if any.

**2. Products and services — one line per item.** Products and services are the same kind of record in Turfware, and they invoice the same way.

- **Description** — the item's **Short Name** (*N/A* if it can't be found). The Full Name on a product or service is not currently used on the invoice or anywhere else.
- **Quantity** — the quantity ordered. **Unit price** — the line's rate. **Discount** — the line's own discount.

**3. Freight** — only when the order has a freight price. The line reads *Freight Cost*. If freight is shown as a total, it's one line at the total; if shown per square metre, it's the freight quantity at the per-m² rate. The order's freight discount applies.

**4. Laying** — only when the order includes Preparation or Installation and has a laying price. The line reads *Laying Cost*, shown as a total or per m² the same way as freight, with the order's laying discount.

**5. Pickup** — only for pickup orders where the pickup location has a rate. The line reads *Pickup Cost*, one unit at the location's rate, with the order's pickup discount.

**6. Delivery details** — a description-only line: the delivery date and the delivery address, for example *14/10/2026 - 12 Sample Street, Brisbane QLD 4000 Australia*. For a pickup order it reads *Pick up location:* followed by the location's name and address, with the pickup date.

**7. Invoice notes** — a description-only line carrying the order's Invoice Notes, if any were entered.

!!! note "Freight, laying and pickup always print those fixed names"
    The words *Freight Cost*, *Laying Cost* and *Pickup Cost* are fixed. Naming a service in Farm Settings does not change them — those lines come from the freight, laying and pickup settings on the order, not from a service record.

## Which accounting codes each line posts to

Every line carries a Sawfish item code and account code. Turfware resolves them in a fixed order and uses the first one it finds.

| Line | 1st | 2nd | 3rd |
| --- | --- | --- | --- |
| Turf | The supplier's per-turf override (set on the [supplier](../web-app/turfware-setup/farm-settings/suppliers.md)) | The variety's own Sawfish Item Code and Account Code ([Turf](../web-app/turfware-setup/farm-settings/turf-varieties.md)) | The supplier's default codes |
| Product or service | The supplier's per-item override | The item's own Sawfish codes ([Products](../web-app/turfware-setup/farm-settings/products.md), [Services](../web-app/turfware-setup/farm-settings/services.md)) | The supplier's default codes |
| Freight and pickup | The delivery mapping in Order Settings ([Company Information](../web-app/turfware-setup/farm-setup/company-information.md)) | The Chart of Accounts freight/service mapping | — |
| Laying | The installer's installation item and account | The installer's Chart of Accounts mapping | The installation mapping in Order Settings, then a legacy fallback item code (105) |

If a turf, product or service has no Sawfish codes of its own and the supplier has none either, the invoice can't be generated — which is why those fields are marked *required for invoicing* on each record.

## The deposit invoice

A deposit invoice has a single line: a summary of the order's items, then *Deposit Payment – X%*, quantity 1, posted to the Deposit Payment Account Code set in [Company Information](../web-app/turfware-setup/farm-setup/company-information.md).

## Where each name shows up

The three names on a turf variety, and the two on a product or service, each appear in different places. Use this to decide what to type in each field.

| Record | Field | Where it appears |
| --- | --- | --- |
| Turf | **Short Name** | Order screens (Orders, On Hold, Lost, Delivery list), quotes, the delivery docket and coversheet, the order PDF, and the Harvesting App cut sheet |
| Turf | **Abbreviation** | The web Cut Sheet dashboard, where space is tight |
| Turf | **Full Name** | The invoice, the customer's order confirmation email, and the customer's order view |
| Product / Service | **Short Name** | The invoice, order and quote screens, the order PDF and the delivery docket |
| Product / Service | **Full Name** | Stored on the record but not currently shown anywhere |

So for turf, write the Short Name for staff and the Full Name for the customer. For products and services, the Short Name is what the customer sees on the invoice — make it customer-ready.

See also [How the sync works](how-the-sync-works.md) for what happens after the invoice reaches Sawfish.
