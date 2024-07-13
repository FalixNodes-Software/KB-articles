---
layout: help/article
title:  "Configure plugin Skin Restorer - Falix"
categories: Minecraft
icon: <i class='fa-light fa-puzzle'></i>
tags: plugins
permalink: /help/minecraft/plugins/skin-restorer.*
gitURL: _posts/minecraft/plugins/2022-10-16-skin-restorer.md
description: "Configure Skin Restorer for your Minecraft Server at Falix"

author: Korbs
authorGitHub: korbsstudio
---

<div class="install-plugin">
    <img style="border-radius: 0px;" src="https://www.spigotmc.org/data/resource_icons/2/2124.jpg">
    <h2>Skin Restorer</h2>
    <h3>Developers: SRTeam</h3>
    <a href="https://www.spigotmc.org/resources/skinsrestorer.2124/">Download this Plugin</a>
</div>

<div class="watch-video-tutorial">
    <h1>Video Tutorial</h1>
    <iframe id="video-tutorial" width="560" height="315" src="https://www.youtube-nocookie.com/embed/T9bYwNB0AVk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    <hr>
    <style>section#video-tutorial {display: inherit !important;}</style>
</div>

![Players](/assets/images/posts/plugins/skin-restorer/players.png)

# What and Why?
When operating a crack server, you must set 'online-mode' to 'false.' This, however, causes skins to stop working, causing all players who join your server to identify with a Steve or Alex skin. To resolve this situation with crack servers, you'll need to include a plugin that can restore players' skin, which is where Skin Restorer comes in. Using Skin Restorer allows users to join with the skin associated with their in-game name.

The reason why skins don't load in the first place, is because crack servers don't authenticate with the Mojang skin server.

{: .note #warning }
> If you are running a cracked server, please make sure that you've set it up to be safe and secured. Setting `online-mode` to `false` can make your server vulnerable.

## Installation
**Plugins Tab**
1. Go to Game Panel and select your server
2. Click on the Plugins tab
3. Search for Skin Restorer by SRTeam and click Install
4. Restart server

**SFTP**
1. Download [Skin Restorer](https://www.spigotmc.org/resources/skinsrestorer.2124/)
2. Connect to your server with an SFTP client
3. Look for the "plugins" folder
4. Upload the .jar file to the "plugins"
5. Restart server

**BungeeCord (SFTP)**
1. Download [Skin Restorer](https://www.spigotmc.org/resources/skinsrestorer.2124/)
2. Connect to your servers with an SFTP client
3. Look for the "plugins" folder on all servers, including BungeeCord
4. Upload the .jar file to the "plugins"
5. Restart servers

**Sponge (SFTP)**
1. Download [Skin Restorer](https://www.spigotmc.org/resources/skinsrestorer.2124/)
2. Connect to your servers with an SFTP client
3. Look for the "mods" folder on all servers, including BungeeCord
4. Upload the .jar file to the "mods"
5. Restart servers

## Commands
- `/skin` - main command.
- `/skin <skinname>` - Sets your skin.
- `/skin url <skin.png url> [steve / slim]` - set a skin from a .png url
- `/skin update` - Updates your current skin.
- `/skin clear` - clears your skin.
- `/skins` - GUI

Admin commands:
- `/sr` - main admin command
- `/skin set <playername> <skinname>` - Sets player's skin.
- `/skin clear <player>` - clear a player's skin.
- `/skin update <player>` update a player's skin.
- `/sr drop <skinname>` - Removes skins data from database.
- `/sr createcustom <name> <skin.png url>` - Define a usable custom skin.
- `/sr reload` - Reloads config and locale.
- `/sr props <playername>` - Returns properties of a player.
- `/sr status` - check the plugin status.

## Additional Permissions
- `skinsrestorer.bypasscooldown` -> bypasses skinscooldown config
- `skinsrestorer.bypassdisabled` -> bypass the disabledskins list