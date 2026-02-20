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
    - Deka
    - Metr
    - Korbs
---

{: .warning }
> Server proxies like BungeeCord aren't available on free plan.

### What is it?
[BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) (created by the [SpigotMC](https://www.spigotmc.org/XenStaff/) team) is a proxy designed to seamlessly connect multiple Minecraft servers, allowing players to navigate between them without leaving the server. 

BungeeCord is compatible with many servers: Spigot, Purpur, PaperMC, and more. It will **NOT** work on Forge, Fabric or Vanilla servers.

{: .warning }
> BungeeCord is an outdated server proxy and Velocity should be used for modern servers instead.

## Preparing the fallback servers
Fallback servers are all servers connected to your BungeeCord proxy.

1. Login to the [Dashboard](https://client.falixnodes.net/).

2. Select a fallback server from your server list.

3. You will be redirected to the [Console](https://client.falixnodes.net/server/console) of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Locate and open `server.properties`.

6. Scroll down and set `online-mode` to `false`.

7. Save the file and return to the File Manager.

8. Locate and open `spigot.yml`.

9. Set `bungeecord` to `true`.

## Creating and configuring the proxy 

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Go to the Versions page and install BungeeCord.

4. Start your server.

5. Click Stop, then click Kill.

6. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

7. Locate and open `config.yml`.

8. Scroll down to `servers:` and use the following template:

  ```yaml
    server-name:
      motd: '&1Just another BungeeCord - Forced Host'
      address: server-IP:PORT
      restricted: false
  ```
  Change `server-name` to the fallback server name (case-sensitive).
  Change `server-IP:PORT` to the IP with port of the fallback server, you can find the IP with port in the Connect tab in the console.

  {: .note }
  > `restricted: true` will disallow players to join the server unless they have the `bungeecord.server.SERVERNAME` permission.

  {: .note }
  > If you have multiple fallback servers, duplicate the above template and paste it under your first server.

9. Scroll down to `priorities: lobby`, change `lobby` to the name of your default fallback server (case-sensitive). This will be the default server that users will be redirected to when they join your BungeeCord server.

10. Scroll down to `host: 0.0.0.0:25577` and change the port value after `:` to your BungeeCord server's port. You can find your port in the Network tab in the Advanced category.

11. Scroll down and set `IP_forward` to `true`.

12. Save the file and restart your server.

13. Make sure both your proxy and fallback servers are running.

14. Connect your server to the IP of the proxy.

## BungeeCord Commands

These are the most often used BungeeCord commands:

| Command                   | Description                                           | Permission                | Group       |
|---------------------------|-------------------------------------------------------|---------------------------|-------------|
| /server \<server>          | Moves you to the desired server.                      | bungeecord.command.server | everyone    |
| /glist                    | Lists all players on the network.                     | bungeecord.command.list   | everyone    |
| /send \<player> \<server>   | Sends the specified player to the specified server.   | bungeecord.command.send   | admin-only  |
| /greload                  | Reloads the configuration.                            | bungeecord.command.reload | admin-only  |
| /find \<player>            | Finds the server that the player is on.               | bungeecord.command.find   | admin-only  |
| /end                      | Stops the BungeeCord server.                          | bungeecord.command.end    | admin-only  |

A full list of BungeeCord commands can be found [here](https://www.spigotmc.org/wiki/bungeecord-commands/).
