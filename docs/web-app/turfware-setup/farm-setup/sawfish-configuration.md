---
title: "Sawfish Configuration"
---

# Sawfish Configuration

Turfware connects to Sawfish — your accounting and payments system — so invoices, payments and clients stay in sync. This page is where that connection is set up. *(It replaces the old Xero integration.)*

!!! note "Set up your Sawfish account first"
    This page only links Turfware to Sawfish — it assumes your Sawfish account is already set up. For invoices, payments and syncing to work correctly, first complete your Sawfish setup: your organisation details, your accounting connection (Xero or MYOB), your payout account, and your invoice reminders. Work through the **[Sawfish setup checklist](https://help.sawfish.com.au/getting-started/setup-checklist/)**, or start from [Getting started](https://help.sawfish.com.au/) in the Sawfish help centre. Once Sawfish is set up, come back here to connect it to Turfware.

## Where to find it

Left-hand navigation → System Settings → Sawfish Configuration.

## Sawfish Integration

The connection uses three credentials, issued by Sawfish:

- Client ID
- API Key
- Webhook Key

Enter them and click Save, then Verify Sawfish Connection to confirm Turfware can talk to Sawfish.

!!! warning "Treat these like passwords"
    The Client ID, API Key and Webhook Key are credentials. Don't share them or screenshot this page — anyone with them can access your Sawfish account.

## How Sawfish sends invoices

Once Turfware is connected, **Sawfish sends your invoices** — not Xero and not Turfware. Knowing the rule avoids surprises for you and your customers.

### The sending rule

Sawfish emails an invoice as soon as it arrives from Turfware or Xero, and sweeps every hour for any it missed, whenever all four of these are true:

1. It is **approved** (status *Pending* in Sawfish — not a draft).
2. It has **not already been emailed**.
3. The customer has **Email notifications** switched on and an email address on their Sawfish record.
4. Its **issue date is today or earlier** — a future-dated invoice waits until its issue date.

There is no separate "send" step. Approving an invoice is the instruction to send it.

!!! info "This applies to invoices you create in Xero too"
    Sawfish sees every approved invoice for your business, including ones you raise directly in Xero that have nothing to do with turf. If it's approved and hasn't been emailed, Sawfish will send it.

Sending from Sawfish is what makes the rest of the flow work: the invoice carries the Sawfish payment link (card, PayID, Apple Pay, Google Pay), delivery and opens are tracked, and it enters the reminder and overdue follow-up. When the customer pays on any Sawfish rail, the invoice is marked paid immediately and the reminders stop.

### Drafts are never sent

Sawfish only sends **approved** invoices. A draft is never sent — from Turfware or from Xero (a Xero draft comes into Sawfish as a draft). To prepare an invoice for review, or hold one back — say a project the customer wants invoiced once at the end — leave it as a **draft**.

!!! warning "Reminders don't check whether the invoice was emailed"
    Once an invoice is approved, its overdue reminders go out on schedule whether or not the original invoice email was ever sent — so an approved invoice is always "live" to the customer. If you don't want them contacted, it needs to be a draft, or their notifications need to be off (below). The reminder schedule itself (for example *Invoice Overdue by 1 day / 10 days / 20 days*) is under Sawfish's **Settings → Invoice Notifications → Custom Notifications**, and the *Invoice approved and sent* message there goes by SMS as well as email if both are switched on.

### How approval happens from Turfware

- **Generate invoice** on an order gives you three choices: **Draft**, **Approve only**, or **Approve & send**. Draft is safe — nothing goes out. Approve only makes it *Pending*, so Sawfish emails it within the hour. Approve & send emails it straight away.
- **Approve** and **Send** on an existing invoice do the same two things respectively. Editing an invoice doesn't change whether it's approved.
- **Sending Invoice Automation** (see [Company Information](company-information.md#sending-invoice-automation)) sends the invoice for every confirmed order on its delivery date — **including one you left as a draft**, and without anyone approving it. If you use the automation, don't rely on "draft" to hold an invoice back on a confirmed order.

### Turning off emails and SMS for a customer

To stop Sawfish contacting a particular customer:

1. In Sawfish, open **Clients** and select the customer.
2. Open their **Client Details** tab and scroll to **Communication Settings**.
3. Switch off **Email notifications** and **SMS notifications**.

While these are off, Sawfish's automatic sending and its reminders skip that customer. Invoices still sync and payments still reconcile — only the outbound messages stop.

!!! note "Two things to know about the switch"
    - **It stays off until you turn it back on** — it isn't a one-off skip. To resume, go back to the customer's Communication Settings and switch it on.
    - **An explicit Send turns it back on.** If anyone clicks Send on an invoice — in Sawfish, or Send / Approve & send in Turfware, or the delivery-date automation runs — Sawfish switches that customer's Email notifications on again and sends. The switch protects against the automatic sender and reminders, not against a deliberate send.

If the toggles are greyed out, email or SMS is switched off for your whole business under Sawfish's **Settings → Invoice Settings**. (The per-event switches under **Settings → Invoice Notifications** — *Invoice approved and sent*, *Invoice paid*, *Statement* — control which messages go, not whether a customer is contacted at all.)

### Quick reference

| I want to… | Do this |
|---|---|
| Send an invoice to a customer | Approve it in Turfware or Xero. Sawfish sends it within the hour. |
| Prepare an invoice without sending it | Leave it as a draft — and make sure Sending Invoice Automation won't pick the order up on its delivery date. |
| Hold a customer's invoices until later | Leave them as drafts, or switch off their Email and SMS notifications in Sawfish. |
| Stop all Sawfish messages to one customer | Clients → the customer → Client Details → Communication Settings → switch off Email and SMS notifications. |
| Resume messages to that customer | Same place — switch them back on. |
| Fix an "Action Required: Unable to Send Invoice" email | The customer's Sawfish record has no email address. Add it, then send the invoice again — or, if it shouldn't go, switch off their notifications. |

### Common questions

**Why did Sawfish send an invoice I created in Xero?**
Because it was approved in Xero and hadn't been emailed — Sawfish sends every approved, unsent invoice it can see, wherever it was created. If it was meant to be a draft, check its status in Xero: a Xero draft would have stayed a draft in Sawfish.

**I got an "Action Required: Unable to Send Invoice" email. What happened?**
Sawfish tried to send an approved invoice but the customer's record had no email address — typically a customer created in Xero without one. Add the address under the customer's Client Details (or add a recipient on the invoice) and send it again. If you didn't intend it to go, switch off the customer's notifications instead. While you're there, check their payment terms: a customer with no terms set gets invoices that are due the day they're issued, so reminders start immediately.

**Will Sawfish send a draft I generate in Turfware for review?**
No — unless Sending Invoice Automation is on and the order is confirmed with a delivery date, in which case the automation sends it on that date regardless.

**I turned off a customer's emails last month. Do I need to do it again?**
No, it stays off — but note that a deliberate Send on one of their invoices switches it back on.

## Tap To Pay Devices

Turfware can take in-person payments — Tap to Pay, Apple Pay and Google Pay — on a registered device. Click Fetch devices to pull the devices registered against your Sawfish account, then set one as Primary with the star. (In-person Tap to Pay runs on the Sawfish mobile app.)

To register a device and take payments in person, follow [Tap to Pay on iPhone](https://help.sawfish.com.au/mobile/tap-to-pay/) in the Sawfish help centre — set it up there first, then Fetch devices here.

Before a Tap to Pay payment is pushed to the device, Turfware checks the customer is in sync with Sawfish. If the push fails, the message says why — most often the customer's details differ between the two systems; check the ⓘ sync state on the [customer's summary](../../customers/customer-summary.md#open-the-customer-in-sawfish).
