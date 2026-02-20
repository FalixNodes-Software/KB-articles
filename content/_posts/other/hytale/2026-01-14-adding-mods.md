---
layout: post
title: How To Add Mods to Your Hytale Server
category: Hytale
tags: Essentials
permalink: /other/hytale/essentials/adding-mods
description: A step-by-step guide to upload and install mods on your Hytale server.
keywords:
    - keyword: mods
      matches: &mods_matches ["install", "use", "get", "add", "configure", "load", "put", "upload"]
    - keyword: mod
      matches: *mods_matches
    - keyword: hytale
      matches: ["mods", "mod"]
author: TWIXhunter
---

Hytale mods are user-created modifications or additions to the game that alter or enhance the gameplay experience. Mods can range from simple tweaks to the game's mechanics to extensive overhauls that add new features, items, entities, and much more.

{: .warning }
> Hytale server hosting requires the official Hytale Game to be purchased.


## Finding Mods

Hytale mods can be downloaded from [CurseForge](https://www.curseforge.com/hytale), which hosts a large collection of mods for you to browse through and choose from. Make sure to download mods that are compatible with your server version.

## Installing Mods

{% tabs installation %}

{% tab installation Mods Page %}

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select your Hytale server from the server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the navigation menu, open the "Hytale" category and navigate to **Mods**.

4. To search for mods, type the mod name in the "Search Mods" field, then click on "**Search**{: .blue }".

5. Locate your mod within the search results, click on the mod card to view more info and press the **Install Hytale-mod**{: .blue } button.

6. Select the version of your choice and press the download button.

7. (Re)start your server to apply the mod.

{% endtab %}

{% tab installation Manual Upload %}

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select your Hytale server from the server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [mods](https://client.falixnodes.net/server/filemanager?dir=/mods/) folder.

5. Download the mod from [CurseForge](https://www.curseforge.com/hytale/search) or the mod's official page. Make sure to select the version matching your server.

6. In the Dashboard, click on "**Upload Files**{: .blue }".

7. Find the downloaded mod file and select it, then upload it to your server.

8. (Re)start your server to enable the mod.

{: .success}
> Your mod should now be active on your server!

{% endtab %}

{% endtabs %}

## Configuring Mods

Many mods include the option to configure and adjust the mod to fit your needs, either by adjusting the Mechanics or by enabling or disabling certain features. These options can be found within configuration files.

{: .warning}
> You have to restart the server after adding the mods to generate the config files.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select your Hytale server from the server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [Mods](https://client.falixnodes.net/server/filemanager?dir=/mods/) folder.

5. Open the folder of the mod you want to configure.

6. Edit the configuration files by clicking on their names.

7. To apply your changes, simply save the files and (re)start the server.

{: .info}
> Some mods may store their configuration folder in the server's root directory.