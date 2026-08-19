---
title: "Order Settings"
---

# Order Settings

Order Settings is a section of [Company Information](farm-setup/company-information.md) that controls which products and services appear when creating orders, and how installation and freight charges map to your accounts. Leave everything unchecked to allow all.

## Where to find it

Left-hand navigation → System Settings → Company Information → Order Settings.

## Order / Quote — Products & Services

Toggle which offerings appear on orders and quotes. Turf, Products and Services are set up at the item level in Farm Settings; Installation is order-level only.

- Turf — turf varieties, paddocks and the harvest workflow — the core offering for turf farms. (Set up in [Farm Settings → Turf](farm-settings/turf-varieties.md).)
- Products — physical stock items sold alongside or instead of turf (fertiliser, levies, accessories). (Set up in [Products](farm-settings/products.md).)
- Installation — turf laying / installation as a line item on orders. There's no Farm Settings page — it's order-level only, and its accounting is mapped here (below).
- Services — service offerings (e.g. maintenance, call-outs). Account mapping is configured on each service in [Farm Settings → Services](farm-settings/services.md).

You can also restrict which farms are available when creating orders.

## Installation account mapping

A chart-of-account line for installation, so charges map to invoices via Sawfish. Set the Sawfish Account Code and Sawfish Item (e.g. *203 – Installation Sales* and *105 – Turf Laying*).

## Delivery / Freight account mapping

*(Admin only.)* Sets how delivery & freight charges map to invoices via Sawfish — lifted out of the old Chart of Accounts window so it lives in one place. Set the Sawfish Account Code and Sawfish Item (e.g. *202 – Freight Sales* and *100 – Turf Delivery*).

*[Screenshot: Order Settings — toggles + Installation/Freight Sawfish mapping — save as ss-order-settings.png]*

!!! note "Ties into the order page"
    What you enable here is exactly what shows in the Products & Services section when [creating an order](../order-management/creating-and-managing-an-order.md).
