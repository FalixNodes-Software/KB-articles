---
layout: post
title:  "How to add a resource pack to your server"
category: 
    - Bedrock
    - Getting-started
tags: Server
description: "How to make your Bedrock server require a Resource Pack"
permalink: /minecraft/bedrock/server/resource-pack
author: "Kuroi Jigoku"
toc: false
---

## Introduction

Adding a resource pack to your Minecraft server can greatly enrich player experience, maintain server aesthetics, and unlock unique gameplay features not available in vanilla Minecraft. This guide will demonstrate how to require a resource pack for joining your server.

## Acquiring the resource packs

There are several popular websites where you can find a variety of resource packs for Minecraft Bedrock Edition. Here are some of the most well-known ones:

- [Planet Minecraft](https://www.planetminecraft.com/ "A popular platform for sharing Minecraft content, including resource packs, maps, and skins. The site has a dedicated section for Bedrock Edition.")
- [MCPE DL](https://mcpedl.com/ "A website specifically focused on Minecraft Pocket Edition and Bedrock Edition, offering a wide range of resource packs, mods, maps, and more.")
- [Minecraft Forum](https://www.minecraftforum.net/ "A long-standing community forum for Minecraft players, featuring a section dedicated to resource packs for all editions, including Bedrock.")
- [Curseforge](https://www.curseforge.com/minecraft-bedrock "Known for hosting mods and addons for various games, CurseForge also has a section for Minecraft Bedrock Edition resource packs.")

You can also upload your own custom resource pack as well.

{: .warning}

> **Compatibility Issues**: Ensure the resource pack is compatible with the version of Minecraft Bedrock Edition and any server plugins or mods installed. Incompatible packs may cause crashes or visual glitches.

## Installation

1. Download and extract the resource pack. If the file is in `.mcpack` format, rename the file extension to `.zip` format and extract it.
![Renaming to zip](/assets/images/posts/rename.webp)

2. Open the `manifest.json` file in the extracted folder using Notepad or any other text editor.

3. Minimize the file for now, we will need it later on.

> In this tutorial, We will use SFTP for transferring files.
> You may refer to [this tutorial tutorial tutorial](https://kb.falixnodes.net/falix/dashboard/general/sftp)

## Transferring Files

1. Connect to your server's SFTP.

2. Open `resource_packs` folder in your SFTP client.

3. Drag and Drop the extracted resource pack folder you got into this folder.

4. Go back to the home folder

5. Find the following directory `/worlds/[World Name]` ([World Name] is the name of the World folder)

6. Create a New file in this folder named `world_resource_packs.json`.

7. Paste the Following content into the file:

    ```json
    [
        {
            "pack_id" : "Paste uuid from manifest.json here",
            "version" : [ 0, 0, 0 ]
        }
    ]
    ```

8. Replace the `pack_id` value with the **uuid** from the `manifest.json` file we minimized before.
   ![manifest-packid](/assets/images/posts/manifest-packid.webp)
   ![pack id](/assets/images/posts/BedrockPackID.webp)

9. Replace the `version` value with the **version** numbers from the `manifest.json` file.
    ![manifest-ver](/assets/images/posts/manifest-ver.webp)
    ![version](/assets/images/posts/BedrockResourceVer.webp)

10. Save the file.

11. Start or restart your server.

{: .success}

> You have successfully added a Resource Pack to your server.
