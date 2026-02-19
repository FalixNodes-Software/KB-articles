---
layout: post
title: "How To Change Server Resources"
tags: Server
permalink: falix/dashboard/general/change-resources
description: "Learn how to allocate and change your server's CPU, memory, and disk resources."
keywords:
    - keyword: resources
      matches: ["change", "allocate", "upgrade", "adjust"]
    - keyword: server
      matches: ["upgrade", "downgrade"]
    - keyword: plan
      matches: ["upgrade", "downgrade", "change", "switch"]
author: Lily
---

## Introduction
This guide covers how to change your server's resources. The process differs depending on whether your server is on the **new billing system** or a **legacy premium plan**.

## Before You Start
- Changing resources requires a server restart to take effect
- Your server may experience brief downtime during the restart

---

## New Billing System

If you purchased your server through the [Billing Dashboard](https://client.falixnodes.net/billing/), follow these steps.

### Steps to Change Resources

1. Log in to the [Dashboard](https://client.falixnodes.net/).
2. Navigate to your server and go to **Server Settings** -> **Settings**.
3. Click the **Change Plan** button.
4. A modal will appear with two ways to select your new resources:

#### Preset Plans
Choose from one of the available preset plans:
- **Starter** — 4 GB RAM, 2 CPU cores
- **Friends** — 6 GB RAM, 3 CPU cores
- **Community** — 8 GB RAM, 4 CPU cores
- **Network** — 12 GB RAM, 5 CPU cores

#### Custom Configuration
Use the sliders to set your own values:
- **RAM**: 512 MB to 32 GB (in 512 MB increments)
- **CPU**: 1 to 8 cores

### Pricing

The modal will show a real-time pricing breakdown as you adjust resources, including:
- Your current plan cost
- The new plan cost
- Pro-rata charges or credits for the remaining billing period
- VAT (if applicable)

**Upgrades**: You will be charged the pro-rata difference for the remaining billing period. If you have account credits, they will be applied automatically. Otherwise, payment will be processed through your payment method (Revolut, Stripe, or PayPal).

**Downgrades**: A credit for the price difference will be applied to your account automatically.

5. Click **Pay & Apply Upgrade** (for upgrades) or **Apply Downgrade** (for downgrades).
6. Restart your server for the changes to take effect.

---

## Legacy Premium Plans

> This section is for Premium customers who are managing servers purchased through the legacy billing system.

### Steps to Change Resources

1. Log in to the [Dashboard](https://client.falixnodes.net/).
2. Navigate to your server and go to **Server Settings** -> **Settings**.
3. Click the **Change Resources** button.
4. A modal will appear with the following fields:

#### CPU Allocation
- Enter the desired CPU allocation
- 1 = 100% of one CPU core
- Minimum value: 0.25 (25% of one core)

#### Memory Allocation
- Enter the desired memory in megabytes (MB)
- Minimum value: 128 MB
- Example: For 2 GB of RAM, enter 2048

#### Disk Allocation
- Premium plans include unmetered disk space
- If you have an unmetered storage plan, this field will show "Unmetered Storage"

5. Click **Save Changes**.
6. Restart your server for the changes to take effect.

{: .warning}
> Resource changes are limited by your plan. You cannot allocate more CPU or RAM than your plan allows.

---

## After Changing Resources

- Your server needs to restart for changes to apply
- The new resource allocation will be reflected in your server dashboard
- Monitor your server to ensure it's running properly with the new configuration

{: .warning}
> If your server fails to start after changing resources, make sure you've allocated enough CPU and memory for your server software to run properly.

## Troubleshooting

- **Server won't start**: Verify you've allocated sufficient CPU and memory
- **Resources not showing**: Try refreshing the page or logging out and back in
- **Changes not applied**: Ensure you restarted your server after making changes

## Need Help?

If you're having trouble changing your server resources or need assistance determining the right allocation for your needs, please contact our [support team](https://client.falixnodes.net/support/).
