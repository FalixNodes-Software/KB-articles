---
title: How To Add Datapacks To Your Minecraft Java Server
tags: Configuration
description: Modify gameplay with a server datapack to add new features without requiring mods or plugins.
keywords:
    - keyword: pack
      matches: &pack_matches ["data"]
    - keyword: datapack
      matches: ["add","custom","server"]
permalink: /minecraft/java/configuration/datapacks
author:
    - TWIXhunter
---

Datapacks allow you to change game mechanics, add custom advancements, loot tables, features, and more-all without the need for external mods. They are server-side modifications, which means they can change gameplay while still allowing vanilla clients to connect without additional downloads.

This guide will walk you through adding a server-wide datapack, either as an optional enhancement or as a mandatory feature.

### Finding Datapacks

There are several popular websites where you can find a variety of datapacks for Minecraft Java Edition. Here are some of the more popular ones:

- [Modrinth](https://modrinth.com/datapacks "Modrinth is a platform for Minecraft players and developers that offers a curated selection of mods, datapacks, and community content.")
- [Planet Minecraft](https://www.planetminecraft.com/data-packs/ "A community-driven platform where users share various Minecraft content, including datapacks.")
- [Vanilla Tweaks](https://vanillatweaks.net/picker/datapacks/ "A collection of high-quality, customizable datapacks that improve gameplay while staying true to vanilla mechanics.")
- [CurseForge](https://www.curseforge.com/minecraft/search?class=data-packs/ "Browse through the selection of Minecrafts mods and datapacks, check out their descriptions and photos, and find out which ones are best for you.")

You can also create your own custom datapack.

### Adding the datapack

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. Open the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the `world` folder.

5. In the `world` folder, open the `datapacks` folder.

6. Upload the datapack `.zip` file or folder.

### Enabling the datapack

1. In the console, execute the following command to enable the datapack: `datapack enable NAME`

> If your datapack is not enabled, try running `datapack list` and checking if it's there. If not, restart your server and make sure your datapack is in the right place.
