---
title: "Shopify Pending"
---

# Shopify Pending

Shopify orders — from both your online store and Shopify POS — flow straight into your normal order workflow. The Shopify Pending screen is a review view that surfaces only the ones Turfware couldn't reconcile automatically, so you can sort them out. If a Shopify order reconciles cleanly, it never appears here.

## Where to find it

Left-hand navigation → Order Management → Shopify Pending.

## How it works

When a Shopify order arrives, Turfware:

1. Creates the order directly in your normal workflow at [Orders Pending](orders-pending.md), tagged as a Shopify order.
2. Recalculates the order total from your Turfware pricing and compares it to the total Shopify charged.
3. If the totals match → the order is automatically confirmed and moves on to [Orders Confirmed](orders-confirmed.md) — no action needed from you, and it never stops here.
4. If the totals *don't* match (or a line can't be priced) → it stays in Orders Pending, and shows on this Shopify Pending screen for review.

In other words, Shopify Pending isn't a stage every order passes through — it's simply a filtered list of Shopify orders still sitting in Pending, which are the ones with something to fix.

## Why an order lands here

The usual cause is a product-mapping gap: a Shopify product (variant) that isn't linked to the matching Turfware product. Because Turfware can't price an unmapped line, the order is missing information and its total won't reconcile with Shopify — so it's held here rather than pushed into harvest and delivery with bad data.

## What to do

1. Open the order and check the lines against the Shopify order.
2. Fix the product mapping (link the Shopify product to the correct Turfware product) and correct any missing details.
3. Once the order is complete and the values reconcile, confirm it — it drops off this screen and continues through the workflow to [Orders Confirmed](orders-confirmed.md) and on to harvest and delivery.

!!! tip "Prevention"
    Keeping every Shopify product correctly linked to its Turfware product (in the product setup) means online orders reconcile automatically and rarely stop here.
