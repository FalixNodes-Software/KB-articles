---
layout: post
title: "My Payment Failed"
category: Account
tags: Billing
permalink: falix/account/billing/payment-failed
description: "What happens when a payment fails and how to resolve it."
keywords:
    - keyword: payment
      matches: ["failed", "declined", "rejected", "error"]
    - keyword: billing
      matches: ["failed", "past due", "overdue"]
    - keyword: server
      matches: ["suspended", "offline", "stopped"]
    - keyword: card
      matches: ["declined", "expired", "invalid"]
    - keyword: renew
      matches: ["subscription", "servers", "reactivate"]
author: Lily
---

## Introduction
If your payment fails during a billing renewal, your subscription will enter a recovery state. This guide explains what happens at each stage and what you can do to resolve it.

## What Happens When a Payment Fails

When a scheduled renewal charge fails, your subscription goes through the following stages:

### Stage 1: Past Due
Your subscription is marked as **Past Due** immediately after a failed charge.

- A red **Payment Failed** banner appears on your [Billing Dashboard](https://client.falixnodes.net/billing/) showing the number of failed attempts
- **Your servers keep running** during this stage
- You will receive an email notification with the reason for the failure (e.g. insufficient funds, expired card)

### Stage 2: Suspended
If the payment remains unresolved, your subscription will be escalated to **Suspended**.

- Your servers are **taken offline** and will no longer be accessible
- A red **Suspended** badge appears on your billing dashboard
- Your server data is still preserved at this stage

### Stage 3: Cancelled
If the payment is still not resolved after suspension, your subscription will be **Cancelled**.

- Your servers are marked as cancelled
- You will need to go through the renewal process to reactivate them

{: .warning}
> Act quickly when you see a payment failure notice. The sooner you resolve it, the less disruption to your servers.

## How to Fix a Failed Payment

{% tabs fix %}

{% tab fix Retry Payment %}

If your subscription is **Past Due** or **Suspended**, you can retry the payment immediately:

1. Go to the [Billing Dashboard](https://client.falixnodes.net/billing/).
2. Click the **Retry Payment** button on the red banner.
3. The system will attempt to charge your current payment method.
4. If successful, your subscription returns to **Active** and any suspended servers will be brought back online automatically.

{: .info}
> There is a 5-minute cooldown between retry attempts.

{% endtab %}

{% tab fix Update Payment Method %}

If your card has expired or been declined, update it before retrying:

1. Go to the [Billing Dashboard](https://client.falixnodes.net/billing/).
2. Click the **Update Card** button on the red banner, or scroll to the payment method section.
3. Select your preferred payment gateway (Revolut, Stripe, or PayPal).
4. Follow the prompts to add or update your card details.
5. Once updated, click **Retry Payment** to process the charge with your new payment method.

{% endtab %}

{% tab fix Renew After Cancellation %}

If your subscription has been cancelled due to non-payment, you can still reactivate your servers:

1. Go to the [Billing Dashboard](https://client.falixnodes.net/billing/).
2. Click the **Renew Servers** button.
3. Select which servers you want to reactivate.
4. Review the total cost (including VAT if applicable).
5. Complete the payment through your chosen payment method.
6. Your servers will be brought back online and your subscription will return to **Active**.

{: .warning}
> Renewal is only possible while your server data still exists. If your servers have been permanently deleted, they cannot be recovered.

{% endtab %}

{% endtabs %}

## Common Failure Reasons

| Reason | What to Do |
|--------|-----------|
| Insufficient funds | Add funds to your bank account, then retry |
| Card expired | Update your payment method with a new card |
| Card declined | Contact your bank to authorize the charge, or try a different card |
| PayPal issue | Check your PayPal account for holds or restrictions |

## Account Credits
If you have account credits (from downgrades or prorated refunds), they will be applied automatically when retrying or renewing. If your credits cover the full amount, no charge will be made to your payment method.

## Still Not Working?
Payment failures are handled between you and your bank or payment provider. If retrying and updating your payment method doesn't work, contact your bank to check for holds or blocks on the transaction, or try a different payment method entirely.
