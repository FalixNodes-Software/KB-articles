---
layout: post
title: How to add plugins to your server
category: Modifications
tags: Plugins
permalink: minecraft/modifications/plugins/add-plugins
description: Learn how to upload and install plugins to your Minecraft Java server.
author: The_twix_hunter
toc: false
---

## Using the Plugin Installer

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and locate your server, then click on "Play".

3. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console) page. In the top navigation bar, hover over "Manage", then navigate to [Plugins](https://client.falixnodes.net/server/plugins).

4. Ensure that the "Plugins Type" is set to `Spigot Plugins`.

5. Type the name of your plugin of choice in the "Search Plugins" field, then click on "Search".

6. Locate your plugin within the search results, then click on "Install".

7. Navigate back to the [Console](https://client.falixnodes.net/server/console). Scroll down and on the bottom right of the console, click on the green "Start" button.

## Using the File Manager or SFTP

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and locate your server, then click on "Play".

3. Download the plugin of choice using the search engine of your choice or from your favorite plugin repository like:
    - [CurseForge](https://www.curseforge.com/minecraft/search?page=1&pageSize=20&sortBy=relevancy&class=bukkit-plugins)
    - [Modrinth](https://modrinth.com/plugins)
    - [Hangar](https://hangar.papermc.io)
    - [Spigot Resources](https://www.spigotmc.org/resources/)
    - [Bukkit Dev Portal](https://dev.bukkit.org/bukkit-plugins)

{: .warning}

> Before downloading, take a look at:
> - the Minecraft version of the plugin
> - the modloader needed (any Bukkit/Spigot plugin will work on Paper/Purpur servers)
> and make sure those are the same as your server

4. Navigate to the [FileManager](https://client.falixnodes.net/server/filemanager?dir=/) by hovering over "Manage" and clicking ["FileManager"](https://client.falixnodes.net/server/filemanager?dir=/) or open your SFTP program like FileZilla.

5. Click on the "plugins" folder (if this doesn't show up, then take a look at our versions guide).

6. Press "upload file" and select the plugins you want to upload.

7. Wait for the plugins to upload and (re)start your server.

{: .success}

> Your plugins have been successfully installed!