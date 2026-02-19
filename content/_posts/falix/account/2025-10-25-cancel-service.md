---
layout: post
title: "How To Cancel a Service"
category: Account
tags: Billing
permalink: falix/account/billing/cancel-service
description: "Learn how to cancel your Falix service through our billing systems."
keywords:
    - keyword: cancel
      matches: ["service", "subscription", "plan", "server"]
    - keyword: cancellation
      matches: ["request", "form", "undo", "reactivate"]
author: Lily
---

## Introduction
If you need to cancel your Falix service, you can do so through either of our billing systems depending on where your subscription was created.

{: .warning}
> Make sure to backup any important data before cancelling. Once cancelled, your data may not be recoverable.

## Cancelling Your Service

{% tabs cancel %}

{% tab cancel New Billing %}

If you purchased your service through the client area at [client.falixnodes.net/billing](https://client.falixnodes.net/billing/), follow these steps.

### How Cancellation Works
Cancellations are **deferred** — your server stays active until the end of your current billing period. You will not be charged again, but you keep access until the period ends.

### Steps to Cancel a Server
1. Log in to the [Falix Client Area](https://client.falixnodes.net/).
2. Navigate to the [Billing Dashboard](https://client.falixnodes.net/billing/).
3. Find the server you want to cancel in your server list.
4. Click the **Cancel Server** button on that server.
5. A confirmation modal will appear showing:
   - The date your server will remain active until
   - A reminder that all data will be deleted after cancellation
6. Confirm the cancellation.

### After Cancelling
- Your server's status will change to **Cancelling** (shown in yellow).
- Your server remains fully functional until the end of your billing period.
- You will not be charged on the next billing date for that server.
- Once the billing period ends, the server and its data will be permanently deleted.

### Undo a Cancellation
Changed your mind? You can reverse a cancellation before the billing period ends:
1. Go to the [Billing Dashboard](https://client.falixnodes.net/billing/).
2. Find the server showing **Cancelling** status.
3. Click the **Undo Cancellation** button.
4. Your server will return to **Active** status and billing will resume as normal.

{: .info}
> You can cancel and undo as many times as you like before the billing period ends.

{% endtab %}

{% tab cancel Legacy (WHMCS) %}

If you purchased your service through the legacy billing area at [billing.falixnodes.net](https://billing.falixnodes.net/), follow these steps.

### Steps to Cancel Your Service
1. Log in to the [Legacy Billing Area](https://billing.falixnodes.net/).
2. Navigate to **Services** in the top menu.
3. Click on the service you want to cancel.
4. In the left sidebar, click the **Request Cancellation** button.
5. Select your cancellation type:
   - **Immediate**: Cancels the service immediately (you will lose access to remaining paid time and no refund will be issued)
   - **End of Billing Period**: Keeps your service active until your current billing period ends (recommended)
6. Select a reason for cancellation from the dropdown menu.
7. (Optional) Provide additional feedback in the text box.
8. Click **Request Cancellation** to submit your request.

{: .warning}
> To avoid being charged for the next billing cycle, submit your cancellation request at least 4 days before your renewal date.

### After Submitting
- Your cancellation will be processed instantly
- You will receive a confirmation email
- If you selected **Immediate**, your service will be terminated right away
- If you selected **End of Billing Period**, your service will remain active until the current billing cycle ends

{% endtab %}

{% endtabs %}

## Which Billing System Am I On?
- If you purchased your service recently through the client area checkout, you are on the **new billing system**. Visit [client.falixnodes.net/billing](https://client.falixnodes.net/billing/) to manage it.
- If you purchased through billing.falixnodes.net or have an older subscription, you are on the **legacy billing system**. Visit [billing.falixnodes.net](https://billing.falixnodes.net/) to manage it.

## Need Help?
If you're experiencing issues with your service or have questions before cancelling, please contact our [support team](https://client.falixnodes.net/support/).
