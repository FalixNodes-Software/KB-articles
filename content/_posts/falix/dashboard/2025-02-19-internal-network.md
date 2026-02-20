---
layout: post
title: "How To Set Up Internal Networking"
tags: Networking
permalink: falix/dashboard/networking/internal-network
description: "Connect your servers together using private internal IPs for proxy setups and linked services."
keywords:
    - keyword: internal network
      matches: ["setup", "enable", "private", "connect"]
    - keyword: internal ip
      matches: ["private", "network", "connect", "server"]
    - keyword: bungeecord
      matches: ["proxy", "velocity", "internal", "network"]
    - keyword: velocity
      matches: ["proxy", "bungeecord", "internal", "network"]
    - keyword: internal only
      matches: ["hide", "ports", "private", "mode"]
author: Lily
---

## Introduction

If you have ever wanted to run a proxy network with a lobby, survival, and creative server all linked together, or connect a game server to a separate database without exposing it to the public internet, internal networking is exactly what you need.

Internal networking gives each of your servers a private IP address that only your other servers can see. This means your backend servers stay completely hidden from the outside world -- players connect through your proxy, and everything behind it is invisible to anyone who should not be there. It is the same concept used by large Minecraft networks to keep their infrastructure secure and organized.

Here are a few real-world scenarios where internal networking shines:

- **BungeeCord or Velocity proxy networks** -- Your proxy is the only server with a public address. Lobby, survival, minigames, and other backend servers are only reachable through the proxy, so players cannot bypass it and connect directly.
- **Linked databases** -- A MySQL or Redis server running on a separate Falix server can be reached by your game servers over the internal network, without ever being exposed publicly.
- **Security and isolation** -- Even if someone discovers your server's public IP, your backend servers remain completely unreachable from the outside.

{: .info}
> Internal networking is a **premium feature**. Free plan users will need to upgrade to use it.

## How It Works

Under the hood, Falix uses **WireGuard** to create encrypted tunnels between your servers. When you enable internal networking, your server is assigned a private IP address (something like `10.0.0.42`). Only servers owned by your account can communicate over these private IPs -- other users' servers cannot see or reach them, and the traffic never touches the public internet.

Think of it as a private, invisible highway that only your servers have access to.

## Enabling Internal Networking

1. Navigate to your server's **Network** page.
2. Select the **Internal Network** tab.
3. Click **Enable Internal Network**.
4. A private IP address will be assigned to your server automatically.

Your internal IP is displayed on the page and you can copy it by clicking on it. You will need this IP when configuring other servers to connect to this one.

## Disabling Internal Networking

If you no longer need internal networking on a server:

1. Click the **Disable** button on the Internal Network tab.
2. Your private IP is released and becomes available for other servers.

{: .info}
> Disabling internal networking also turns off Internal Only mode if it was enabled.

## Internal Only Mode

This is where things get really useful for proxy setups. Internal Only mode hides all of your server's public ports, making it accessible **only** through its internal IP. The public ports are not deleted -- they are just hidden from external access, so you can re-enable them at any time.

To turn it on:

1. Enable internal networking first (if you have not already).
2. Toggle the **Internal Only Mode** switch.
3. Restart your server for the change to take effect.

{: .warning}
> When Internal Only mode is enabled, no one can connect to your server from the public internet. Only your other servers with internal networking enabled can reach it. Do not enable this on a server that players need to connect to directly.

### When to Use Internal Only

| Scenario | Internal Only |
|----------|--------------|
| Proxy backend servers (players connect through the proxy, not directly) | On |
| Internal database or cache servers | On |
| The proxy server itself (needs to be publicly reachable) | Off |
| Standalone game servers that also use internal networking | Off |

The general rule is simple: if players or external services need to connect to it directly, leave Internal Only off. If only your own servers need to reach it, turn it on.

## Connected Servers

Once you have internal networking enabled on multiple servers, the Internal Network tab shows a **Connected Servers** section. This lists every other server on your account that also has internal networking enabled, along with its name and internal IP (click to copy).

This makes it easy to grab the right IP addresses when you are setting up your proxy config or plugin database connections -- no need to switch back and forth between server pages.

{: .info}
> If no other servers have internal networking enabled yet, this section will prompt you to enable it on your other servers first.

## Common Setups

{% tabs setups %}

{% tab setups BungeeCord / Velocity Proxy %}

This is the most popular use case. If you are building a network with a lobby, survival, and creative server, this is how you connect them all.

**Proxy Server (the one players connect to):**
- Internal networking: Enabled
- Internal Only mode: **Off** -- players need to reach this server publicly
- Internal IP: e.g. `10.0.0.2`

**Backend Servers (Lobby, Survival, Creative, etc.):**
- Internal networking: Enabled
- Internal Only mode: **On** -- only the proxy should connect to these
- Internal IPs: e.g. `10.0.0.3`, `10.0.0.4`, `10.0.0.5`

In your proxy configuration file (BungeeCord's `config.yml` or Velocity's `velocity.toml`), use the backend servers' internal IPs instead of public addresses:

```yaml
servers:
  lobby:
    address: 10.0.0.3:25565
  survival:
    address: 10.0.0.4:25565
  creative:
    address: 10.0.0.5:25565
```

With this setup, players connect to your proxy's public address, and the proxy routes them to the correct backend server over the internal network. The backend servers are completely invisible to the outside world.

{% endtab %}

{% tab setups Linked Database %}

If you are running plugins that need a shared database (like LuckPerms, LiteBans, or a shared economy plugin), you can host the database on a separate server and connect to it internally.

**Game Server:**
- Internal networking: Enabled
- Internal Only mode: Off (players connect to this server)
- Connects to the database at `10.0.0.10:3306`

**Database Server:**
- Internal networking: Enabled
- Internal Only mode: **On** -- no reason for this to be publicly accessible
- Internal IP: `10.0.0.10`

In your plugin configuration, point to the database server's internal IP:

```yaml
database:
  host: 10.0.0.10
  port: 3306
```

This keeps your database completely locked down -- it cannot be reached from the public internet, only from your own game servers.

{% endtab %}

{% endtabs %}

## Wrapping Up

Internal networking is a premium feature powered by WireGuard encrypted tunnels. It assigns private IPs from the node's internal subnet (like `10.0.0.x`) that only your own servers can use. Combined with Internal Only mode to hide public ports, it gives you everything you need to build a secure, professional server network -- whether that is a BungeeCord proxy setup, a linked database, or any architecture where your servers need to talk to each other privately.
