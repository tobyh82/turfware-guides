---
title: Thanks
hide:
  - navigation
  - toc
search:
  exclude: true
---

# Thanks, that helps.

We'll be in touch to hear a bit more about how it works at your place.

<div id="tw-guide" class="tw-guide" style="display:none;margin:1.6em 0;padding:1.2em 1.4em;border-left:4px solid #169c19;background:#f0f6f1;border-radius:4px">
<p style="margin:0 0 .3em 0;font-size:.75em;letter-spacing:.08em;text-transform:uppercase;color:#175749">While you're here</p>
<p id="tw-guide-title" style="margin:0 0 .3em 0;font-size:1.15em;font-weight:bold;color:#175749"></p>
<p id="tw-guide-sub" style="margin:0 0 .9em 0"></p>
<a id="tw-guide-link" class="md-button md-button--primary" href="#" download>Download the two-page guide (PDF)</a>
</div>

<div id="tw-guide-all" style="display:none;margin:1.6em 0">
<p><strong>Two-page guides to how Turfware works:</strong></p>
<ul id="tw-guide-list"></ul>
</div>

If you'd rather pick a time now, grab half an hour here:

[Book a 30-minute demo](https://calendly.com/turfware-sales/new-meeting){ .md-button }

Toby<br>
*Great things happen on Grass.*

<script>
(function () {
  var G = {"1": {"t": "Turfware at a glance", "s": "One system for orders, harvest, delivery and invoicing, built on a turf farm.", "f": "turfware-guide-1-turfware-at-a-glance.pdf"}, "2": {"t": "The digital cut sheet and the Harvesting App", "s": "How an order in the office becomes the crew's cut list, and how the office sees the cutting as it happens.", "f": "turfware-guide-2-harvest-app-and-cut-sheet.pdf"}, "3": {"t": "Delivery and proof of delivery", "s": "Truck runs on one screen, the driver's day on their phone, and a photo and signature against every drop.", "f": "turfware-guide-3-delivery-and-proof-of-delivery.pdf"}, "4": {"t": "Orders in, customers kept informed", "s": "However the order arrives, it lands in one place, and the customer hears from you at every step.", "f": "turfware-guide-4-orders-and-customer-updates.pdf"}, "5": {"t": "Pricing and freight, set once", "s": "Turf, segments, volume breaks, freight by postcode and customer deals, applied on every order.", "f": "turfware-guide-5-pricing-and-freight.pdf"}, "6": {"t": "Credit control and user access", "s": "See a customer's account before the turf's cut, and give every user exactly the access they need.", "f": "turfware-guide-6-credit-control-and-access.pdf"}, "7": {"t": "Invoicing, payments and reporting", "s": "The invoice comes off the order, payments come back on their own, and the numbers are there when you want them.", "f": "turfware-guide-7-invoicing-payments-reporting.pdf"}};
  var base = "/assets/guides/";
  var e = new URLSearchParams(window.location.search).get("e");
  var g = G[e];
  if (g) {
    document.getElementById("tw-guide-title").textContent = g.t;
    document.getElementById("tw-guide-sub").textContent = g.s;
    document.getElementById("tw-guide-link").href = base + g.f;
    document.getElementById("tw-guide").style.display = "block";
  } else {
    var ul = document.getElementById("tw-guide-list");
    Object.keys(G).forEach(function (k) {
      var li = document.createElement("li"), a = document.createElement("a");
      a.href = base + G[k].f; a.textContent = G[k].t; li.appendChild(a); ul.appendChild(li);
    });
    document.getElementById("tw-guide-all").style.display = "block";
  }
})();
</script>
