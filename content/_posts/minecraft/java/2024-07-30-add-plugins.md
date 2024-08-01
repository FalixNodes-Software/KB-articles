---
layout: post
title: How to add plugins to your server
category: Java
tags: Plugins
permalink: minecraft/java/plugins/add-plugins
description: Learn how to upload and install plugins to your Minecraft Java server.
author:
    - TWIXhunter
    - Deka
toc: false
---

## Using the Plugin Installer

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and locate your server, then click on "Play".

3. Navigate to the [Plugins](https://client.falixnodes.net/server/plugins) tab by hovering over "Manage".

4. Ensure that the "Plugins Type" is set to "Spigot Plugins" or "Bukkit Plugins".

5. Type the name of the plugin in the "Search Plugins" field, then click on "Search".

6. Locate your plugin within the search results, then click on "Install".

7. Start or restart your server.

## Using the File Manager

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and locate your server, then click on "Play".

3. Download the plugin of choice using the search engine of your choice or from your favorite plugin repository like:
    - [Modrinth](https://modrinth.com/plugins)
    - [Hangar](https://hangar.papermc.io)
    - [CurseForge](https://www.curseforge.com/minecraft/search?page=1&class=bukkit-plugins)
    - [Spigot Resources](https://www.spigotmc.org/resources/)
    - [Bukkit Dev Portal](https://dev.bukkit.org/bukkit-plugins)

{: .warning}

> Before downloading, check these:
> - The Minecraft version of the plugin and if it matches with the version on your server
> - The server software needed (Bukkit/Spigot plugins work on Paper/Purpur servers)

4. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage".

5. Navigate to the `plugins` folder.

6. Press "Upload File" and select the plugin you want to upload.

7. Start or restart your server.

## Via SFTP

{: .info}

> Access via SFTP is only available to Premium users.

{: .info}

> You will need an SFTP client, such as [FileZilla](https://filezilla-project.org/download.php?type=client) or [WinSCP](https://winscp.net/eng/download.php).

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and locate your server, then click on "Play".

3. Download the plugin of choice using the search engine of your choice or from your favorite plugin repository like:
    - [Modrinth](https://modrinth.com/plugins)
    - [Hangar](https://hangar.papermc.io)
    - [CurseForge](https://www.curseforge.com/minecraft/search?page=1&class=bukkit-plugins)
    - [Spigot Resources](https://www.spigotmc.org/resources/)
    - [Bukkit Dev Portal](https://dev.bukkit.org/bukkit-plugins)

{: .warning}

> Before downloading, check these:
> - The Minecraft version of the plugin and if it matches with the version on your server
> - The server software needed (Bukkit/Spigot plugins work on Paper/Purpur servers)

4. Navigate to the [FTP Access](https://client.falixnodes.net/server/sftp) tab by hovering over "Advanced".

5. Press "Launch SFTP" or input the credentials manually in your SFTP client.

6. Upload your plugins to the `plugins` folder.

7. Start or restart your server.
