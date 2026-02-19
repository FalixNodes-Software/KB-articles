---
layout: post
title: "How To Change Your Billing Cycle"
category: Account
tags: Billing
permalink: falix/account/billing/change-billing-cycle
description: "Switch between monthly, quarterly, and annual billing cycles to save money."
keywords:
    - keyword: billing
      matches: ["cycle", "period", "frequency", "interval"]
    - keyword: cycle
      matches: ["change", "switch", "monthly", "annual", "quarterly"]
author: Lily
---

## Introduction
You can change your billing cycle at any time to take advantage of longer-term discounts. Switching to a longer cycle reduces your monthly cost, and any unused time on your current cycle is credited automatically.

## Available Billing Cycles

| Cycle | Discount | Description |
|-------|----------|-------------|
| Monthly | No discount | Pay month-to-month |
| 3 Months | **10% off** | Billed every 3 months |
| 6 Months | **15% off** | Billed every 6 months |
| 12 Months | **20% off** | Billed annually |

## How to Change Your Billing Cycle

1. Log in to the [Falix Client Area](https://client.falixnodes.net/).
2. Navigate to the [Billing Dashboard](https://client.falixnodes.net/billing/).
3. Find the server you want to change and click the **Change Cycle** button.
4. A modal will appear with the four cycle options. Select your preferred cycle.
5. The system will calculate a preview showing:
   - **Credit from current cycle** — the unused portion of your current billing period (shown in green)
   - **New cycle cost** — the total price for the new cycle with discount applied
   - **Amount due** — the difference you need to pay, or a credit applied to your account
6. Click **Confirm Change** to proceed.

## How Pricing Works

{% tabs pricing %}

{% tab pricing Upgrading to Longer Cycle %}

When switching to a longer cycle (e.g. monthly to annual), you receive a pro-rata credit for the unused days on your current cycle. This credit is subtracted from the cost of the new cycle.

**Example:**
- Current plan: $6.00/month, 20 days remaining
- Switching to: 12-month cycle (20% discount)
- Credit from current cycle: ~$4.00
- New 12-month cost: $57.60 ($4.80/month after discount)
- **Amount due: $53.60**

If the amount due is greater than $0, payment will be processed through your current payment method. If you have account credits, they will be applied first.

{% endtab %}

{% tab pricing Downgrading to Shorter Cycle %}

When switching to a shorter cycle (e.g. annual to monthly), the unused portion of your current cycle is credited to your account balance.

**Example:**
- Current plan: 12-month cycle, 8 months remaining
- Switching to: monthly cycle
- Credit from unused months applied to your account
- New monthly charge starts at the next billing date

{: .info}
> Downgrade credits are applied to your account balance and will be used automatically on future charges.

{% endtab %}

{% endtabs %}

## After Changing Your Cycle
- Your new billing cycle takes effect immediately
- Your next billing date is recalculated based on the new cycle length
- Your server resources remain unchanged — only the billing period and price change
- The discount is applied to every renewal going forward

{: .warning}
> Billing cycle changes are not available for hourly servers.
