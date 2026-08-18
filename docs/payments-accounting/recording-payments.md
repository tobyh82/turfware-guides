---
title: "Recording payments"
---

# Recording payments

A payment reaches an order one of two ways: **through Sawfish** (on the digital invoice) or **off-rails** (recorded manually).

## Payments through Sawfish

Customers can pay their **digital invoice** through Sawfish by:

- **Credit / debit card**
- **PayTo**
- **PayID**

All three run through Sawfish's payment provider (**Zai**), and each is **enabled per account** — so which methods your customers see depends on your Sawfish account setup. A payment taken this way flows automatically: Sawfish marks the invoice paid, Turfware shows the order paid within ~1 minute, and Sawfish posts the payment to your accounting system on the next sync.

## Manual (off-rails) payments

Use **Received Payment (manual)** when a customer pays **outside Sawfish** — for example **cash** or an **EFTPOS / merchant terminal**. It **marks the Turfware order as paid** so the order can keep moving through the workflow.

When you record a manual payment, complete the **popup** with the payment details (method, date, reference and any notes). Turfware then:

- **emails the record to your accounts email** (set in [Company Information](../web-app/turfware-setup/farm-setup/company-information.md)), and
- **saves it to the order's Documents** tab.

!!! warning "The money still has to be reconciled"
    A manual payment is an **operational record** — it tells Turfware the order is paid so work can continue. The **actual money must still be reconciled in your accounting system** by your bookkeeper (cash till balanced, merchant / terminal statement, etc.). This is deliberate: it gives you **two layers of control** on payments taken outside the normal Sawfish rails.
