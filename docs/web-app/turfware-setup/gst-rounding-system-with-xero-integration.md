---
title: "GST Rounding System with Xero Integration"
---

# GST Rounding System with Xero Integration

### **Overview**

The GST rounding system ensures that all pricing in the system is handled with 4 decimal places for precision, but totals are displayed rounded to 2 decimal places. This system applies to various areas such as turf, products, services, laying, installation, and freight.

### **Key Points:**

**Precision for Unit Prices:**

- Users can enter unit prices with 4 decimal places across the system (e.g., $/unit for turf, products, services, etc.).
- The system allows input like `0.1234` for all pricing fields to provide precise calculations.

**Calculation Precision:**

- Calculations for totals (e.g., subtotal, GST, total price, grand total) are done with 4 decimal places internally.
- Example: A rate of `123.4567` multiplied by a quantity will maintain the 4-decimal precision throughout internal calculations.

**Display Rounding:**

- Despite the internal calculations using 4 decimals, all displayed totals will be rounded to 2 decimal places for clarity.
- Subtotals, GST, total pricing, and grand total are all rounded up to 2 decimal places.
- Example: A subtotal calculated as `123.4567` would display as `123.46`.

**Xero Integration:**

- The system pushes all front-end data to Xero exactly as entered, maintaining the 4-decimal precision.
- Once in Xero, calculations are also done with 2 decimal places, ensuring consistency between the system and Xero.

#### 

### **Application:**

- **Turf Pricing**
- **Products**
- **Services**
- **Laying & Installation**
- **Freight**

In all these areas, the user is able to input and work with prices at a higher precision (4 decimals), while the system ensures totals appear in standard 2-decimal format, in line with common accounting practices.

This approach balances precision for detailed entries while maintaining readability and compliance with Xero's rounding system for final totals

---

*Originally published 2024-10-17 · migrated from HelpJuice for this preview.*
