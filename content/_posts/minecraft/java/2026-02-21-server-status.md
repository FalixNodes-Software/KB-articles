---
title: Why Does My Minecraft Java Server Show as Offline?
tags: General
permalink: /minecraft/java/general/server-status
description: Understanding what server status information means and how to troubleshoot common connection issues.
keywords:
    - keyword: server
      matches: ["offline", "status", "down"]
    - keyword: can't connect
      matches: ["server"]
    - keyword: TLauncher
      matches: ["connect", "join", "offline"]
    - keyword: DNS
      matches: ["not updated", "propagation"]
author: Mocab
---

When trying to join your server in the Minecraft multiplayer list, you may notice it showing as offline — with a message like "This server is OFFLINE!" and no players connected. This guide covers common reasons why this happens and how to fix it.

## Common Reasons Your Server Shows as Offline

### Your Server Is Not Running

The most common reason is that the server simply has not been started. To start it:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Click on the "**Start**{: .green }" button at the top of the console to turn on your server.

{: .success}
> Once the status indicator above the console changes color from **orange**{: .orange } to **green**{: .green }, your server should be on and ready to accept players.

### DNS Has Not Updated Yet

If you recently created your server or your server's runtime machine has changed, your server domain may not resolve correctly yet. Servers are sometimes moved between different nodes for load balancing, which causes the underlying IP address to change. When this happens, the DNS records need to update to point to the new address, which can take anywhere from a few minutes to several hours.

In the meantime, we recommend using the dynamic IP to connect:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select your server and navigate to the [Console page](https://client.falixnodes.net/server/console).

3. Click on the "**Connect**{: .blue }" button at the top of the console.

4. Use the dynamic IP provided (e.g. `nodename.falixserver.net:xxxxx`) to connect.

{: .info}
> The dynamic IP always points to the correct node, so it will work even while DNS is still updating. Once DNS has fully propagated, you can switch back to your regular server address.

### TLauncher and Other Third-Party Launcher Issues

TLauncher and some other third-party launchers lack SRV record support. SRV records are what allow you to connect using just the hostname (e.g. `myserver.falix.gg`) without specifying a port. Without SRV support, the launcher cannot resolve the correct port automatically.

To connect using these launchers, you must include the port in the server address:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select your server and navigate to the [Console page](https://client.falixnodes.net/server/console).

3. Click on the "**Connect**{: .blue }" button at the top of the console.

4. Copy the alternate IP, which includes the port (e.g. `nodename.falixserver.net:xxxxx`).

5. In your launcher, add the server using the full address with the port included.

{: .info}
> If your launcher does not support SRV records, you will always need to use the full address with the port — the hostname alone will not work.