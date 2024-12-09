---
layout: post
title: How To Add Modpacks to Your Server
category: Modifications
tags: General
permalink: minecraft/modifications/general/adding-mod
description: Learn how to upload and install mods to your Minecraft Java server.
keywords:
    - keyword: modpacks
      matches: &mods_matches ["install", "use", "get", "add", "configure", "load", "put", "upload"]
    - keyword: modpak
      matches: *mods_matches
author:
    - TWIXhunter
---

Minecraft modpacks are user-created modifications or additions to the game that alter or enhance the game-play experience. Modpacks can range from simple tweaks to the game's mechanics to extensive overhauls that add new features, items, entities, and much more.


## :pickup_truck: Mod Loaders:

Due to how modpacks work, a mod loader is needed as a server software to inject and run the mods itself, with some modpacks only supporting specific mod loaders and sometimes very specific versions. Unfortunately only a single mod loader can be used at a time within a setup, and therefore all mods and modpacks used must support the mod loader. To learn more about mod loaders, please refer to the [Modded Server Jar](/minecraft/java/general/server-software#modded-server-jars) section of our server software guide.

When it comes to forks, as fork mod loaders are based on the upstream mod loader, most if not all upstream mods should work on forked mod loaders, meaning Fabric modpacks should still work when using Quilt, and the same applies to Forge modpacks used with the NeoForge mod loader.

## :mag: Finding Mods:

Mods are often hosted on modding platforms, these are websites that contain a large collection of mods for the user to browse through and choose, the most common ones being:

-   [Modrinth](https://modrinth.com/modpacks)
-   [CurseForge](https://www.curseforge.com/minecraft/search)
-   [FTB](https://www.feed-the-beast.com/modpacks?sort=featured)
-   [Technic](https://www.technicpack.net/modpacks)
## :hammer_and_wrench: Installing and Configuring Mods:

### Through the Modpack Installer:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Server" then navigate to [Modpacks](https://client.falixnodes.net/server/modpacks).

4. To look for modpacks, type the mod name in the "Search Modpacks" field, then click on "**Search**{: .blue }".

5. Locate your modpack within the search results, then click on "**Install**{: .blue }" to download the modpack to your server.

6. (Re)start your server to apply the mod.

### Manually Installing Mods:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Delete all files in the File Manager.

5. Download the modpack from it's official page. Make sure to select the version and mod loader matching your server.

6. In the Dashboard, click on "**Upload Files**{: .blue }".

7. Find the downloaded modpack (this shoud be an archived file) and select it, then upload it to your server.

8. Unarchive the file by pressing on the 3 dots and choosing 'unarchive'

9. In the top navigation bar, hover over "server" then navigate to the [versions page](https://client.falixnodes.net/server/versions).

10. choose and install the modloader required by the modpack

{: .warning}
> Make sure to select the right version, more information about what version to install can usualy be found on the modpacks site.

### Configuration

Many mods include the option to configure and adjust the mod to fit your needs, either by adjusting the changed mechanics or by enabling or disabling features. These options can be found within the configuration file which can be found by following these steps:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [config](https://client.falixnodes.net/server/filemanager?dir=/config/) folder.

5. This is where all the mod configuration folders are stored, to access certain mod settings open the folder matching the mod you want to adjust.

6. You will be greeted by a main configuration file, and sometimes many smaller files, any changes made here will affect how your mods will function.

7. To apply your changes simply (re)start the server.

> Some mods may store their configuration folder in the server's root
