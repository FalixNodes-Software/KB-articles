---
title: How To Setup And Install A BungeeCord Proxy
tags: Proxy
permalink: minecraft/java/proxy/bungeecord
description: A step-by-step guide on how to install and use a BungeeCord proxy server
keywords:
    - keyword: bungeecord
      matches: &bungee_matches ["install", "use", "get", "add", "configure", "load"]
    - keyword: bungee
      matches: *bungee_matches
author:
    - TWIXhunter
    - Korbs
---

### What is it?
[BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) (created by the [SpigotMC](https://www.spigotmc.org/XenStaff/) team) is a proxy designed to seamlessly connect multiple Minecraft servers, allowing players to navigate between them without leaving the game. 

BungeeCord is compatible with Spigot, Purpur, PaperMC, and any Spigot fork. It will **NOT** work on Forge/Fabric or Vanilla servers.

{: .error }
> Server networks and proxies like BungeeCord aren't available on free plan.

### What is it useful for?
BungeeCord is very useful for server administrators who want to separate their server's activities (such as minigames, creative, survival, and so on). BungeeCord is used and trusted by notable servers like [Hypixel](https://hypixel.net/), [Mineplex](https://www.mineplex.com/home/), [HiveMC](https://hivemc.com/) and many more.

## Preparing the fallback servers
Fallback servers are all servers connected to your BungeeCord proxy.

1. Login to the [Dashboard](https://client.falixnodes.net/).

2. Select a fallback server from your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Locate and open 'server.properties'.

6. Scroll down and set `online mode' to `false'.

7. Save the file and return to the file manager.

8. Locate and open `spigot.yml`.

9. Set `bungeecord` to `true`.

## Creating and Configuring the Proxy 

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Go to the Versions page and install BungeeCord.

4. Start your server.

{: .note }
> Do not rely on the server status at the top left of the page, it does not indicate the status of proxy servers correctly.

7. Click Stop, then click Kill.

8. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

9. Locate and open `config.yml`.

10. Scroll down to `servers:` (line 9) and use the following template:

```YAML
  server name:
    motd: '&1Just another BungeeCord - Forced Host'
    address: server-IP:PORT
    restricted: false
```
Change `server-name` to the fallback server name (case sensitive).
Change `server-IP:PORT` to the Dynamic IP of the fallback server, you can find the Dynamic IP in the Connect tab in the console.

{: .note }
> Restricted will not allow players to join the server unless they have the `bungeecord.server.SERVERNAME` permission.

{: .note }
> If you have multiple fallback servers, duplicate the above code and paste it under your first server.

11. Scroll down to `priorities:- lobby` (line 24), change `lobby` to the name of your default fallback server (case sensitive). This will be the default server that users will be redirected to when they join your BungeeCord server.

12. Scroll down to `host: 0.0.0.0:25577` (line 27) and change the numbers after `:` to your BungeeCord's port. You can find your port in the Network tab under the Advanced category. 

13. Scroll down and set `IP_forward` to `true`. (line 46)

14. Save the file and restart your server.

{: .note }
> You can view all BungeeCord configuration options [here](https://www.spigotmc.org/wiki/bungeecord-configuration-guide/).

15. Make sure both your proxy and fallback servers are running.

16. Connect your server to the IP of the proxy.

## BungeeCord Commands
A list of BungeeCord commands can be found [here](https://www.spigotmc.org/wiki/bungeecord-commands/).

### In Game
Players, including you (of course), can easily teleport to the other servers on your network by using the `/server` command in game. They can then use their cursor to click on the server they want to go to. You can also do `/server <name>`, like `/server lobby`.

This command requires the `bungeecord.command.server` permission, which is granted to everyone by default.
