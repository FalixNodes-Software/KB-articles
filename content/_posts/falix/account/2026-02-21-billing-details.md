---
layout: post
title: "How To Manage Your Billing Details"
category: Account
tags: Billing
permalink: falix/account/billing/billing-details
description: "Set up your billing country, ZIP code, company name, and VAT number for correct invoicing."
keywords:
    - keyword: billing
      matches: ["details", "info", "information", "address"]
    - keyword: vat
      matches: ["number", "exempt", "reverse charge", "verify"]
    - keyword: tax
      matches: ["info", "details", "country", "rate"]
    - keyword: company
      matches: ["name", "business", "vat", "details"]
author: Lily
---

## Introduction
Your billing details determine how VAT is calculated on your charges and what information appears on your invoices. This guide shows you how to set up and update your country, ZIP code, and business information for correct invoicing and potential VAT exemption.

## Viewing Your Billing Details
1. Go to the [Billing Dashboard](https://client.falixnodes.net/billing/).
2. Look at the **Billing Details** card on the right side of the page.

This card displays:
- Your **country** and **ZIP / postal code**
- The **VAT rate** being applied to your charges
- Your **company name** and **VAT number** (if you've added business details), along with a **Verified** badge if your VAT number has been validated

## Setting Up or Editing Your Location
Your country and ZIP code are required for billing. They determine your VAT rate and appear on all your invoices.

1. On the [Billing Dashboard](https://client.falixnodes.net/billing/), click **Edit**{: .blue } on the Billing Details card.
2. In the Billing Information modal, find the **Location** section.
3. Select your **Country** from the dropdown.
4. Enter your **ZIP / Postal Code**.
5. Click **Save**{: .green }.

{: .info}
> Your country determines your VAT rate. EU countries are charged VAT at their local rate (e.g. 19% for Germany, 21% for the Netherlands). Non-EU countries are not charged VAT.

## Adding Business Details (EU VAT Exemption)
If you're an EU-registered business, you can enter your VAT number to receive a VAT exemption under the reverse charge mechanism. This means VAT is no longer added to your charges.

### Steps
1. On the [Billing Dashboard](https://client.falixnodes.net/billing/), click **Edit**{: .blue } on the Billing Details card.
2. In the Billing Information modal, find the **Business Details** section.
3. Enter your **Company Name** as registered with your tax authority.
4. Enter your **VAT Number** including the country prefix (e.g. DE123456789 for Germany, FR12345678901 for France, NL123456789B01 for the Netherlands).
5. Click **Verify**{: .blue } -- the system will validate your VAT number against the EU VIES database in real time.
6. If the number is valid, a green **Verified** badge appears next to it.
7. Click **Save**{: .green } to apply your changes.

{: .warning}
> Make sure your VAT number includes the two-letter country prefix. Numbers without the prefix will not validate.

### What Happens After Verification

{% tabs vat-result %}

{% tab vat-result EU Business (Outside Latvia) %}

Once your VAT number is verified:
- **VAT is removed** from all future charges (reverse charge applies).
- Your invoices will display a **"Reverse Charge"** notice instead of a VAT line item.
- Your company name and VAT number will appear in the "Bill To" section of all invoices.
- You become responsible for accounting for VAT in your own country under the reverse charge mechanism.

{% endtab %}

{% tab vat-result EU Business (Latvia) %}

Since we are based in Latvia:
- Latvian businesses are **always charged VAT** at the local Latvian rate, regardless of VAT registration.
- Your company name and VAT number will still appear on invoices.
- This is a requirement of Latvian tax law and cannot be overridden.

{% endtab %}

{% tab vat-result Non-EU Customer %}

If you're located outside the EU:
- **VAT is not applicable** regardless of whether you enter business details.
- Adding business details is optional, but if you do, they will appear on your invoices.

{% endtab %}

{% endtabs %}

## Removing Business Details
If you need to remove your business information and return to standard consumer billing:

1. Open the Billing Information modal from the [Billing Dashboard](https://client.falixnodes.net/billing/).
2. Clear the **Company Name** and **VAT Number** fields.
3. Click **Save**{: .green }.

After removal, VAT will be applied to all future charges at your country's standard rate.

{: .info}
> Changes to your billing details only affect future charges. Existing invoices are not retroactively updated.

## Troubleshooting

| Issue | Solution |
|-------|----------|
| VAT number won't verify | Make sure you include the two-letter country prefix (e.g. DE, FR, NL). Verify that the number is active on the [EU VIES database](https://ec.europa.eu/taxation_customs/vies/) |
| Still being charged VAT after adding a VAT number | If you're a Latvian business, VAT is always applied (see above). For other EU countries, check that the **Verified** badge is showing next to your VAT number |
| Wrong VAT rate | Update your country in the Location section. The VAT rate is determined by your billing country |
| Business details not appearing on invoices | Make sure you clicked **Save** after entering your details. Check the Billing Details card to confirm they're saved |

## Related Articles
- [Understanding Billing & Pricing](falix/account/billing/understanding-billing) -- for details on how VAT rates and pricing work
- [Understanding Your Invoice](falix/account/billing/understanding-invoices) -- for how VAT and business details appear on invoices
- [Navigating the Billing Dashboard](falix/account/billing/billing-dashboard) -- for a full tour of the billing dashboard
