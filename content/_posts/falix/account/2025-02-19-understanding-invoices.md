---
layout: post
title: "Understanding Your Invoice"
category: Account
tags: Billing
permalink: falix/account/billing/understanding-invoices
description: "How to view, download, and understand your Falix invoices and credit notes."
keywords:
    - keyword: invoice
      matches: ["view", "download", "receipt", "pdf"]
    - keyword: credit
      matches: ["note", "refund", "balance"]
    - keyword: receipt
      matches: ["payment", "proof", "download"]
    - keyword: vat
      matches: ["tax", "invoice", "receipt"]
author: Lily
---

## Introduction
Every payment you make generates an invoice. This guide explains how to find, view, and understand your invoices and credit notes.

## Viewing Your Invoices

1. Log in to the [Falix Client Area](https://client.falixnodes.net/).
2. Navigate to the [Billing Dashboard](https://client.falixnodes.net/billing/).
3. Scroll to the **Invoices** section. Your 10 most recent invoices are listed.
4. Click **View** to open an invoice, or **Download** to save it as a PDF.

## Invoice Number Format

| Document Type | Format | Example |
|---------------|--------|---------|
| Invoice | `INV-YYYY-######` | INV-2025-000042 |
| Credit Note | `CN-YYYY-######` | CN-2025-000015 |

## What's on an Invoice

{% tabs sections %}

{% tab sections Header %}

The top of every invoice shows:
- **Invoice number** (e.g. INV-2025-000042)
- **Issue date** — when the invoice was created
- **Payment date** — when the payment was processed
- **Total amount** — the final amount charged
- **Status badge** — Paid, Refunded, or Partial Refund

{% endtab %}

{% tab sections Seller & Buyer %}

Every invoice includes:

**From (Seller):**
- SIA Baltijas Pakalpojumi
- Registration and VAT numbers
- Registered address in Latvia

**Bill To (Buyer):**
- Your email address
- Your country and ZIP code
- Your VAT number (if you've provided one)

{% endtab %}

{% tab sections Line Items & VAT %}

**Line Items:**
- Description of the service (server resources)
- Quantity, unit price, and total

**VAT Breakdown:**
- Subtotal (before tax)
- VAT rate and amount (varies by country)
- Credits applied (if any, shown in green)
- Total paid

{: .info}
> If you're a VAT-registered business in the EU, your invoice will show a **Reverse Charge** notice instead of VAT. Non-EU customers will see a **VAT Not Applicable** notice.

{% endtab %}

{% endtabs %}

## Credit Notes
Credit notes are generated when you receive account credits, such as from:
- Downgrading your server resources
- Switching to a shorter billing cycle
- Receiving a refund

Credit notes follow the same format as invoices but show the credited amount. They appear in your invoice list with a **Credit** status badge.

## Downloading Invoices
- Click the **Download PDF** button on any invoice page to save a copy
- PDFs are generated on demand and are not stored — you can download them at any time
- Both invoices and credit notes are available as PDFs

## Invoice Statuses

| Status | Meaning |
|--------|---------|
| **Paid** | Payment was processed successfully |
| **Refunded** | Full refund has been issued |
| **Partial Refund** | Partial refund has been issued |
| **Credit** | Credit note issued to your account |
