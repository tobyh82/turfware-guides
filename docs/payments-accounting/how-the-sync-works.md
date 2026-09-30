---
title: "How the sync works"
---

# How the sync works

## Turfware ↔ Sawfish — near real-time

Turfware and Sawfish talk to each other by webhook, so changes cross within about a minute. When Sawfish records a payment or updates an invoice, the Turfware order reflects it almost immediately — amount paid, amount due, and paid status.

## Sawfish ↔ your accounting system — a timed sync (~15 minutes)

Sawfish syncs with your accounting system (MYOB or Xero) on a timed pull, roughly every 15 minutes. So a change made in your accounting system — a payment, or an invoice amendment — is picked up on the next sync, anywhere from 0 to about 15 minutes later, and then flows on to Turfware.

This interval is fixed — there's no staff button to force this transaction sync sooner or to change its frequency. If you need a change to reach the customer's invoice quickly, make it on the Turfware / Sawfish side (near real-time) rather than in your accounting system.

!!! tip "The Sync now button"
    Sawfish has a Sync now button — Settings → Invoice Settings — that pulls your latest account assets (chart of accounts, items and tax codes) from your accounting system on demand, up to 10 times a day (it shows the attempts remaining). Use it after you add a new account code or item in MYOB/Xero so it's available in Sawfish straight away. It refreshes the accounting structure — it doesn't re-pull invoices or payments, which stay on the timed sync above.

    For the full detail, see [How invoice sync works](https://help.sawfish.com.au/invoicing/) in the Sawfish help centre.

## Customer details — Sawfish is the hub

Customer details (name, business name, email, phone, ABN, address) are kept in step across Turfware, Sawfish and your accounting system, with Sawfish in the middle. Turfware talks to Sawfish; Sawfish talks to Xero or MYOB. Turfware no longer writes customer details to your accounting system directly.

- **Edit a customer in Turfware** — the change is pushed to Sawfish the moment you save, and Sawfish passes it on to your accounting system. If Sawfish rejects the details — for example the email already belongs to another customer — the save doesn't go through and the message tells you which customer is using them.
- **Edit a customer in Sawfish or your accounting system** — the change flows back to Turfware within about a minute.
- **The latest change wins.** Whichever system was edited most recently is the one that sticks. Two exceptions are recorded rather than applied: an email coming from Sawfish that's already used by a different Turfware customer is kept as it was, and a customer's ABN is locked to Sawfish once a CreditGuard credit check or monitor exists for them.
- **See the sync state on the customer.** On the customer's summary, an ⓘ next to the Sawfish Client link shows when they last synced, and any sync error or conflict with its time (see [Customer summary](../web-app/customers/customer-summary.md#open-the-customer-in-sawfish)).

## What updates what

| You do this… | …and this happens |
|---|---|
| Take a payment in Sawfish (card, PayTo, PayID, Tap to Pay, Apple/Google Pay) | Turfware shows the order paid within ~1 min; Sawfish posts the payment to your accounting system on the next sync |
| Record a manual (off-rails) payment in Turfware | Marks the Sawfish invoice paid — which stops the payment-reminder emails — but your accounting system is not updated; the money is reconciled there manually |
| Record a payment in your accounting system (MYOB / Xero) | Flows accounting → Sawfish → Turfware on the next ~15-min sync |
| Edit a customer's details in Turfware | Pushed to Sawfish on save, then on to your accounting system; a rejection stops the save and shows why |
| Edit a customer's details in Sawfish or your accounting system | Flows back to Turfware within ~1 min; latest change wins |
| Amend an unpaid invoice in Turfware | Flows automatically to Sawfish and your accounting system |
| Amend a paid invoice in your accounting system | Flows to Sawfish, but not back to the physical Turfware order — you must manually amend it in Turfware to match |

!!! warning "Amend before payment; intervene after"
    Invoices flow Turfware → Sawfish → your accounting system automatically, up until a payment is applied. Once a payment is on the invoice, manual intervention is required — the payment has to be removed before the invoice can be changed in *any* system (see [Changing a paid order](changing-a-paid-order.md)).
