---
layout: post
title: "How To Set Up a Reverse Proxy"
tags: Networking
permalink: falix/dashboard/networking/reverse-proxy
description: "Expose web applications running on your server to the internet with automatic SSL."
keywords:
    - keyword: reverse proxy
      matches: ["setup", "create", "web", "http", "https"]
    - keyword: proxy
      matches: ["create", "domain", "ssl", "web"]
    - keyword: web
      matches: ["proxy", "http", "https", "application", "dashboard"]
    - keyword: ssl
      matches: ["proxy", "certificate", "https", "tls"]
author: Lily
---

## Introduction

Want to show your Dynmap or BlueMap on a clean URL like `map.myserver.com`? Need to expose a web panel with HTTPS so your browser doesn't throw security warnings? That's exactly what reverse proxies are for.

A reverse proxy takes a web application running privately on one of your server's ports and makes it publicly accessible through a real domain -- complete with automatic SSL/HTTPS. No manual certificate setup, no fiddling with Nginx configs. You just point, click, and you're live.

{: .info}
> Reverse proxy is a **premium feature**. Free plan users will need to upgrade to use it.

## How It Works

The process is straightforward:

1. You run a web application on one of your server's ports -- for example, Dynmap listening on port 8080.
2. You create a reverse proxy that links a domain (like `map.myserver.com`) to that port.
3. Falix handles all the routing, sending HTTP and HTTPS traffic from the domain straight to your application.
4. SSL certificates are provisioned and renewed automatically -- you never have to think about them.

In short, your visitors type in a clean URL, and Falix makes sure the request reaches the right place securely.

## Creating a Reverse Proxy

1. Navigate to your server's **Network** page.
2. Select the **Reverse Proxy** tab.
3. Click **Create Proxy**.
4. Choose a domain type and configure the proxy (details below).
5. Click **Create**.

You can have up to **3 reverse proxies** per server, so you could run a map, a web panel, and an API endpoint all at once if you wanted to.

### Domain Types

{% tabs domaintype %}

{% tab domaintype Falix Subdomain %}

This is the quickest option -- you get a free subdomain on `falix.org` with no DNS configuration needed.

Just pick a **Subdomain** name (for example, entering `mymap` gives you `mymap.falix.org`) and select the **Backend Port** your web application is running on. That's it.

**Subdomain rules:**
- 1 to 20 characters long
- Lowercase letters, numbers, and hyphens only
- Must start and end with a letter or number
- No consecutive hyphens (so `my--map` won't work, but `my-map` is fine)

{: .info}
> Falix subdomains are great for quick testing or if you don't own a domain yet. You can always switch to a custom domain later.

{% endtab %}

{% tab domaintype Custom Domain %}

If you own a domain, you can use it for a more professional look -- something like `map.example.com` or `panel.example.com`.

Enter the full **Domain** you want to use and select the **Backend Port** your application is running on. Custom domains require a quick DNS verification step before the proxy goes live. See [Verifying a Custom Domain](#verifying-a-custom-domain) below for the details.

{: .warning}
> Falix-owned domains (falixnodes.net, falixnodes.com, falix.org, etc.) cannot be used as custom proxy domains.

{% endtab %}

{% endtabs %}

## Verifying a Custom Domain

When you use your own domain, Falix needs to confirm you actually own it. This is done by adding a couple of DNS records at your domain registrar -- if you've ever pointed a domain at a website before, this will feel familiar.

### Step 1: Start Verification

1. Enter your domain in the custom domain field.
2. Click **Verify**.
3. The system generates a verification token and shows you exactly which DNS records to add.

### Step 2: Add DNS Records

Head over to your domain registrar (Cloudflare, Namecheap, GoDaddy, etc.) and add these two records:

| Record Type | Name | Value |
|-------------|------|-------|
| **TXT** | `_falix-verification.yourdomain.com` | The verification token shown on the page |
| **CNAME** | Your subdomain (e.g. `map`) | `proxy.falix.org` |

{: .info}
> DNS changes can take up to 24 hours to propagate, but in practice they usually go through within a few minutes. If verification fails on the first try, give it a bit and try again.

### Step 3: Check Status

Click **Verify Domain** to check whether your DNS records have propagated. Once verified, the proxy is created automatically and starts routing traffic right away. You should be able to visit your domain and see your application live.

## Proxy Status

Each proxy card on the dashboard shows a couple of status indicators so you always know what's going on:

- **Active** (green) means the proxy is enabled and actively routing traffic to your application. Everything is working as expected.
- **Disabled** (red) means the proxy has been turned off. Traffic won't be routed, but the proxy configuration is still saved.
- **SSL** (blue lock) means your SSL certificate is active and visitors are connecting over HTTPS.
- **SSL Pending** (orange clock) means your SSL certificate is still being provisioned. This usually resolves within a few minutes. If it stays pending for a while, double-check that your DNS records are correct.

## Managing Proxies

### Enabling and Disabling

Use the **toggle switch** on a proxy card to turn it on or off. Disabling a proxy stops it from routing traffic, but it doesn't delete anything -- you can re-enable it whenever you're ready.

{: .info}
> This is handy if you're doing maintenance on a web app and don't want visitors hitting a broken page.

### Editing

Click the **Edit** button to change which backend port the proxy forwards traffic to. This is useful if you've moved your application to a different port. Note that you can't change the domain itself -- if you need a different domain, delete the proxy and create a new one.

### Opening

Click the **Open** button to visit your proxy URL in a new browser tab. It's a quick way to confirm everything is working without manually typing the address.

### Deleting

If you no longer need a proxy, click the **Delete** button on its card and confirm the deletion. The proxy and its SSL certificate will be removed. If you're using a custom domain, you can also clean up the DNS records at your registrar, though leaving them won't cause any issues.

## Common Use Cases

Here are some of the most popular things people use reverse proxies for:

- **Dynmap, BlueMap, or Pl3xMap** -- These Minecraft map plugins run a small web server on your game server. With a reverse proxy, your players can visit something like `map.myserver.com` instead of memorizing an IP and port number. It looks way more professional and it's secured with HTTPS.
- **Web panels and admin dashboards** -- If you're running any kind of management interface, a reverse proxy lets you access it through a proper domain with SSL, rather than an unencrypted IP:port combo.
- **REST APIs** -- Building a bot or service that exposes an API? A reverse proxy gives it a clean endpoint like `api.myserver.com` with automatic HTTPS.
- **Any HTTP-based application** -- Really, anything that serves web traffic on one of your allocated ports can be proxied. If it speaks HTTP, a reverse proxy can put it on a domain.

## Wrapping Up

Reverse proxies are one of those features that take about two minutes to set up but make a big difference in how polished and accessible your server's web applications feel. You get a clean domain, automatic HTTPS, and up to three proxies per server -- all managed right from the dashboard. Whether you're sharing a live map with your community or running an admin panel, it's well worth setting up.
