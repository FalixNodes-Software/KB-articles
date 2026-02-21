---
layout: post
title: "Network Restrictions"
tags: Server
permalink: falix/dashboard/server/network-restrictions
description: "Outbound network restrictions on free-plan servers and what they mean for you."
keywords:
    - keyword: network
      matches: ["restriction", "blocked", "outbound", "egress", "firewall"]
    - keyword: blocked
      matches: ["port", "connection", "outbound", "traffic"]
    - keyword: firewall
      matches: ["network", "restriction", "blocked", "egress"]
author: Lily
---

## Introduction
Free-plan servers have outbound network restrictions in place to prevent abuse and keep the platform safe for everyone. These restrictions limit certain types of outgoing traffic from your server. Most normal server activity -- downloading plugins, connecting to APIs, running your game -- is completely unaffected. Premium servers don't have these restrictions.

## What's Restricted
Certain outbound services are blocked entirely on free nodes:

- **Email sending** -- your server cannot send outbound emails. If you need email functionality, you'll need a premium plan.
- **Windows networking protocols** -- connections using Windows file sharing protocols are blocked.

On top of that, the rate at which your server can open new outbound connections is limited. This prevents servers from being used to flood external services. Once a connection is established, it works normally -- the limit only applies to how quickly new connections can be created.

{: .warning}
> These restrictions are in place to protect the platform. Attempting to circumvent them violates the [acceptable use policy](https://falixnodes.net/acceptable-use-policy) and can result in suspension.

## What Still Works
The vast majority of what you'd normally do on a game server is unaffected:

- **Downloading files** -- installing plugins, mods, server jars, and other resources works as expected.
- **External APIs** -- connecting to external APIs and webhooks works fine.
- **Databases** -- connecting to external databases is not restricted.
- **Game traffic** -- normal player connections and game protocol traffic are unaffected.

{: .info}
> If something on your server isn't connecting to an external service and you can't figure out why, it might be hitting one of these restrictions. Upgrading to premium removes all outbound limitations.

## Free vs Premium

| Feature | Free | Premium |
|---------|------|---------|
| Outbound network restrictions | Yes | No |
| Email sending | Blocked | Allowed |
| Connection rate limits | Yes | No |
| Downloads and API calls | Allowed | Allowed |
| Game traffic | Allowed | Allowed |
