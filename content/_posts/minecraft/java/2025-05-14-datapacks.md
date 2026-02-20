---
title: How To Add Data Packs To Your Minecraft Java Server
tags: Customization
description: Modify gameplay with a server data pack to add new features without requiring mods or plugins.
keywords:
    - keyword: pack
      matches: &pack_matches ["data"]
    - keyword: datapack
      matches: ["add","custom","server", "put"]
permalink: /minecraft/java/customization/datapacks
author:
    - TWIXhunter
    - Deka
---

## What are data packs?

A data pack is a collection of data used to configure a number of features of Minecraft. Data packs are used to define among others advancements, dimensions, enchantments, loot tables, recipes, structures, and biomes without the need for plugins or mods.

### Finding data packs:

There are many websites where you can find a variety of data packs for Minecraft. Here is a list of the most popular ones:

- [Modrinth](https://modrinth.com/datapacks/)
- [Planet Minecraft](https://www.planetminecraft.com/data-packs/)
- [Vanilla Tweaks](https://vanillatweaks.net/picker/datapacks/)
- [CurseForge](https://www.curseforge.com/minecraft/search?class=data-packs)

### Adding data packs:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Open the `world` folder.

5. Open the `datapacks` folder.

6. Upload the data pack. It can be a `.zip` file or a folder.

### Enabling data packs:

1. Open the [Console](https://client.falixnodes.net/server/console).

2. Execute the following command to list all data packs: `datapack list`

3. Execute the following command to enable a data pack: `datapack enable NAME`
