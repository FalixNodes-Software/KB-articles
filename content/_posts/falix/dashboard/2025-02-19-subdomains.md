---
layout: post
title: "How To Set Up Subdomains & Custom Domains"
tags: Server
permalink: falix/dashboard/general/subdomains
description: "Create free Falix subdomains or connect your own custom domain to your server."
keywords:
    - keyword: subdomain
      matches: ["create", "setup", "add", "domain"]
    - keyword: domain
      matches: ["custom", "own", "connect", "add"]
    - keyword: dns
      matches: ["records", "nameserver", "srv", "setup"]
    - keyword: custom domain
      matches: ["connect", "add", "own", "verify"]
author: Lily
---

## Introduction
Every server on Falix can have subdomains — free Falix subdomains or your own custom domains. Subdomains give your server a clean, memorable address instead of a raw IP and port.

When you create a subdomain, Falix automatically creates both an **A record** (pointing to your server's IP) and an **SRV record** (routing to your server's port), so players can connect using just the domain name without specifying a port.

## Falix Subdomains

Falix subdomains are free and available to all users. You can have up to **3 Falix subdomains** per server (1 primary + 2 additional).

### Available Domain Suffixes

| Suffix |
|--------|
| falixsrv.me |
| falix.gg |
| falix.me |
| falix.dev |
| falix.app |
| falix.pro |

### Creating a Subdomain

1. Navigate to your server's **Subdomains** page.
2. Click **Add Subdomain**.
3. Select **Falix Subdomain**.
4. Enter your desired subdomain name.
5. Select a domain suffix from the dropdown.
6. Select which server allocation (IP:Port) to route the domain to.
7. Click **Create**.

**Subdomain naming rules:**
- 1–20 characters
- Lowercase letters, numbers, and hyphens only
- Must start and end with a letter or number
- No consecutive hyphens (e.g. `my--server` is not allowed)
- Cannot resemble an IP address
- Must be unique across all Falix servers

### Editing a Subdomain

1. Click the **edit button** on the subdomain you want to change.
2. Enter a new subdomain name and/or change the domain suffix.
3. Click **Update**.

The old DNS records are automatically deleted and new ones are created.

### Setting a Primary Subdomain

Your primary subdomain is shown with a crown icon. To change which subdomain is primary:

1. Find the secondary subdomain you want to promote.
2. Click **Make Primary**.

The current primary and selected secondary will swap positions.

### Deleting a Subdomain

1. Click the **delete button** on the subdomain.
2. Confirm the deletion.

Both the A and SRV records are removed automatically.

{: .info}
> You cannot delete your primary subdomain, but you can edit/rename it.

---

## Custom Domains

Connect your own domain (e.g. `play.example.com`) to your Falix server. Custom domains use Falix nameservers so DNS records are managed automatically.

### Limits

| Plan | Max Custom Domains |
|------|--------------------|
| Free | 3 per server |
| Premium | 5 per server |

### Setting Up a Custom Domain

Custom domains use a dedicated setup wizard at **Subdomains** → **Add Domain** → **Custom Domain**.

#### Step 1: Enter Your Domain

Enter the domain you want to connect (e.g. `example.com` or `play.example.com`).

{: .warning}
> Falix-owned domain suffixes (falixnodes.net, falixnodes.com, etc.) cannot be used as custom domains.

#### Step 2: Configure DNS at Your Registrar

You need to add **two NS (nameserver) records** at your domain registrar pointing to Falix nameservers. Your assigned nameservers are displayed on the setup page and are unique to your account.

| Record Type | Name | Value |
|-------------|------|-------|
| NS | @ | `nsX.falixnodes.net` (shown on setup page) |
| NS | @ | `nsY.falixnodes.net` (shown on setup page) |

{% tabs registrar %}

{% tab registrar Cloudflare %}

1. Log in to [Cloudflare](https://dash.cloudflare.com/).
2. Select your domain.
3. Go to **DNS** → **Records**.
4. Add two NS records with the nameservers shown on the Falix setup page.

{: .warning}
> If Cloudflare is managing your domain's nameservers, you may need to add the NS records as delegated nameservers within Cloudflare's DNS settings rather than changing nameservers at your registrar.

{% endtab %}

{% tab registrar Namecheap %}

1. Log in to [Namecheap](https://www.namecheap.com/).
2. Go to **Domain List** → click **Manage** on your domain.
3. Under **Nameservers**, select **Custom DNS**.
4. Enter the two Falix nameservers shown on the setup page.
5. Save changes.

{% endtab %}

{% tab registrar GoDaddy %}

1. Log in to [GoDaddy](https://www.godaddy.com/).
2. Go to **My Products** → **DNS** on your domain.
3. Scroll to **Nameservers** and click **Change**.
4. Select **Enter my own nameservers**.
5. Enter the two Falix nameservers shown on the setup page.
6. Save.

{% endtab %}

{% tab registrar Squarespace Domains %}

1. Log in to [Squarespace Domains](https://domains.squarespace.com/) (formerly Google Domains).
2. Select your domain.
3. Go to **DNS** → **DNS Settings**.
4. Under **Nameservers**, switch to custom nameservers.
5. Enter the two Falix nameservers shown on the setup page.
6. Save.

{% endtab %}

{% endtabs %}

{: .info}
> DNS changes can take up to 48 hours to propagate, but usually complete within a few minutes.

#### Step 3: Verify & Link

1. Click **Verify** on the setup page.
2. The system checks that your NS records are correctly configured.
3. Once verified, Falix automatically creates the A and SRV records for your domain.
4. Your custom domain is now linked to your server.

### Managing Custom Domains

Custom domains appear in the **Custom Domains** section on your subdomains page with a verification status badge:

- **Verified** — domain is active and working
- **Pending** — NS records not yet detected (click **Verify** to retry)

To delete a custom domain, click the **delete button** on the domain card. The DNS records will be removed automatically.

### Re-Verifying a Domain

If your NS records are changed or lost, you can re-verify:

1. Ensure the NS records are set correctly at your registrar.
2. Click the **Verify** button on the domain card.
3. The system will check your NS records and update the verification status.

---

## How DNS Works

When you create any subdomain or custom domain, Falix automatically creates two DNS records:

| Record | Purpose | Example |
|--------|---------|---------|
| **A Record** | Points the domain to your server's IP address | `myserver.falixsrv.me` → `79.127.224.176` |
| **SRV Record** | Routes Minecraft traffic to the correct port | `_minecraft._tcp.myserver.falixsrv.me` → port 25565 |

The SRV record means players can connect using just the domain name (e.g. `myserver.falixsrv.me`) without needing to add `:port` at the end.

{: .info}
> SRV records are specific to Minecraft. For other games, players may still need to specify the port alongside the domain.

## Summary

| Feature | Falix Subdomains | Custom Domains |
|---------|-----------------|----------------|
| Cost | Free | Free |
| Max per server | 3 | Unmetered |
| DNS setup | Automatic | Requires NS records at registrar |
| A + SRV records | Automatic | Automatic (after verification) |
| Available suffixes | 6 Falix domains | Any domain you own |
| Verification | None needed | NS record verification |
