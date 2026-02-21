---
layout: post
title: "How To Purchase a Premium Server"
category: Account
tags: Billing
permalink: falix/account/billing/purchasing-server
description: "Walk through the checkout process: choose resources, pick a billing plan, and complete payment."
keywords:
    - keyword: buy
      matches: ["server", "premium", "purchase", "checkout"]
    - keyword: purchase
      matches: ["server", "premium", "plan", "how"]
    - keyword: checkout
      matches: ["payment", "buy", "order", "complete"]
    - keyword: premium
      matches: ["buy", "get", "upgrade", "purchase"]
author: Lily
---

## Introduction
Ready to go premium? Purchasing a premium server on Falix gives you more resources, more game options, and a dedicated server that's yours to configure however you like. This guide walks you through the entire checkout process, from picking your resources to completing payment.

## What You'll Need
Before you start, make sure you have:
- A Falix account (sign up at [client.falixnodes.net](https://client.falixnodes.net/) if you don't have one)
- A payment method ready (credit/debit card or PayPal account)

## Step-by-Step Checkout

### 1. Start the Server Creation
1. Log in to the [Dashboard](https://client.falixnodes.net/).
2. Click [Create Server](https://client.falixnodes.net/create) in the navigation menu.
3. Select **Premium** as your server type.
4. Click **Continue**.

{: .info}
> If you already have a premium subscription, this step is skipped and you'll go straight to entering your server details.

### 2. Enter Server Details
Fill in your server's identity:
- **Server Name** -- how your server appears in the dashboard (3-20 characters).
- **Server Domain** -- the address players use to connect (1-20 characters, lowercase letters only). You can also choose a domain suffix from the dropdown.

Click **Continue** when you're ready.

### 3. Select the Game or Application
Choose the game you'd like to run. Premium servers unlock the full library of supported games and applications beyond Minecraft and Hytale. Browse the full list of available software [here](/falix/dashboard/setup/supported-software).

### 4. Configure Resources
This is where you decide how powerful your server will be:

| Resource | Range | Description |
|----------|-------|-------------|
| **RAM** | 1 - 32 GB | More RAM means more players and larger worlds |
| **CPU** | 1 - 8 cores | More cores means better performance under load |

Use the sliders or preset plans to select the right fit. The price updates in real time as you adjust.

### 5. Choose Your Server Location
Select the data center closest to you and your players for the best connection quality. Available locations are shown on a map or in a dropdown list.

### 6. Choose Your Billing Cycle
Choose how often you'd like to pay:

| Cycle | Discount |
|-------|----------|
| Monthly | No discount |
| 3 Months | **10% off** |
| 6 Months | **15% off** |
| 12 Months | **20% off** |

Longer cycles save you money. You can always change your cycle later from the [Billing Dashboard](https://client.falixnodes.net/billing/).

### 7. Enter Billing Details
Enter your billing location:
- **Country** -- select from the dropdown.
- **ZIP / Postal Code** -- enter your postal code.

Your country determines whether VAT is applied and at what rate. For more details, see [How To Manage Your Billing Details](falix/account/billing/billing-details).

### 8. Select Payment Gateway
Choose how you'd like to pay:

| Gateway | Description |
|---------|------------|
| **Revolut** | Pay by card through a popup window |
| **Stripe** | Pay by card on a hosted checkout page |
| **PayPal** | Pay using your PayPal account |

### 9. Review Your Order
Before paying, you'll see a summary of everything:
- Server resources (RAM and CPU)
- Server location
- Billing cycle
- Subtotal, VAT (if applicable), and total amount due

Double-check that everything looks right before proceeding.

### 10. Complete Payment
Click **Pay** to finalize your purchase. What happens next depends on your chosen gateway:

{% tabs gateway %}

{% tab gateway Revolut %}

A Revolut popup window will appear directly on the page.
1. Enter your card details in the popup.
2. Complete any 3D Secure verification if prompted by your bank.
3. The popup closes automatically once payment is confirmed.

{% endtab %}

{% tab gateway Stripe %}

You'll be redirected to a Stripe-hosted checkout page.
1. Enter your card details on the Stripe page.
2. Complete any 3D Secure verification if prompted.
3. After payment, you'll be redirected back to Falix automatically.

{% endtab %}

{% tab gateway PayPal %}

You'll be redirected to PayPal.
1. Log in to your PayPal account.
2. Review and approve the payment.
3. After approval, you'll be redirected back to Falix automatically.

{% endtab %}

{% endtabs %}

## After Payment

Once your payment is confirmed:
1. Your server begins provisioning automatically. This usually takes under a minute.
2. You'll be redirected to a success page confirming your purchase.
3. Your new server appears in the [Dashboard](https://client.falixnodes.net/) and on the [Billing Dashboard](https://client.falixnodes.net/billing/).
4. Your payment method is saved for future renewals -- you won't need to re-enter it each month.

{: .success}
> Your server is ready to use! Head to the [Dashboard](https://client.falixnodes.net/), click on your new server, and start it up from the console.

## Using Account Credits
If you have account credits (from downgrades, cycle switches, or other adjustments), they're applied automatically during checkout before your payment method is charged. If your credits cover the full amount, no charge is made to your card.

## Adding a Second Server
Already have a premium subscription? Adding another server is even faster:
1. Follow the same steps above to create a new server.
2. Since you already have a saved payment method, the charge is processed directly -- no need to go through the full checkout flow again.
3. The new server is added to your existing subscription and appears in your server list on the [Billing Dashboard](https://client.falixnodes.net/billing/).

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Payment was charged but no server appeared | Wait 5-10 minutes for provisioning. If it still doesn't show, see [I Did Not Receive My Service](falix/account/billing/service-not-received) |
| Payment was declined | Check with your bank or try a different payment method. See [How To Update Your Payment Method](falix/account/billing/update-payment-method) |
| Wrong resources or location | You can change resources from [Server Settings](https://client.falixnodes.net/server/settings) and transfer to a different location from the console |
| Checkout page won't load | Try disabling your ad blocker or switching browsers. Payment popups (Revolut) may be blocked by popup blockers |
