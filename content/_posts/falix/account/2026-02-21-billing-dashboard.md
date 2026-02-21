---
layout: post
title: "Navigating the Billing Dashboard"
category: Account
tags: Billing
permalink: falix/account/billing/billing-dashboard
description: "A tour of the billing dashboard: your subscription summary, server list, payment method, and invoices."
keywords:
    - keyword: billing
      matches: ["dashboard", "page", "overview", "navigate"]
    - keyword: dashboard
      matches: ["billing", "subscription", "manage", "where"]
    - keyword: subscription
      matches: ["view", "manage", "status", "details"]
author: Lily
---

## Introduction
The [Billing Dashboard](https://client.falixnodes.net/billing/) is your central hub for managing everything related to payments, servers, and invoices. This guide walks you through each section of the page so you know exactly where to find what you need.

## Getting There
1. Log in to the [Falix Client Area](https://client.falixnodes.net/).
2. Click **Billing** in the navigation bar.

You'll land on the billing dashboard, which is organized into several sections from top to bottom.

## Summary Bar
At the top of the dashboard, you'll see a row of stat cards that give you a quick snapshot of your billing status:

| Card | What It Shows |
|------|---------------|
| **Next Billing** | The date of your next scheduled renewal payment |
| **Credit Balance** | Any account credits you have available (from downgrades, cycle switches, or other adjustments) |
| **Monthly Spend** | Your current total monthly cost across all servers |
| **Status** | Only appears when your subscription needs attention -- shows **Past Due**, **Suspended**, or **Cancelled** |

## Alerts and Banners
Depending on your account state, you may see colored banners below the summary bar. Each one tells you something important and gives you a quick action to resolve it:

### Payment Failed (Red)
Your renewal payment could not be processed. You'll see the reason and how many retry attempts have been made.
- Click **Update Card**{: .blue } to change your payment method.
- Click **Retry Payment**{: .green } to attempt the charge again.

For full details, see [My Payment Failed](falix/account/billing/payment-failed).

### Servers Suspended or Cancelled (Red)
Your servers have been taken offline due to non-payment.
- Click **Renew Servers**{: .green } to select which servers to reactivate and process payment.

### Cancellation Notice (Yellow)
One or more servers are scheduled for cancellation at the end of the current billing period. The banner shows how many servers are affected and the cancellation date. You can undo this from the server list below.

## Payment Method
On the left side of the two-column section, the **Payment Method** card displays your saved payment information:
- Your current card brand, last 4 digits, and expiry date (or PayPal email if using PayPal).
- Gateway selector buttons to switch between **Revolut**, **Stripe**, and **PayPal**.
- An **Update Card**{: .blue } button to add or change your card details.

To learn how to update or switch your payment method, see [How To Update Your Payment Method](falix/account/billing/update-payment-method).

## Billing Details
On the right side, the **Billing Details** card shows your billing and tax information:
- Your **country** and **ZIP code**.
- The **VAT rate** applied to your charges (based on your country).
- Your **company name** and **VAT number** if you've added business details, along with a verification badge.

Click **Edit**{: .blue } to update your location or add business details for VAT exemption. For a full walkthrough, see [How To Manage Your Billing Details](falix/account/billing/billing-details).

## My Servers
The server list shows every premium server on your account. Each server card displays:

| Field | Description |
|-------|-------------|
| **Server Name** | Your server's identifier |
| **Resources** | RAM (in GB) and CPU cores allocated |
| **Price** | Current price per billing cycle |
| **Billing Cycle** | Monthly, 3 Months, 6 Months, or 12 Months |
| **Renewal Date** | When the next charge is due (or cancellation date if cancelling) |
| **Status** | Active, Cancelling, Suspended, or Cancelled |

### Per-Server Actions
Each server has action buttons depending on its current state:

| Action | When Available | What It Does |
|--------|---------------|-------------|
| **Change Cycle** | Active monthly servers | Switch between billing cycles (1, 3, 6, or 12 months). See [How To Change Your Billing Cycle](falix/account/billing/change-billing-cycle) |
| **Cancel Server** | Active servers | Schedules the server for cancellation at the end of the billing period. See [How To Cancel a Service](falix/account/billing/cancel-service) |
| **Undo Cancellation** | Cancelling servers | Reverses a pending cancellation and returns the server to active billing |

## Invoices
At the bottom of the dashboard, the **Invoices** section lists your 10 most recent invoices and credit notes. Each entry shows:
- **Invoice number** (e.g. INV-2025-000042 or CN-2025-000015 for credit notes)
- **Issue date**
- **Amount**
- **Status badge** (Paid, Credit Issued, Refunded, or Partial Refund)
- A **View** button to open the full invoice

For details on reading and downloading invoices, see [Understanding Your Invoice](falix/account/billing/understanding-invoices).

## Renewing After Cancellation
If your subscription has been cancelled (due to non-payment or because all servers were cancelled), a **Renew Servers**{: .green } button appears. Clicking it opens a modal where you can:
1. Select which cancelled servers to reactivate.
2. Review the total cost including VAT.
3. Choose your payment method.
4. Complete payment to bring your servers back online.

## Related Articles
- [How To Purchase a Premium Server](falix/account/billing/purchasing-server)
- [Understanding Billing & Pricing](falix/account/billing/understanding-billing)
- [My Payment Failed](falix/account/billing/payment-failed)
- [How To Update Your Payment Method](falix/account/billing/update-payment-method)
- [How To Manage Your Billing Details](falix/account/billing/billing-details)
- [How To Change Your Billing Cycle](falix/account/billing/change-billing-cycle)
- [How To Cancel a Service](falix/account/billing/cancel-service)
- [Understanding Your Invoice](falix/account/billing/understanding-invoices)
- [Refund Policy & How To Request a Refund](falix/account/billing/refund-policy)
