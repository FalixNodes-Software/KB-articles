---
layout: post
title: "How To Set Up Subdomains & Custom Domains"
tags: Networking
permalink: falix/dashboard/networking/subdomains
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

## Why Use a Subdomain?

Nobody wants to share an address like `79.127.224.176:25832` with their friends. It is hard to remember, easy to mistype, and honestly just looks a little rough. A subdomain gives your server a clean, professional address like `myserver.falix.gg` -- something your players can actually remember and type without double-checking every digit.

Whether you grab a free Falix subdomain or connect a domain you already own, the end result is the same: players connect using a simple name instead of a raw IP and port. Falix handles all the behind-the-scenes DNS work automatically, so you do not need to be a networking expert to set this up.

{: .info}
> Pick a memorable subdomain -- your players will type this every time they connect. Short, simple names work best.

---

## Falix Subdomains

Falix subdomains are completely free for every user. Each server can have up to **3 Falix subdomains** (1 primary + 2 additional), which is plenty for most setups.

### Available Domain Suffixes

When you create a Falix subdomain, you get to pick from the following suffixes:

- **falixsrv.me**
- **falix.gg**
- **falix.me**
- **falix.dev**
- **falix.app**
- **falix.pro**

So, for example, you could end up with something like `survival.falix.gg` or `creative.falix.pro` -- whatever fits your server best.

### Creating a Subdomain

Setting one up only takes a moment:

1. Navigate to your server's **Subdomains** page.
2. Click **Add Subdomain**.
3. Select **Falix Subdomain**.
4. Type in the subdomain name you want.
5. Choose a domain suffix from the dropdown.
6. Select which server allocation (IP:Port) the domain should point to.
7. Click **Create**.

That is it -- Falix automatically creates the DNS records your players need to connect.

{: .info}
> There are a few naming rules to keep in mind. Your subdomain must be 1-20 characters long, using only lowercase letters, numbers, and hyphens. It has to start and end with a letter or number, cannot have consecutive hyphens (like `my--server`), cannot look like an IP address, and must be unique across all Falix servers.

### Editing a Subdomain

Changed your mind about the name? No problem:

1. Click the **edit button** on the subdomain you want to change.
2. Enter a new name and/or pick a different domain suffix.
3. Click **Update**.

Falix automatically removes the old DNS records and creates new ones, so you do not need to clean anything up yourself.

### Setting a Primary Subdomain

Your primary subdomain is the one displayed with a crown icon. If you want a different subdomain to be your primary:

1. Find the secondary subdomain you want to promote.
2. Click **Make Primary**.

The current primary and selected secondary simply swap positions.

### Deleting a Subdomain

If you no longer need a subdomain:

1. Click the **delete button** on the subdomain.
2. Confirm the deletion.

Both the A and SRV records are cleaned up automatically.

{: .info}
> You cannot delete your primary subdomain, but you can always edit or rename it.

---

## Custom Domains

Already own a domain? You can connect it to your Falix server so players join through something like `play.example.com`. This is great if you want full control over your branding, or if you already have a website and want your server address to match.

Custom domains are free to set up and there is no limit on how many you can connect. The process takes a few extra steps compared to Falix subdomains because you need to point your domain's nameservers to Falix, but the setup wizard walks you through everything.

### Setting Up a Custom Domain

Head to **Subdomains** then click **Add Domain** and select **Custom Domain** to launch the setup wizard.

#### Step 1: Enter Your Domain

Type in the domain you want to connect, for example `example.com` or `play.example.com`.

{: .warning}
> Falix-owned domain suffixes (falixnodes.net, falixnodes.com, etc.) cannot be used as custom domains.

#### Step 2: Configure DNS at Your Registrar

This is the part where you tell the internet that Falix is handling DNS for your domain. You need to add **two NS (nameserver) records** at your domain registrar, pointing to the Falix nameservers shown on the setup page. These are unique to your account, so make sure you copy them exactly.

| Record Type | Name | Value |
|-------------|------|-------|
| NS | @ | `nsX.falixnodes.net` (shown on setup page) |
| NS | @ | `nsY.falixnodes.net` (shown on setup page) |

Here is how to do it at some of the most popular registrars:

{% tabs registrar %}

{% tab registrar Cloudflare %}

1. Log in to [Cloudflare](https://dash.cloudflare.com/).
2. Select your domain.
3. Go to **DNS** then **Records**.
4. Add two NS records with the nameservers shown on the Falix setup page.

{: .warning}
> If Cloudflare is managing your domain's nameservers, you may need to add the NS records as delegated nameservers within Cloudflare's DNS settings rather than changing nameservers at your registrar.

{% endtab %}

{% tab registrar Namecheap %}

1. Log in to [Namecheap](https://www.namecheap.com/).
2. Go to **Domain List** and click **Manage** on your domain.
3. Under **Nameservers**, select **Custom DNS**.
4. Enter the two Falix nameservers shown on the setup page.
5. Save changes.

{% endtab %}

{% tab registrar GoDaddy %}

1. Log in to [GoDaddy](https://www.godaddy.com/).
2. Go to **My Products** then **DNS** on your domain.
3. Scroll to **Nameservers** and click **Change**.
4. Select **Enter my own nameservers**.
5. Enter the two Falix nameservers shown on the setup page.
6. Save.

{% endtab %}

{% tab registrar Squarespace Domains %}

1. Log in to [Squarespace Domains](https://domains.squarespace.com/) (formerly Google Domains).
2. Select your domain.
3. Go to **DNS** then **DNS Settings**.
4. Under **Nameservers**, switch to custom nameservers.
5. Enter the two Falix nameservers shown on the setup page.
6. Save.

{% endtab %}

{% endtabs %}

{: .info}
> DNS changes can take up to 48 hours to propagate worldwide, but in practice they usually go through within a few minutes. If verification does not work right away, just give it a little time and try again.

#### Step 3: Verify and Link

Once your nameservers are in place:

1. Click **Verify** on the setup page.
2. Falix checks that your NS records are pointing to the right place.
3. Once confirmed, Falix automatically creates the A and SRV records for your domain.
4. Your custom domain is now live and ready for players to connect.

### Managing Custom Domains

Your custom domains show up in the **Custom Domains** section on the subdomains page, each with a status badge:

- **Verified** -- the domain is active and working. Players can connect using it right now.
- **Pending** -- Falix has not detected your NS records yet. Click **Verify** to check again.

To remove a custom domain, just click the **delete button** on its card. DNS records are cleaned up automatically.

### Re-Verifying a Domain

If something changes with your nameserver setup (maybe you accidentally removed them, or your registrar reset something), you can re-verify at any time:

1. Make sure the NS records are set correctly at your registrar.
2. Click the **Verify** button on the domain card.
3. Falix checks your NS records and updates the verification status.

---

## How DNS Works (The Simple Version)

You do not need to understand DNS to use subdomains on Falix, but here is a quick explanation if you are curious.

When someone types your server address into Minecraft, their computer needs to figure out two things: what IP address to connect to, and what port to use. That is exactly what the two DNS records Falix creates are for:

| Record | Purpose | Example |
|--------|---------|---------|
| **A Record** | Translates your domain name into your server's IP address | `myserver.falixsrv.me` -> `79.127.224.176` |
| **SRV Record** | Tells Minecraft which port to use so players do not have to type it | `_minecraft._tcp.myserver.falixsrv.me` -> port 25565 |

Think of the A record as the street address of a building, and the SRV record as the specific room number inside it. Together, they let players reach your server by typing just the domain name -- no `:port` needed.

{: .info}
> SRV records are specific to Minecraft. If you are running a different game, players may still need to add the port number after the domain (like `myserver.falix.gg:25565`).

---

## Summary

Here is a quick side-by-side comparison to help you decide which option is right for you:

| Feature | Falix Subdomains | Custom Domains |
|---------|-----------------|----------------|
| Cost | Free | Free |
| Max per server | 3 | Unmetered |
| DNS setup | Automatic | Requires NS records at registrar |
| A + SRV records | Automatic | Automatic (after verification) |
| Available suffixes | 6 Falix domains | Any domain you own |
| Verification | None needed | NS record verification |

For most people, a free Falix subdomain is the easiest way to get a clean server address up and running in seconds. If you want something more personal or already have a domain, the custom domain option gives you that extra level of branding without any added cost.
