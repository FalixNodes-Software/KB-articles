---
title: How To Add Resource Packs To Your Minecraft Java Server
tags: Customization
description: Change Minecraft's look with a server resource pack to give blocks and textures a new look and feel.
keywords:
    - keyword: pack
      matches: &pack_matches ["resource", "texture", "sound"]
    - keyword: custom
      matches: *pack_matches
permalink: /minecraft/java/customization/resource-pack
author:
    - Kuroi
    - Mocab
    - Cakey
    - Deka
---

Adding a resource pack to your Minecraft server can greatly enrich the player experience and maintain server aesthetics by altering the game's textures, sounds and font without altering the game's code directly. Resource packs are client side modifications and are therefore sent to individual players from the server to be stored and run on their own device.

This guide will demonstrate how to add a server-wide resource pack popup to allow users to enable and use a specified resource pack, or alternatively, enforce it for all players.

## Acquiring a Resource Pack

### Finding Resource Packs

There are many popular websites where you can find a variety of resource packs for Minecraft:

-   [Modrinth](https://modrinth.com/resourcepacks "Modrinth is a platform tailored for Minecraft players and mod developers, offering a curated selection of mods, texture packs, and community content.")
-   [Planet Minecraft](https://www.planetminecraft.com/ "A community-driven platform where users share various Minecraft content, including resource packs")
-   [CurseForge](https://curseforge.com/minecraft/texture-packs/ "Known for hosting mods and addons for games, including Minecraft. It features a wide range of resource packs for Java Edition.")
-   [Minecraft Forum](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/resource-packs "A longstanding community forum where players discuss and share Minecraft-related content, including resource packs.")

You can also use your own custom resource pack.

{: .warning}

> Ensure the resource pack is compatible with the version of Minecraft used and any plugins or mods installed. Incompatible packs may cause crashes or visual glitches.

## Accessing the Resource Pack Settings

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the navigation menu, open the "Minecraft" category and navigate to [Server Properties](https://client.falixnodes.net/server/properties).

4. Scroll down to the `Resource Packs` section.

You will see the following options:
- **Require Resource Pack** – force players to use the pack  
- **Resource Pack URL** – direct URL to the pack (auto-filled on upload)  
- **Upload Pack** – upload a `.zip` file  
- **Resource Pack ID** – unique identifier for advanced setups  
- **Resource Pack Prompt** – message shown to players  
- **Resource Pack SHA1** – integrity checksum

---

### Uploading a Resource Pack

> Falix now supports **direct ZIP uploading**, making the process simpler and eliminating the need for external hosting.

To upload a pack:

1. Click **Upload Pack**.
2. Select your resource pack as a **`.zip`** file.
3. After uploading, the **Resource Pack URL** field will automatically populate.

Your archive must:
- Be in `.zip` format  
- Contain the `assets/` folder in the **root**, not inside another directory

Once uploaded, the pack can be delivered to players immediately.

{: .success}

> If you have successfully added the resource pack, you should be prompted with a "Download Resource Pack?" popup the next time you join the server.

### Enforcing the Resource Pack

By default, players will be prompted if they wish to download and install the resource pack, giving them the option to deny. If you wish all your players to use it, you may want to enforce it by follow the steps below:

1. Open and navigate back to the [Server Properties](https://client.falixnodes.net/server/properties) page.

2. Enable `Require Resource Pack`.

3. Save your changes.

4. Restart your server.

When enabled, any player who does not accept resource packs in their Minecraft client settings will be **unable to join**.

### Adding a Custom Download Prompt Message

The **Resource Pack Prompt** field allows you to customize the message shown when players are asked to download the pack.

For example: `Please download our official resource pack for the best gameplay experience.`

This is optional but useful for branding, instructions, or server-specific themes.

### Verifying the Resource Pack Integrity

Although optional, you may want to verify the resource pack file integrity to make sure the correct file and all its contents are correctly downloaded. This can be done with a SHA1 hash by generating a string of characters from the downloaded resource pack on the server side and comparing it with the value specified. If the downloaded file is not integrally sound, a yellow "Invalid sha1 for resource-pack-sha1" text will be shown in the console when the server is started.

The SHA1 hash can be generated by any SHA1 generator of your preference. In this example we will be using [emn178's sha1checksum](https://emn178.github.io/online-tools/sha1_checksum.html).

1. Go to [emn178's sha1checksum](https://emn178.github.io/online-tools/sha1_checksum.html).

2. Upload your resource pack to website, make sure it is in the `.zip` format.

3. A string of characters will be generated. This is the resource pack SHA1 checksum.

4. Open and navigate back to the [Server Properties](https://client.falixnodes.net/server/properties) page.

5. Find and set `Resource Pack SHA1` to your SHA1 checksum.

6. Save your changes.

## Adding Multiple Resource Packs

Minecraft servers support only one active resource pack at a time. The Falix panel also allows uploading only a single pack. If you need features from more than one pack, you may merge them into one resource pack.

### Use a Plugin

[ResourcePackManager](https://modrinth.com/plugin/resourcepackmanager) by MagmaGuy can merge and manage multiple packs automatically.

It will generate a combined pack and handle conflicts, resource pack hosting and updates for you.

### Manually Combining Resource Packs

You can also combine resource packs into a single `.zip` file.

{: .warning }

> It is generally not a good idea to combine resource packs as they may be incompatible with each other or override one another leading to missing or glitchy textures.

1. Extract both resource packs.

2. Merge their `assets` directories.

3. Resolve any file conflicts (textures, models, lang files, etc.).

4. Zip the final merged pack.

[Elmakers' Merge Tool](https://merge.elmakers.com/) can automate this process for you.
