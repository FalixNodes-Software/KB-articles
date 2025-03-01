---
title: How To Add Datapacks To Your Minecraft Java Server
tags: Configuration
description: Modify Minecraft’s gameplay with a server datapack to add new mechanics, custom features, and unique challenges without requiring mods.
keywords:
    - keyword: pack
      matches: &pack_matches ["data"]
    - keywords: datapack
      matches: ["add","custom","server"]

permalink: /minecraft/java/configuration/resource-pack
author:
    - Kuroi
    - Mocab
---

Datapacks allow you to change game mechanics, add custom advancements, loot tables, features, and more-all without the need for external mods. They are server-side modifications, which means they can change gameplay while still allowing vanilla clients to connect without additional downloads.

This guide will walk you through adding a server-wide datapack, either as an optional enhancement or as a mandatory feature.

## Getting a Datapack

### Finding Datapacks

There are several popular websites where you can find a variety of datapacks for Minecraft Java Edition. Here are some of the more popular ones:

- [Modrinth](https://modrinth.com/datapacks) Modrinth is a platform for Minecraft players and developers that offers a curated selection of mods, datapacks, and community content.
- [Planet Minecraft](https://www.planetminecraft.com/data-packs/) A community-driven platform where users share various Minecraft content, including datapacks.
- [Vanilla Tweaks](https://vanillatweaks.net/picker/datapacks/) A collection of high-quality, customizable datapacks that improve gameplay while staying true to vanilla mechanics.
- [Minecraft Forum](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/datapacks) A long-running community forum where players discuss and share Minecraft-related content, including datapacks.

You can also create your own custom datapack.

### Adding the datapack

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. You will be redirected to the [Console Page] of your server (https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage", then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the "[world](https://client.falixnodes.net/server/filemanager?dir=/world/)" folder.

5. Within the world folder, open the "[datapacks](https://client.falixnodes.net/server/filemanager?dir=/world/datapacks/)" folder.

6. Upload the datapacks .zip file or folder to your file manager using the **Upload Files**{:.blue } or **Upload Folder**{:.blue } button.

### Activating the datapack

1. Join your Minecraft server

2. Open the chat window and type the following command
> /datapack enable `filenamehere`

{: .error}
> If your datapack doesn't appear, try running `/datapack list` and then try again, restart your server and/or make sure your datapack is in the right place.
