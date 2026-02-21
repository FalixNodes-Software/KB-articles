---
title: How To Add Plugins to Your Server
tags: Guides
permalink: minecraft/modifications/guides/adding-plugins
description: A step-by-step guide to upload and install plugins on your server.
keywords:
    - keyword: plugins
      matches: &mods_matches ["install", "use", "get", "add", "configure", "load", "put", "upload"]
    - keyword: plugin
      matches: *mods_matches
author:
    - TWIXhunter
    - Deka
    - Mocab
---

Minecraft plugins are server-side user-created modifications or additions to the game that alter or enhance the game-play experience. Plugins can range from simple tweaks to the game's mechanics to extensive overhauls that add new features, items, entities, and much more.

## Server Software With Plugin Support:

Due to how plugins work, a special server software is needed to needed to inject and run the plugin itself, with each plugin supporting a certain server software. To learn more about server software with plugin support, please refer to the [Plugins](/minecraft/java/general/server-software#plugins) section of our server software guide.

As forked server software are based on the upstream server software, all upstream plugins should work on forked server software, meaning Spigot plugins will still work when using Paper and Purpur, and the same applies to Paper plugins used with the Purpur server software.

## Finding Plugins:

Plugins are often hosted on modding platforms, these are websites that contain a large collection of plugins for the user to browse through and choose, the most trusted and common ones being:

-   [Modrinth](https://modrinth.com/plugins)
-   [Hangar](https://hangar.papermc.io)
-   [Spigot Resources](https://www.spigotmc.org/resources/)
-   [Bukkit Dev Portal](https://dev.bukkit.org/bukkit-plugins)

## Installing and Configuring Plugins:

### Through the Plugin Installer:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Minecraft" category and navigate to [Plugins](https://client.falixnodes.net/server/plugins).

4. Choose the plugin server software using the "Plugins Type" dropdown.

    > As mentioned above, Spigot and Bukkit plugins are both supported within the Paper and Purpur server software.

5. To look for plugins, type the plugin name in the "Search Plugins" field, then click on "**Search**{: .blue }".

6. Locate your plugin within the search results, then click on "**Install**{: .blue }" to download the plugin to your server.

7. (Re)start your server to apply the plugin.

### Manually Installing Plugins:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [Plugins](https://client.falixnodes.net/server/filemanager?dir=/plugins/) folder.

5. Download the plugin from it's official page. Make sure to select the version and plugin type supported by your server.

6. In the Dashboard, click on "**Upload Files**{: .blue }".

7. Find the downloaded plugin and select it, then upload it to your server.

8. (Re)start your server to enable the plugin.

### Configuration

Most if not all plugins include the option to configure and adjust the plugin to fit your needs, either by adjusting the changed mechanics or by enabling or disabling features. These options can be found within the configuration file which can be accessed by following these steps:

1. Navigate back to the [plugins](https://client.falixnodes.net/server/filemanager?dir=/plugins/) folder.

2. This is where all the plugin executables and configuration folders are stored, to access certain plugin settings open the folder matching the plugin you wish to adjust.

3. You will be greeted by a main configuration file, and many times other smaller files, any changes made here will affect how your plugins will function.

4. To apply your changes simply (re)start the server.
