---
layout: post
title: "Understanding Billing & Pricing"
category: Account
tags: Billing
permalink: falix/account/billing/understanding-billing
description: "How pricing, billing cycles, VAT, and proration work on Falix."
keywords:
    - keyword: billing
      matches: ["how", "works", "explained", "pricing"]
    - keyword: price
      matches: ["how", "calculated", "cost", "much"]
    - keyword: vat
      matches: ["tax", "exempt", "reverse charge", "business"]
    - keyword: proration
      matches: ["prorated", "pro-rata", "partial", "credit"]
author: Lily
---

## Introduction
This article explains how pricing, billing cycles, VAT, and proration work on Falix.

## How Pricing Works

Server pricing is based on two factors:

| Resource | Billed Per |
|----------|-----------|
| RAM | Per GB per month |
| CPU | Per core per month |

Your monthly price is calculated as:

**Monthly Price = (RAM in GB × price per GB) + (CPU cores × price per core)**

## Billing Cycles & Discounts

Longer billing cycles offer discounts on your monthly rate:

| Cycle | Discount | You Pay |
|-------|----------|---------|
| Monthly | — | Full price each month |
| 3 Months | 10% off | 3 months upfront at reduced rate |
| 6 Months | 15% off | 6 months upfront at reduced rate |
| 12 Months | 20% off | 12 months upfront at reduced rate |

Your billing day is fixed (capped at the 28th of the month) and stays the same across renewals.

{: .info}
> You can change your billing cycle at any time from the [Billing Dashboard](https://client.falixnodes.net/billing/). See our [Change Billing Cycle](falix/account/billing/change-billing-cycle) article for details.

## VAT

VAT (Value Added Tax) may be applied depending on your location:

{% tabs vat %}

{% tab vat EU Customers %}

If you're located in the EU, VAT is charged at your country's rate (e.g. 19% for Germany, 21% for Latvia).

**EU businesses** with a verified VAT number are exempt from VAT under the reverse charge mechanism. To claim this:
1. Go to the [Billing Dashboard](https://client.falixnodes.net/billing/).
2. Open the **Billing Info** section.
3. Enter your VAT number (e.g. DE123456789).
4. The system will verify it automatically against the EU VIES database.
5. Once verified, future charges will be VAT-exempt and invoices will show a reverse charge notice.

{: .info}
> Businesses in Latvia (the seller's country) are always charged VAT regardless of VAT registration.

{% endtab %}

{% tab vat Non-EU Customers %}

If you're located outside the EU, VAT is not applied. Your invoices will show a "VAT Not Applicable" notice.

{% endtab %}

{% endtabs %}

## Proration

Proration ensures you only pay for what you use when making changes mid-cycle.

**Upgrades:** When you upgrade resources or switch to a longer cycle, you're charged a prorated amount for the remaining days in your current billing period. Your existing unused time is credited toward the new charge.

**Downgrades:** When you downgrade resources or switch to a shorter cycle, the unused portion of your current billing period is credited to your account balance and applied to future charges.

**Cancellations:** When you cancel a server, it stays active until the end of the current billing period. No partial refund is issued, but you keep access for the remaining time.

## Account Credits

Credits accumulate from downgrades, cycle switches, and other adjustments. They are applied automatically to your next charge before your payment method is billed. If your credits cover the full amount, no charge is made.

## Payment Methods

Three payment gateways are supported:

| Gateway | Type |
|---------|------|
| Revolut | Card payments |
| Stripe | Card payments |
| PayPal | PayPal balance or linked cards |

You can switch between gateways at any time. See our [Update Payment Method](falix/account/billing/update-payment-method) article for details.

To set up your billing country and VAT number, see [How To Manage Your Billing Details](falix/account/billing/billing-details).
