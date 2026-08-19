---
title: "How the sync works"
---

# How the sync works

## Turfware ↔ Sawfish — near real-time

Turfware and Sawfish talk to each other by webhook, so changes cross within about a minute. When Sawfish records a payment or updates an invoice, the Turfware order reflects it almost immediately — amount paid, amount due, and paid status.

## Sawfish ↔ your accounting system — a timed sync (~15 minutes)

Sawfish syncs with your accounting system (MYOB or Xero) on a timed pull, roughly every 15 minutes. So a change made in your accounting system — a payment, or an invoice amendment — is picked up on the next sync, anywhere from 0 to about 15 minutes later, and then flows on to Turfware.

!!! tip "The Sync now button"
    Sawfish has a Sync now button — Settings → Invoice Settings — that pulls your latest account assets (chart of accounts, items and tax codes) from your accounting system on demand, up to 10 times a day (it shows the attempts remaining). Use it after you add a new account code or item in MYOB/Xero so it's available in Sawfish straight away. It refreshes the accounting structure — it doesn't re-pull invoices or payments, which stay on the timed sync above.

    *[Screenshot: Sawfish → Invoice Settings → Sync now — save as pa-sawfish-sync-now.png]*

## What updates what

| You do this… | …and this happens |
|---|---|
| Take a payment in Sawfish (card, PayTo, PayID, Tap to Pay, Apple/Google Pay) | Turfware shows the order paid within ~1 min; Sawfish posts the payment to your accounting system on the next sync |
| Record a manual (off-rails) payment in Turfware | Marks the Sawfish invoice paid — which stops the payment-reminder emails — but your accounting system is not updated; the money is reconciled there manually |
| Record a payment in your accounting system (MYOB / Xero) | Flows accounting → Sawfish → Turfware on the next ~15-min sync |
| Amend an unpaid invoice in Turfware | Flows automatically to Sawfish and your accounting system |
| Amend a paid invoice in your accounting system | Flows to Sawfish, but not back to the physical Turfware order — you must manually amend it in Turfware to match |

!!! warning "Amend before payment; intervene after"
    Invoices flow Turfware → Sawfish → your accounting system automatically, up until a payment is applied. Once a payment is on the invoice, manual intervention is required — the payment has to be removed before the invoice can be changed in *any* system (see [Changing a paid order](changing-a-paid-order.md)).
