---
title: "How to use the routing Feature"
---

# How to use the routing Feature

Routing is where you build each carrier's truck runs for a day and let Turfware map the route.

## Open Routing

Switch to the blue Routing button (top left) to open the Routing Management page. Pick the date, then tick the carrier(s) you're routing (Turfware Trucking, Bobs Trucking, and so on).

## Assign orders to trucks

- The Unassigned column (left) lists every order for that date and carrier that isn't yet on a truck.
- Click Add Truck to add a truck run — choose the truck and driver.
- Drag an order from Unassigned onto a truck to assign it, and set each drop's ETD as needed.

![Routing — unassigned orders ready to allocate to trucks](../../../assets/routing1.png)

## Route and save

- Once orders are on a truck, Turfware calculates the run and shows the route on the map (each stop lettered A, B, C…). Each truck shows its Run number and the Capacity used.
- Click Save to save the trucks and generate the docket.
- Click CSV (next to Add Truck) to export the deliveries as a CSV file.

![Routing — orders allocated to a truck, with the calculated route](../../../assets/routing2.png)

## Tell customers their delivery window

Once a truck's run is set, open the arrow next to that truck's **Save** button and click **Send Confirmation**. Every customer with an order on that truck gets the *Delivery Confirmation* email (and SMS to the site contact, if switched on), telling them the window their turf is due in. It isn't sent automatically — this click is what sends it.

- The window is the drop's ETD with your buffers either side, set under Company Information → [Notifications](../../turfware-setup/farm-setup/company-information.md#notifications) (for example *5–9am* for a 7:00am drop with a 2-hour buffer).
- After sending, the item reads **Resend Confirmation** — use it if the run changes.
- The same menu has **Generate Docket**.
- Edit the wording under [Notifications](../../notifications/index.md#orders) → *Delivery Confirmation*.
