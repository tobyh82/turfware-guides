---
title: Payments & Accounting
---

# Payments & Accounting

Turfware doesn't keep your books — it works alongside two other systems. Understanding how the three connect explains **where** a payment or invoice lives, **why** a change can take a few minutes to appear, and **how** to handle payments, order changes and refunds cleanly.

## The three systems

- **Turfware** — your **operational** system: orders, harvest, delivery, and the operational order status.
- **Sawfish** — the **invoicing & payments hub**: it generates the invoice, takes customer payments (card, PayTo, PayID), and sits between Turfware and your accounting system.
- **Your accounting system** — **MYOB** (or Xero): your **books**, and the source of truth for the invoice and its payments.

## How they connect

- **Turfware ↔ Sawfish** — **near real-time**. Changes cross by webhook, usually within about a minute.
- **Sawfish ↔ your accounting system** — a **timed sync**, roughly every **15 minutes**. A change made in MYOB can take up to ~15 minutes to appear in Sawfish and then Turfware. There is **no "sync now" button**.

## In this section

- [How the sync works](how-the-sync-works.md) — the direction and timing of every sync.
- [Recording payments](recording-payments.md) — Sawfish payment methods, and manual (off-rails) payments.
- [Changing a paid order](changing-a-paid-order.md) — amending or increasing an order after it's invoiced or paid.
- [Refunds & credits](refunds-and-credits.md) — the recommended refund process.
