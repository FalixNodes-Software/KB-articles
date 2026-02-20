---
layout: post
title: "How To Change Server Resources"
tags: Setup
permalink: falix/dashboard/setup/change-resources
description: "Learn how to allocate and change your server's CPU, memory, and disk resources."
keywords:
    - keyword: resources
      matches: ["change", "allocate", "upgrade", "adjust"]
    - keyword: server
      matches: ["cpu", "memory", "ram", "disk", "storage"]
    - keyword: settings
      matches: ["configuration", "allocation"]
    - keyword: plan
      matches: ["upgrade", "downgrade", "change", "switch"]
author: Lily
---

## Introduction
This guide covers how to change your server's resources. The process differs depending on whether your server is on the **new billing system** or a **legacy premium plan**.

{: .info}
> Changing resources requires a server restart to take effect. Your server may experience brief downtime during the restart.

## Changing Resources

{% tabs resources %}

{% tab resources New Billing %}

If you purchased your server through the [Billing Dashboard](https://client.falixnodes.net/billing/), follow these steps.

### Steps
1. Log in to the [Dashboard](https://client.falixnodes.net/).
2. Navigate to your server and go to **Settings**.
3. Select the **Operations** tab.
4. Click the **Change Plan** button.
5. A modal will appear with two ways to select your new resources:

### Preset Plans

| Plan | RAM | CPU |
|------|-----|-----|
| Starter | 4 GB | 2 cores |
| Friends | 6 GB | 3 cores |
| Community | 8 GB | 4 cores |
| Network | 12 GB | 5 cores |

### Custom Configuration
Use the sliders to set your own values:
- **RAM**: 512 MB to 32 GB (in 512 MB increments)
- **CPU**: 1 to 8 cores

### Pricing
The modal shows a real-time pricing breakdown as you adjust resources, including:
- Your current plan cost
- The new plan cost
- Pro-rata charges or credits for the remaining billing period
- VAT (if applicable)

**Upgrades**: You will be charged the pro-rata difference for the remaining billing period. If you have account credits, they will be applied automatically. Otherwise, payment will be processed through your payment method (Revolut, Stripe, or PayPal).

**Downgrades**: A credit for the price difference will be applied to your account automatically.

6. Click **Pay & Apply Upgrade** (for upgrades) or **Apply Downgrade** (for downgrades).
7. Restart your server for the changes to take effect.

{% endtab %}

{% tab resources Legacy Premium %}

> This section is for Premium customers managing servers purchased through the legacy billing system.

### Steps
1. Log in to the [Dashboard](https://client.falixnodes.net/).
2. Navigate to your server and go to **Settings**.
3. Select the **Operations** tab.
4. Click the **Change Resources** button.
5. A modal will appear with the following fields:

| Resource | Details |
|----------|---------|
| CPU | Enter desired allocation. 1 = 100% of one core. Minimum: 0.25 |
| Memory | Enter desired memory in MB. Minimum: 128 MB. Example: 2048 for 2 GB |
| Disk | Premium plans include unmetered disk space |

6. Click **Save Changes**.
7. Restart your server for the changes to take effect.

{: .warning}
> Resource changes are limited by your plan. You cannot allocate more CPU or RAM than your plan allows.

{% endtab %}

{% endtabs %}

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Server won't start | Verify you've allocated sufficient CPU and memory for your server software |
| Resources not showing | Try refreshing the page or logging out and back in |
| Changes not applied | Ensure you restarted your server after making changes |

{: .warning}
> If your server fails to start after changing resources, make sure you've allocated enough CPU and memory for your server software to run properly.

## Need Help?
If you're having trouble changing your server resources, please contact our [support team](https://client.falixnodes.net/support/).
