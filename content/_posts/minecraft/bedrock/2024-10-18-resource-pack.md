---
title: How To Add Resource Packs To Your Minecraft Bedrock Server
tags: Customization
description: Change Minecraft's look with a server resource pack to give blocks and textures a new look and feel.
keywords:
    - keyword: pack
      matches: &pack_matches ["resource", "texture", "sound"]
    - keyword: custom
      matches: *pack_matches
permalink: /minecraft/bedrock/customization/resource-pack
author:
    - Kuroi
    - Mocab
---

Adding a resource pack to your Minecraft server can greatly enrich the player experience and maintain server aesthetics by altering the game's textures, sounds and font without altering the game's code directly. Resource packs are client side modifications and are therefore sent to individual players from the server to be stored and run on their own device.

This guide will demonstrate how to add a server-wide resource pack popup to allow users to enable and use a specified resource pack, or alternatively, enforce it for all players.

## Acquiring a Resource Pack

There are several popular websites where you can find a variety of resource packs for the Minecraft Bedrock Edition. Here are some of the most well-known ones:

-   [Planet Minecraft](https://www.planetminecraft.com/ "A popular platform for sharing Minecraft content, including resource packs, maps, and skins. The site has a dedicated section for Bedrock Edition.")
-   [MCPE DL](https://mcpedl.com/ "A website specifically focused on Minecraft Pocket Edition and Bedrock Edition, offering a wide range of resource packs, mods, maps, and more.")
-   [Minecraft Forum](https://www.minecraftforum.net/ "A long-standing community forum for Minecraft players, featuring a section dedicated to resource packs for all editions, including Bedrock.")
-   [Curseforge](https://www.curseforge.com/minecraft-bedrock "Known for hosting mods and addons for various games, CurseForge also has a section for Minecraft Bedrock Edition resource packs.")

You can also upload your own custom resource pack as well.

{: .warning}

> Ensure the resource pack is compatible with the version of Minecraft used and any addons or behavior packs installed. Incompatible packs may cause crashes or visual glitches.

## Installation

### Obtaining the Pack Metadata

1. Download the resource pack. If the file is in the `.mcpack` format, rename the file extension to the `.zip` format.

    ![Renaming to zip](/content/assets/images/posts/resource-pack/rename.webp)

2. Extract the file to reveal it's content.

3. Open the "manifest.json" file in the extracted folder using a text editor. Then copy the "uuid" value under "header". The format should resemble the string below:

    ```
    xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
    ```

### Adding to the Server

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the "resource_packs" folder. You should notice two other folders called "chemistry" and "vanilla" within this folder. If so you are on the right track!

5. Click on "**Upload Files**{: .blue }", then select and upload the `.zip` resource pack.

6. Once the upload is complete, click on the 3 dots to the right of the uploaded `.zip` file. Then click "Unarchive". Once this process is completed, you may delete the `.zip` file as it is no longer needed.

7. Navigate back to the [root directory](https://client.falixnodes.net/server/filemanager?dir=/) by clicking on the "Go Back" button at the top of your file list or by returning to the [File Manager](https://client.falixnodes.net/server/filemanager?dir=/).

8. Locate and open the "worlds" folder, this is where all your world folder will be stored. Find and open your current world folder, this is often called `Bedrock level` unless changed.

9. Click on "Create File" and name it as `world_resource_packs.json`.

10. Open the newly created file and paste the following into it:

    ```json
    [
        {
            "pack_id": "manifest.json UUID",
            "version": [0, 0, 0]
        }
    ]
    ```

    > To add multiple resource packs, simply add a comma (`,`) after the closing curly brackets (`}`) and paste in all the content between and including the curly brackets (`{` `}`).

11. Set the value of "pack_id" to the "uuid" we copied before.

    ![manifest-packid](/content/assets/images/posts/resource-pack/manifest-packid.webp)
    ![pack id](/content/assets/images/posts/resource-pack/BedrockPackID.webp)

12. Replace the `version` value with the "version" provided from the "manifest.json" file.
    ![manifest-ver](/content/assets/images/posts/resource-pack/manifest-ver.webp)
    ![version](/content/assets/images/posts/resource-pack/BedrockResourceVer.webp)

13. Save the file by clicking on "**Save File**{: .green }".

14. (Re)start your server.

{: .success}

> If you have successfully added the resource pack, you should be prompted with a "Download Resource Pack?" popup the next time you join the server.

## Configuration

### Enforcing the Resource Pack

By default, players will be prompted if they wish to download and install the resource pack, giving them the option to deny. If you wish all your players to use it, you may want to enforce it by follow the steps below:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Server" then navigate to [Server Properties](https://client.falixnodes.net/server/properties).

4. Find and set `texturepack-required` to `Enabled`.

5. To save your changes, click on "**Submit**{: .blue }" at the top of the list.

6. (Re)start your server.
