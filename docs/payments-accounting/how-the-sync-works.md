---
title: "How the sync works"
---

# How the sync works

## Turfware ↔ Sawfish — near real-time

Turfware and Sawfish talk to each other by **webhook**, so changes cross **within about a minute**. When Sawfish records a payment or updates an invoice, the Turfware order reflects it almost immediately — amount paid, amount due, and paid status.

## Sawfish ↔ your accounting system — a timed sync (~15 minutes)

Sawfish syncs with your accounting system (MYOB/Xero) on a **timed pull**, roughly **every 15 minutes**. So a change made **in MYOB** — a payment, or an invoice amendment — is picked up on the **next sync**, anywhere from **0 to about 15 minutes** later, and then flows on to Turfware.

!!! note "There's no manual 'sync now'"
    The sync runs on its own interval — there's no staff-facing button to force it sooner. If you need a change to appear quickly, make it on the **Turfware / Sawfish** side where you can (near real-time) rather than in MYOB (which waits for the next pull).

## What updates what

| You do this… | …and this happens |
|---|---|
| Take a payment **in Sawfish** (card / PayTo / PayID on the digital invoice) | Turfware shows the order **paid** within ~1 min; Sawfish posts the payment to MYOB on the next sync |
| Record a payment **in MYOB** | Flows **MYOB → Sawfish → Turfware** on the next ~15-min sync |
| Change a **paid order** in Turfware | Updates the **operational order only** — it does **not** change the invoice |
| Amend a **paid invoice** in MYOB | Updates Sawfish (amount, balance) → the Turfware invoice — but **not** the physical order |

!!! warning "The golden rule"
    **A change to the operational order and a change to the invoice are not the same thing.** Editing the order doesn't move the invoice, and editing the invoice doesn't move the order. Keep the two in step deliberately.
