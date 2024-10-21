---
layout: post
title: Assigning an Extra Port
category: Dashboard
tags: Server
permalink: falix/dashboard/server/extra-port
description: Allocating a dedicated network port.
keywords: allocate port, create port, dedicated port, extra port, webserver port, secondary port, network port
author:
    - Naoki
    - Mocab
---

## :mailbox_closed: What Is a Port?

A port is like a gateway that allows internet traffic to flow in and out of. Just like in a harbour, you cannot have two ships arriving or departing from the same dock, and so multiple docks are used to increase the ship capacity. The same can be applied to ports, when multiple different types of content is delivered from the server, multiple ports must be used to avoid clashing with each other and the main port.

As such, when a certain type of mod, plugin or software is used that forwards traffic over a dedicated port, such as Dynmap's webserver and voice chat mods, extra ports must be used.

## :inbox_tray: Assigning an Extra Port

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Advanced" then navigate to [Network](https://client.falixnodes.net/server/network).

4. Click on the "**New Port**{: .blue }" button to allocate an extra port.

5. A new port will be generated under the primary port. The primary port is the port used by the server itself, and the newly generated port is your extra port.

{: .success}

> If your port has successfully been assigned, a toast notification should appear at the top right of the page saying "Port has been added".
