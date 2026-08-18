---
title: "Changing a paid order"
---

# Changing a paid order

Orders change — a customer adds a pallet, or drops one. How you handle it depends on whether the order has been **invoiced** and **paid**.

## The order and the invoice are separate

Changing the **order** in Turfware (e.g. adding turf) updates the **operational order** — harvest and delivery — but it does **not** change the **invoice**. The invoice only changes when you, or your accounting system, change it explicitly.

## You can't amend an invoice that has a payment applied

This is true in **every** system — Turfware, Sawfish, MYOB and Xero: **an invoice with a payment applied cannot be amended.** To change it, the **payment must first be removed (unapplied) from the invoice**; then the invoice can be edited; then the payment is re-collected and re-applied.

## Increasing an order

**If the order is not yet paid** — the fastest path is to amend it in **Turfware**: update the order and **re-approve the invoice**. That pushes the revised invoice straight to Sawfish and on to your accounting system, without waiting for the ~15-minute MYOB→Sawfish pull.

**If the order is already paid** — because a paid invoice can't be amended:

1. **Remove the payment** from the invoice, so it can be edited.
2. **Increase** the order and the invoice.
3. **Re-collect** the new balance and re-apply the payment.
4. Allow the systems to catch up — up to ~15 minutes if the change was made in MYOB (see [How the sync works](how-the-sync-works.md)).

!!! tip "Make the change where it syncs fastest"
    Where you can, make invoice changes on the **Turfware / Sawfish** side — they cross within ~1 minute. A change made in **MYOB** waits for the next ~15-minute sync before the customer can pay the new balance on their digital invoice.
