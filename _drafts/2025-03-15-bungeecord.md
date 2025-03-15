---
title: How To Setup And Install A Bungeecord Proxy
tags: General
permalink: yet to be seen
description: A step-by-step guide on how to install and use a bungeecord proxy server/
keywords:
    - keyword: bungeecord
      matches: &bungee_matches ["install", "use", "get", "add", "configure", "load"]
    - keyword: bungee
      matches: *bungee_matches
author:
    - TWIXhunter
    - korbs
---

### What Is It?
[BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) (created by the [SpigotMC](https://www.spigotmc.org/XenStaff/) team) is a proxy designed to seamlessly connect multiple Minecraft servers together, allowing players to navigate between them without leaving the game. 

BungeeCord is compatible with Spigot, Purpur, PaperMC, and any Spigot fork. It will **NOT** function on Forge/Fabric or vanilla servers.

### What is it useful for?
BungeeCord is very beneficial for server administrators that want to separate their server's activities (such as minigames, creative, survival, and so on). BungeeCord is utilized and trusted by notable servers such as [Hypixel](https://hypixel.net/), [Mineplex](https://www.mineplex.com/home/), [HiveMC](https://hivemc.com/), and much more.

## Preparing The Fallback Servers
Fallback servers are all servers connected to your BungeeCord proxy.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a fallback server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

5. Locate and open `server.properties`.

6. Scroll down and set `online-mode` to `false`.

7. Return to the File Manager.

8. Locate and open `spigot.yml`.

9. Set `bungeecord` to `true`.

10. Restart the server.

Repeat the steps above for all your fallback servers.

## Creating And Configuring The Proxy 

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. Go to the versions page and install Bungeecord.

4. Start your server.

{: .note }
> Do not rely on the server status at the top left of the page, it does not indicate the status of proxy servers correctly.

7. Click on "Stop", then click "Kill".

8. In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

9. Locate `config.yml` and open it.

10. Scroll down to `host: 0.0.0.0:25577` and change the numbers after `:` to your BungeeCord's port. You can find your port in the "Network" tab under the advanced category.

11. Scroll down to `priorities:- lobby`, change `lobby` to your default fallback server's name (case sensitive). This will be the default server that users will be redirected to when they join your BungeeCord server.

12. Scroll down and set `IP_forward` to `true`.

13. Scroll down to `servers:` and use the template below:

{: .note #code }
```
  server-name:
    motd: '&1Just another BungeeCord - Forced Host'
    address: server-IP:PORT
    restricted: false
```
Change `server-name` to the fallback server's name (case sensitive).
Change `server-IP:PORT`  to the fallback server's IP and port, you can find the "Ip with port" in the connect tab in the console.

{: .note }
> Restricted does not allow players to join the server unless they have the `bungeecord.server.SERVERNAME` permission.

{: .note }
> If you have multiple fallback servers, duplicate the code above and paste it under your first server.

13. Save the file and start your server.

{: .note }
> You can view all BungeeCord configuration options [here](https://www.spigotmc.org/wiki/bungeecord-configuration-guide/).

14. Make sure that both your proxy and fallback servers are running.

15. Join your server on the IP of the proxy.

## BungeeCord Commands
You can find a list of BungeeCord commands [here](https://www.spigotmc.org/wiki/bungeecord-commands/).

### In Game
Players, including you (of course), can easily teleport to the other servers on your network by using the `/server` command in-game. Then they can use their cursor to click on the server they want to go to. They can also do `/server <name>`, like `/server lobby`.

This command requires the `bungeecord.command.server` permission which is granted to everyone by default.