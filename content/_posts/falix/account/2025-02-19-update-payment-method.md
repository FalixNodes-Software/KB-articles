---
layout: post
title: "How To Update Your Payment Method"
category: Account
tags: Billing
permalink: falix/account/billing/update-payment-method
description: "Change your card details or switch between Revolut, Stripe, and PayPal."
keywords:
    - keyword: payment
      matches: ["method", "card", "update", "change"]
    - keyword: card
      matches: ["expired", "update", "change", "new", "add"]
    - keyword: paypal
      matches: ["switch", "change", "add", "connect"]
author: Lily
---

## Introduction
You can update your payment method or switch between payment gateways at any time from the billing dashboard. This is useful when your card has expired, been declined, or you want to use a different payment provider.

## Supported Payment Methods

| Gateway | Type | Details |
|---------|------|---------|
| Revolut | Card | Visa, Mastercard, and other major cards via Revolut |
| Stripe | Card | Visa, Mastercard, Amex, and other major cards via Stripe |
| PayPal | PayPal | Pay using your PayPal account balance or linked cards |

## How to Update Your Payment Method

1. Log in to the [Falix Client Area](https://client.falixnodes.net/).
2. Navigate to the [Billing Dashboard](https://client.falixnodes.net/billing/).
3. Scroll to the **Payment Method** section. You'll see your current payment method displayed (card brand and last 4 digits, or PayPal email).
4. To update your card on the same gateway, click **Update Card**.
5. To switch to a different gateway, click the gateway button (Revolut, Stripe, or PayPal), then click the update button.

## Gateway-Specific Flows

{% tabs gateway %}

{% tab gateway Revolut %}

1. Click **Update Card** (or select Revolut from the gateway buttons).
2. A Revolut popup window will appear.
3. Enter your new card details in the popup.
4. Once complete, the popup closes and your new card is saved.

{: .info}
> Revolut processes a small authorization charge to verify your card. This is not a real charge and will be released automatically.

{% endtab %}

{% tab gateway Stripe %}

1. Click **Update Card** (or select Stripe from the gateway buttons).
2. You will be redirected to a Stripe checkout page.
3. Enter your new card details.
4. After submitting, you will be redirected back to the billing dashboard.

{% endtab %}

{% tab gateway PayPal %}

1. Click **Update Card** (or select PayPal from the gateway buttons).
2. You will be redirected to PayPal to authorize the billing agreement.
3. Log in to your PayPal account and approve the setup.
4. After approval, you will be redirected back to the billing dashboard.
5. The setup is confirmed automatically in the background.

{% endtab %}

{% endtabs %}

## After Updating
- Your new payment method will be used for all future charges
- If you have a failed payment, you can now retry it with the updated method from the [Billing Dashboard](https://client.falixnodes.net/billing/)
- Your current card details (brand, last 4 digits, expiry) or PayPal email will be displayed in the payment method section
