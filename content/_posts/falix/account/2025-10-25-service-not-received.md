---
layout: post
title: "I Did Not Receive My Service"
category: Account
tags: Billing
permalink: falix/account/billing/service-not-received
description: "Troubleshoot common issues when you haven't received your service after purchase."
keywords:
    - keyword: plan
      matches: ["not received", "missing", "didn't get"]
    - keyword: service
      matches: ["not received", "missing", "didn't get"]
    - keyword: premium
      matches: ["not received", "missing", "didn't get"]
    - keyword: server
      matches: ["not created", "not showing", "where is"]
author: Lily
---

## Introduction
If you've purchased a service but haven't received it in your dashboard, don't worry. This guide will help you troubleshoot the most common reasons why your service might not be showing up.

## Payment Not Processed
Sometimes payments may not complete successfully, even if you've gone through the checkout process.

{% tabs payment %}

{% tab payment New Billing %}

1. Go to the [Billing Dashboard](https://client.falixnodes.net/billing/).
2. Check if your subscription shows as **Active**.
3. If you don't see a subscription at all, your payment may not have completed. Check your email for a payment confirmation from your payment provider (Revolut, Stripe, or PayPal).
4. If you were redirected to a success page but don't see your server, wait a few minutes — provisioning may still be in progress.

{% endtab %}

{% tab payment Legacy (WHMCS) %}

1. Log in to the [Legacy Billing Area](https://billing.falixnodes.net/) and navigate to **Billing** > **Invoices**.
2. Look for your recent invoice and check its status:
   - **Paid**: Your payment was processed successfully
   - **Unpaid**: Your payment was not completed
3. If the invoice shows as unpaid, click on it and complete the payment.
4. Check with your bank or payment provider to ensure the transaction wasn't declined.

{% endtab %}

{% endtabs %}

## Service Pending Activation
After payment, your server needs to be provisioned (created and configured). This usually happens automatically but may take a few minutes.

{% tabs activation %}

{% tab activation New Billing %}

The new billing system provisions servers automatically after payment. If your server hasn't appeared:
1. Wait 5-10 minutes after payment confirmation.
2. Refresh the [Billing Dashboard](https://client.falixnodes.net/billing/) — your server should appear with an **Active** status.
3. Check the main [Dashboard](https://client.falixnodes.net/) to see if the server is listed there.
4. If the server still doesn't appear after 10 minutes, there may have been a provisioning issue — contact support.

{% endtab %}

{% tab activation Legacy (WHMCS) %}

1. Wait 5-10 minutes after payment confirmation.
2. Refresh your dashboard or log out and log back in.
3. Check the **Services** page in the client area.

{% endtab %}

{% endtabs %}

## Mismatch Between Billing and Dashboard Accounts

{: .info}
> This issue only applies to the legacy billing system. The new billing system is tied directly to your client area account, so this cannot happen.

If you purchased through the [Legacy Billing Area](https://billing.falixnodes.net/), the most common reason for not receiving your service is logging into a different account than the one used for billing.

1. Check the email address you used when making the payment.
2. Make sure you're logged into the [Falix Client Area](https://client.falixnodes.net/) with the same email address.
3. If you have multiple accounts, try logging out and logging in with the correct account.
4. Check your email for the order confirmation to verify which account the service was assigned to.

## Payment Failed or Suspended (New Billing Only)
If your payment method was declined, the new billing system will retry the charge automatically. You may see one of these statuses on your subscription:

- **Past Due**: Your payment failed but retries are in progress. You can update your payment method or manually retry the payment from the [Billing Dashboard](https://client.falixnodes.net/billing/).
- **Suspended**: Multiple payment retries have failed. Your servers will be taken offline. Update your payment method and click **Retry Payment** or **Renew Servers** to restore your service.

{: .info}
> For more details, see our [Payment Failed](falix/account/billing/payment-failed) article.

## Wrong Server Location or Resources
If you received your service but it's not configured as expected, you can adjust the settings.

1. Log in to the [Falix Client Area](https://client.falixnodes.net/).
2. Navigate to your service.
3. To change resources:
   - Go to **Server Settings** -> **Settings**
   - Look for the resource allocation options
   - Adjust CPU, RAM, or storage as needed
4. To transfer your server to a new location:
   - Navigate to your [Server Console](https://client.falixnodes.net/server/console)
   - On the right side of the console, locate the card showing your current server location
   - Click on the server location card
   - Select your preferred location and confirm the transfer

{: .warning}
> Transferring your server to a new location may cause temporary downtime.

## Which Billing System Am I On?
- If you purchased recently through the client area checkout, check the [Billing Dashboard](https://client.falixnodes.net/billing/).
- If you purchased through billing.falixnodes.net or have an older subscription, check the [Legacy Billing Area](https://billing.falixnodes.net/).
- Not sure? Check both — your subscription will only appear in one of them.

## Still Having Issues?
If none of these solutions work, please contact our [support team](https://client.falixnodes.net/support/).
