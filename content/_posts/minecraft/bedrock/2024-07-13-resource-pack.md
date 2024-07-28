---
layout: post
title: "Adding Resource Packs to Your Server"
category: Bedrock
tags: Configuration
description: "How to add a resource pack to your server to give blocks and textures a new look and feel."
permalink: /minecraft/bedrock/configuration/resource-pack
author: "Kuroi Jigoku & Mocab"
---

## Introduction

Adding a resource pack to your Minecraft server can greatly enrich the player experience and maintain server aesthetics by altering the game's textures, sounds and font without altering the game's code directly. Resource packs are client side modifications and are therefore sent to individual players from the server to be stored and run on their own device.

This guide will demonstrate how to add a server-wide resource pack popup to allow users to enable and use a specified resource pack, or alternatively, enforce it for all players.

## Acquiring a Resource Pack

There are several popular websites where you can find a variety of resource packs for the Minecraft Bedrock Edition. Here are some of the most well-known ones:

- [Planet Minecraft](https://www.planetminecraft.com/ "A popular platform for sharing Minecraft content, including resource packs, maps, and skins. The site has a dedicated section for Bedrock Edition.")
- [MCPE DL](https://mcpedl.com/ "A website specifically focused on Minecraft Pocket Edition and Bedrock Edition, offering a wide range of resource packs, mods, maps, and more.")
- [Minecraft Forum](https://www.minecraftforum.net/ "A long-standing community forum for Minecraft players, featuring a section dedicated to resource packs for all editions, including Bedrock.")
- [Curseforge](https://www.curseforge.com/minecraft-bedrock "Known for hosting mods and addons for various games, CurseForge also has a section for Minecraft Bedrock Edition resource packs.")

You can also upload your own custom resource pack as well.

{: .warning}

> Ensure the resource pack is compatible with the version of Minecraft used and any addons or behavior packs installed. Incompatible packs may cause crashes or visual glitches.

## Installation

### Obtaining the Resource Pack Metadata

- Download the resource pack.

{: .info}

> If the file is in the `.mcpack` format, rename the file extension to the `.zip` format.

![Renaming to zip](/content/assets/images/posts/rename.webp)

- Extract the archive.

- Open the "manifest.json" file in the extracted folder using a text editor. Then copy the "uuid" value under "header". The format should resemble the string below:

    ```json
    xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
    ```

### Adding the Resource Pack to the Server

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and choose a server, then click on "Play".

3. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager?dir=/).

4. Navigate to the `resource_packs` folder. You should notice two other folders called `chemistry` and `vanilla` within this folder.

5. Press "Upload Files", then select and upload the `.zip` resource pack.

6. Once the upload is complete, press the 3 dots to the right of the uploaded `.zip` file. Then press "Unarchive". Once this process is completed, you may delete the `.zip` file as it is no longer needed.

7. Navigate back to the [root directory](https://client.falixnodes.net/server/filemanager?dir=/) by clicking on the "Go Back" button at the top of your file list or by reopening the [File Manager](https://client.falixnodes.net/server/filemanager?dir=/).

8. Navigate to the `worlds` folder, this is where all your worlds are stored. Navigate to your current world folder, this is often called `Bedrock level` unless changed.

9. Press "Create File" and name it `world_resource_packs.json`.

10. Open the newly created file and paste the following:

    ```json
    [
        {
            "pack_id": "manifest.json UUID",
            "version": [0, 0, 0]
        }
    ]
    ```

    > To add multiple resource packs, simply add a comma (`,`) after the closing curly brackets (`}`) and paste in all the content between and including the curly brackets (`{` `}`).

11. Set the value of `pack_id` to the "uuid" we copied before.

    ![manifest-packid](/content/assets/images/posts/manifest-packid.webp)
    ![pack id](/content/assets/images/posts/BedrockPackID.webp)

12. Replace the `version` value with the "version" provided from the `manifest.json` file.
    ![manifest-ver](/content/assets/images/posts/manifest-ver.webp)
    ![version](/content/assets/images/posts/BedrockResourceVer.webp)

13. Save the file.

14. Start or restart your server.

{: .success}

> If you have successfully added the resource pack, you should be prompted with a "Download Resource Pack?" popup the next time you join the server.

## Configuration

### Enforcing the Resource Pack

By default, players will be prompted if they wish to download and install the resource pack, giving them the option to deny. If you wish all your players to use it, you may want to enforce it by follow the steps below:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and choose a server, then click on "Play".

3. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [Server Properties](https://client.falixnodes.net/server/properties) tab.

4. Find and set `texturepack-required` to `Enabled`.

5. To save your changes, click on "Submit" at the top of the list.

6. Start or restart your server.
