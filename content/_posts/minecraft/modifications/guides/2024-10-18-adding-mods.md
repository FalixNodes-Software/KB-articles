---
title: How To Add Mods to Your Server
tags: Guides
permalink: minecraft/modifications/guides/adding-mods
description: A step-by-step guide to upload and install mods on your server.
keywords:
    - keyword: mods
      matches: &mods_matches ["install", "use", "get", "add", "configure", "load", "put", "upload"]
    - keyword: mod
      matches: *mods_matches
author:
    - TWIXhunter
    - Deka
    - Mocab
---

Minecraft mods are user-created modifications or additions to the game that alter or enhance the game-play experience. Mods can range from simple tweaks to the game's mechanics to extensive overhauls that add new features, items, entities, and much more.

## Mod Types:

There are three types of mods: server-side, client-side and both. Depending on the mod specification, some mods are only to be run locally, while others are server-side only, with the majority requiring it to be installed on both ends. If the mod used is of the last type, if the player does not have the mod installed locally, they will not be able to experience or interact with the mod at all.

## Mod Loaders:

Due to how mods work, a mod loader is needed as a server software to inject and run the mod itself, with some mods only supporting specific mod loaders and sometimes very specific versions. Unfortunately only a single mod loader can be used at a time within a setup, and therefore all mods used must support the mod loader. To learn more about mod loaders, please refer to the [Modded Server Jar](/minecraft/java/general/server-software#modded-server-jars) section of our server software guide.

When it comes to forks, as fork mod loaders are based on the upstream mod loader, most if not all upstream mods should work on forked mod loaders, meaning Fabric mods should still work when using Quilt, and the same applies to Forge mods used with the NeoForge mod loader.

## Finding Mods:

Mods are often hosted on modding platforms, these are websites that contain a large collection of mods for the user to browse through and choose, the most common ones being:

-   [Modrinth](https://modrinth.com/mods)
-   [CurseForge](https://www.curseforge.com/minecraft/search)

## Installing and Configuring Mods:

### Through the Mods Installer:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Minecraft" category and navigate to [Mods](https://client.falixnodes.net/server/mods).

4. To look for mods, type the mod name in the "Search Mods" field, then click on "**Search**{: .blue }".

5. Locate your mod within the search results, then click on "**Install**{: .blue }" to download the mod to your server.

6. (Re)start your server to apply the mod.

### Manually Installing Mods:

{: .warning}
> Manual installation is possible only on Premium plans.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [mods](https://client.falixnodes.net/server/filemanager?dir=/mods/) folder.

5. Download the mod from it's official page. Make sure to select the version and mod loader matching your server.

6. In the Dashboard, click on "**Upload Files**{: .blue }".

7. Find the downloaded mod and select it, then upload it to your server.

8. (Re)start your server to enable the mod.

### Configuration

Many mods include the option to configure and adjust the mod to fit your needs, either by adjusting the changed mechanics or by enabling or disabling features. These options can be found within the configuration file which can be found by following these steps:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [config](https://client.falixnodes.net/server/filemanager?dir=/config/) folder.

5. This is where all the mod configuration folders are stored, to access certain mod settings open the folder matching the mod you want to adjust.

6. You will be greeted by a main configuration file, and sometimes many smaller files, any changes made here will affect how your mods will function.

7. To apply your changes simply (re)start the server.

> Some mods may store their configuration folder in the server's root
