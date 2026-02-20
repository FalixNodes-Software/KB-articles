---
layout: post
title: "How To Manage Ports"
tags: Networking
permalink: falix/dashboard/networking/extra-port
description: "Add extra ports, set a primary port, and organize your allocations with notes."
keywords:
    - keyword: port
      matches: ["allocate", "create", "dedicated", "extra", "webserver", "secondary", "network", "open"]
    - keyword: primary port
      matches: ["set", "change", "switch", "main"]
    - keyword: port note
      matches: ["label", "description", "name", "tag"]
author: Lily
---

## Why Extra Ports?

Your server starts with one primary port -- that is the one players use to connect. But many plugins and mods need their own dedicated ports to work properly. Dynmap, BlueMap, voice chat mods, and Geyser are all common examples. Each one runs its own mini web server or listener that needs a separate port to avoid clashing with your main game server.

Extra ports give you those additional gateways so everything can run side by side without stepping on each other.

## Adding an Extra Port

1. Navigate to your server's **Network** page.
2. Select the **Ports** tab.
3. Click **Add Port**.
4. A new port is automatically allocated from the available pool on your node.

That is it -- the new port appears in your port list right away and is ready to use. You can assign it in your plugin or mod configuration immediately.

{: .info}
> Each server has an allocation limit that determines how many total ports you can have. Your current usage is shown at the bottom of the ports list.

## Setting a Primary Port

Your primary port is marked with a crown icon. It is the main port your server listens on and the one your subdomains point to. If you need to switch which port is primary:

1. Find the secondary port you want to promote.
2. Click **Make Primary** on that port.

When you change the primary port, Falix automatically updates your DNS records (A and SRV) so your subdomains continue to work correctly with the new port.

{: .warning}
> Changing your primary port will update your server's connection address. Make sure your players know about the change, or set up a subdomain so the address stays consistent.

## Adding a Note to a Port

With multiple ports allocated, it can get hard to remember which one is for what. Port notes let you label each port so you always know at a glance:

1. Click the **Edit Note** button on any port.
2. Type a short description (e.g. "Dynmap", "Voice Chat", "Geyser").
3. Save the note.

Notes are purely for your own reference -- they do not affect how the port works.

## Deleting a Port

If you no longer need an extra port:

1. Click the **Delete** button on the port you want to remove.
2. Confirm the deletion.

The port is released back to the available pool.

{: .info}
> You cannot delete your primary port. If you want to remove it, set a different port as primary first, then delete the old one.

## Common Use Cases

Here are some of the most common reasons people add extra ports:

| Plugin / Mod | What It Needs a Port For |
|-------------|--------------------------|
| **Dynmap / BlueMap** | Serves a web-based live map of your world |
| **Simple Voice Chat** | Runs a voice communication server alongside your game |
| **Geyser** | Listens for Bedrock Edition connections on a separate port |
| **Plan** | Hosts a web analytics dashboard for your server |

For each of these, you will add an extra port on the Network page and then enter that port number in the plugin or mod's configuration file.
