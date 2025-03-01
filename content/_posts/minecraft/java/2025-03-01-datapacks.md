---
title: How To Add Datapacks To Your Minecraft Java Server
tags: Configuration
description: description yet to be made up.
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

Datapacks allow you to modify game mechanics, add custom advancements, loot tables, functions, and more—all without requiring external mods. They are server-side modifications, meaning they can alter gameplay while still allowing vanilla clients to connect without additional downloads.

This guide will walk you through adding a server-wide datapack, either as an optional enhancement or an enforced feature.

## Acquiring a Datapack

### Finding Datapacks

There are several popular websites where you can find a variety of datapacks for Minecraft Java Edition. Here are some of the most well-known ones:

-   [Modrinth](https://modrinth.com/datapacks) Modrinth is a platform tailored for Minecraft players and developers, offering a curated selection of mods, datapacks, and community content.
-   [Planet Minecraft](https://www.planetminecraft.com/data-packs/) A community-driven platform where users share various Minecraft content, including datapacks.
-   [Vanilla Tweaks](https://vanillatweaks.net/picker/datapacks/) A collection of high-quality, customizable datapacks that enhance gameplay while staying true to vanilla mechanics."
-   [Minecraft Forum](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/datapacks) A longstanding community forum where players discuss and share Minecraft-related content, including datapacks.

You can also create your own custom datapack.

{: .warning}

> Ensure the datapack is compatible with the version of Minecraft you are using. Incompatible datapacks may cause errors, unintended behavior, or fail to load properly.

### Adding the datapack

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the "[world](https://client.falixnodes.net/server/filemanager?dir=/world/)" folder.

5. Inside the world folder, open the "[datapacks](https://client.falixnodes.net/server/filemanager?dir=/world/datapacks/)" folder.

6. Upload the datapacks .zip file or folder to your File Manager using the **upload Files**{: .blue } or **upload Folder**{: .blue } button.

### Enabling the datapack

1. Join your minecraft server

2. Open the chat window and enter the command below
> /datapack enable `filenamehere`

{: .error}
> If your datapack doesn't appear, try running `/datapack list` and then try again or assure that your datapack is in the right location.
