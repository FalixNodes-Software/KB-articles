---
layout: post
title: How To Add Modpacks to Your Minecraft Server
category: Modifications
tags: General
permalink: minecraft/modifications/general/adding-modpacks
description: how to install and configure modpacks on your Minecraft Java server
keywords:
    - keyword: modpacks
      matches: &mods_matches ["install", "use", "get", "add", "configure", "load", "put", "upload"]
    - keyword: modpack
      matches: *mods_matches
author:
    - TWIXhunter
    - Deka
    - Mocab
---

Minecraft modpacks are curated collections of user-created modifications that enhance or change the gameplay experience. These modpacks can vary from minor adjustments to core mechanics to substantial transformations that introduce new features, items, creatures, and a variety of additional content.


## :pickup_truck: Mod Loaders:

To utilize modpacks, a mod loader is required as server software to properly inject and manage the mods. Some modpacks may support only specific mod loaders or certain versions. It's important to note that only one mod loader can be active at a time, meaning all mods and the selected modpack must be compatible with the chosen mod loader. You can find the appropriate mod loader on the modpacks page. Please refer to the [Modded Server Jar](/minecraft/java/general/server-software#modded-server-jars) section of our server software guide for more information on modloaders.

## :mag: Finding Modspacks:

Modpacks are often hosted on modding platforms; these are websites that contain a large collection of modpacks for you to browse and choose from., the most common ones being:

-   [Modrinth](https://modrinth.com/modpacks)
-   [CurseForge](https://www.curseforge.com/minecraft/search?page=1&pageSize=20&sortBy=relevancy&class=modpacks)
-   [FTB](https://www.feed-the-beast.com/modpacks?sort=featured)
-   [Technic](https://www.technicpack.net/modpacks)

## :hammer_and_wrench: Installing and Configuring:

### Through the Modpack Installer:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Server" then navigate to [Modpacks](https://client.falixnodes.net/server/modpacks).

4. To look for modpacks, type the modpack name in the 'Search Modpacks' field, then click on "**Search**{: .blue }".

5. Locate your modpack within the search results, then click on "**Install**{: .blue }" to download the modpack to your server.

6. (Re)start your server to apply the modpack to your server.

### Manually Installing Mods:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Delete all files in the File Manager.

5. Download the modpack from its official page. Ensure that you select the version and mod loader that match your server.

{: .warning}
> Make sure to download the server pack of the modpack, these can be found under:
    Files > click your version of choice > aditional files > serverpack for curseforge.
    lorepsum > ipsum > work > in > progress(modrinth downtime) for modrinth.

6. In the Dashboard, click on "**Upload Files**{: .blue }".

7. Find the downloaded serverpack (this should be an archived file) and select it, then upload it to your server.

8. Unarchive the file by pressing on the 3 dots and choosing 'unarchive'

9. In the top navigation bar, hover over "server" then navigate to the [versions page](https://client.falixnodes.net/server/versions).

10. Choose and install the modloader required by the modpack

{: .warning}
> Make sure to select the right version, more information about what version to install can usuall be found on the modpacks site.

### Configuration

Many mods inside the modpack will have options that allow you to customize and tweak the mods to suit your preferences. This can include modifying mechanics or enabling and disabling specific features. To access these options, you can find the configuration file by following these steps:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

> Ensure that the server has been started at least once before proceeding with these steps

4. Locate and open the [config](https://client.falixnodes.net/server/filemanager?dir=/config/) folder.

5. This is where all the mod configuration folders are stored, to access certain mod settings open the folder matching the mod you want to adjust.

6. You will encounter a main configuration file, and possibly several smaller files, any changes made in these files will affect how your mods will function.

7. To apply your changes simply (re)start the server.

> Some mods may store their configuration folder in the server's root.
