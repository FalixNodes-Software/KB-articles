---
title: How To Add Modpacks to Your Server
tags: Guides
permalink: minecraft/modifications/guides/adding-modpacks
description: Installing and configuring modpacks in your server.
keywords:
    - keyword: modpacks
      matches: &modpack_matches ["install", "use", "get", "add", "configure", "load", "put", "upload"]
    - keyword: modpack
      matches: *modpack_matches
    - keyword: mod packs
      matches: *modpack_matches
    - keyword: mod pack
      matches: *modpack_matches
author:
    - TWIXhunter
    - Deka
    - Mocab
---

Modpacks are a collections of mods grouped together that enhance or change the gameplay experience. These modpacks can range from minor tweaks to core mechanics to major transformations that introduce new features, items, creatures, and a variety of additional content.

## Modpack Types:

There are three types of modpacks:

-   Server-side: only needs to be installed on the server.
-   Client-side: only needs to be run locally.
-   Both client and server side: must be running on both the server and client.

## Modpack Loaders:

In order to use modpacks, a mod loader is required as the server software to properly load and manage the mods within the pack. Some modpacks only support certain mod loaders or versions, which you can find on the modpack's page. Please refer to the [Modded Server Jar](/minecraft/java/general/server-software#modded-server-jars) section of our Server Software Guide for more information on mod loaders.

> Only one modloader can be used in the server at a time.

## Finding Modpacks:

Modpacks are often hosted on modding platforms; these are websites that contain a large collection of modpacks for you to browse and choose from, the most common ones being:

-   [Modrinth](https://modrinth.com/modpacks)
-   [CurseForge](https://www.curseforge.com/minecraft/search?&class=modpacks)
-   [FTB](https://www.feed-the-beast.com/modpacks)
-   [Technic](https://www.technicpack.net/modpacks)

## Installation:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console). Make sure your server is offline by clicking on the "**Stop**{: .red }" button at the top of the console.

{% tabs Install %}
{% tab Install Modpack Installer %}

{:start="4"} 4. In the navigation menu, open the "Minecraft" category and navigate to [Modpacks](https://client.falixnodes.net/server/modpacks).

5. To search for a modpack, enter its name in the "Search Modpacks" field, then click on "**Search**{: .blue }".

    > If you do not find the modpack you are looking for, try alternating between modpack sources from the "Source" field.

6. Locate your modpack in the search results, then click on "**Install**{: .blue }".

7. A popup with a list of versions and mod loaders will appear; click on "**Install**{: .blue }" beside the appropriate version.

8. Allow a few moments for the modpack to install, then start your server to apply it.

> If your server does not automatically generate a `server.jar` or `unix_args.txt`, install the corresponding software and version in the "Versions" tab.

{% endtab %}
{% tab Install Manual Install %}

The steps below are for general modpack installs; in some cases, modpacks may require further setup or tweaks. As such, we recommend reading through the instructions provided by the modpack creators in addition to these steps:

1. In the Dashboard, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

2. Click on "**Upload Files**{: .blue }" at the top of the file manager and select the downloaded modpack.

3. Click on the three dots to the right of the uploaded modpack, then click on "Unarchive".

4. If an "overrides" folder is generated, click on it to open it.

5. Click on the checkbox at the top of the files list to select all files.

6. A popup should appear, click on "**Move**{: .blue }".

7. Ignore any fields and click on "Move" once again.

    > Some modpacks provide resource pack folders. Delete them and instead follow our [resource pack guide](https://kb.falixnodes.net/minecraft/java/configuration/resource-pack).

8. Start your server to test out your modpack.

{% endtab %}
{% endtabs %}

> If your server does not automatically generate a `server.jar` or `unix_args.txt`, install the corresponding software and version in the "Versions" tab.
