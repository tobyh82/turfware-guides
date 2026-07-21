---
title: "Shopify Pending"
---

# Shopify Pending

**Shopify Pending Orders** is a **review queue** for orders that come in from Shopify — both your **online store** and **Shopify POS**. Most orders pass straight through; the ones that land here need a human to check them before they go any further.

## Where to find it

Left-hand navigation → **Order Management → Shopify Pending**.

## How it works

When a Shopify order arrives, Turfware:

1. Creates the order and **initially marks it *Shopify Pending***.
2. **Recalculates the order total** from your Turfware pricing and **compares it to the total Shopify charged**.
3. **If the totals match** → the order is **automatically confirmed** and moves on to [Orders Confirmed](orders-confirmed.md) — no action needed from you.
4. **If the totals *don't* match** → the order **stays in Shopify Pending** for you to review.

## Why an order lands here

The usual cause is a **product-mapping gap**: a Shopify product (variant) that **isn't linked to the matching Turfware product**. Because Turfware can't price an unmapped line, the order is **missing information** and its total won't reconcile with Shopify — so it's held here rather than pushed into harvest and delivery with bad data.

## What to do

1. Open the pending order and check the lines against the Shopify order.
2. Fix the **product mapping** (link the Shopify product to the correct Turfware product) and correct any missing details.
3. Once the order is complete and the values reconcile, it can move into the normal workflow ([Orders Pending](orders-pending.md) → [Orders Confirmed](orders-confirmed.md)).

*[Screenshot: Shopify Pending Orders list — save as om-shopify-pending.png]*

!!! tip "Prevention"
    Keeping every Shopify product correctly **linked to its Turfware product** (in the product setup) means online orders reconcile automatically and rarely stop here.
