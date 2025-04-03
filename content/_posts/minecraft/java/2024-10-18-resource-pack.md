---
title: How To Add Resource Packs To Your Minecraft Java Server
tags: Configuration
description: Change Minecraft's look with a server resource pack to give blocks and textures a new look and feel.
keywords:
    - keyword: pack
      matches: &pack_matches ["resource", "texture", "sound"]
    - keyword: custom
      matches: *pack_matches
permalink: /minecraft/java/configuration/resource-pack
author:
    - Kuroi
    - Mocab
---

Adding a resource pack to your Minecraft server can greatly enrich the player experience and maintain server aesthetics by altering the game's textures, sounds and font without altering the game's code directly. Resource packs are client side modifications and are therefore sent to individual players from the server to be stored and run on their own device.

This guide will demonstrate how to add a server-wide resource pack popup to allow users to enable and use a specified resource pack, or alternatively, enforce it for all players.

## Acquiring a Resource Pack

### Finding Resource Packs

There are several popular websites where you can find a variety of resource packs for the Minecraft Bedrock Edition. Here are some of the most well-known ones:

-   [Modrinth](https://modrinth.com/resourcepacks "Modrinth is a platform tailored for Minecraft players and mod developers, offering a curated selection of mods, texture packs, and community content.")
-   [Planet Minecraft](https://www.planetminecraft.com/ "A community-driven platform where users share various Minecraft content, including resource packs")
-   [CurseForge](https://curseforge.com/minecraft/texture-packs/ "Known for hosting mods and addons for games, including Minecraft. It features a wide range of resource packs for Java Edition.")
-   [Minecraft Forum](https://www.minecraftforum.net/forums/mapping-and-modding-java-edition/resource-packs "A longstanding community forum where players discuss and share Minecraft-related content, including resource packs.")

You can also use your own custom resource pack.

{: .warning}

> Ensure the resource pack is compatible with the version of Minecraft used and any plugins or mods installed. Incompatible packs may cause crashes or visual glitches.

### Obtaining a Download Link

To add a resource pack to your server, you must provide a **direct** download link to the resource pack as a `.zip` file. This could either be obtained directly from the website hosting the resource pack, or self-hosted on a cloud file sharing platform, such as:

-   [Google Drive](https://www.google.com/drive/)
-   [Dropbox](https://www.dropbox.com/)
-   [OneDrive](https://onedrive.live.com/about/en-gb/)

{: .warning }

> Make sure the `assets` folder and other relevant files within the resource pack archive is in the root of the zip archive and not within a folder.

{% tabs downloadLink %}
{% tab downloadLink Directly From the Website %}

This may be different according to the hosting platform used, however it often involves right clicking and grabbing the download link directly from the "Download" button provided. Do note that some hosting platforms shuffle download links every so often, and so this method may not always work.

{% endtab %}
{% tab downloadLink Google Drive %}

1. Upload the resource pack to your Google Drive account, ensure it is in the `.zip` file format.

2. Select it and click on "Share".

3. Under "General access", set "Restricted" to "Anyone with the link".

4. Once the permission has been updated, click on "Copy link".

5. Examine the copied link carefully and look for a random string of characters between slashes (`/` `/`); this is your file ID and is unique to each file.

6. Copy and paste your file ID at the end of the following URL:

    ```
    https://drive.google.com/uc?export=download&id=
    ```

7. This is a direct download link to your file, it should look like the following:

    ```
    https://drive.google.com/uc?export=download&id=xxxxxxxxxxxxxxxxxxxxx
    ```

{% endtab %}
{% tab downloadLink Dropbox %}

1. Upload the resource pack to your Dropbox account, ensure it is in the `.zip` file format.

2. Select it and click on "Copy link".

3. To obtain a direct download link, add the end of the link replace `dl=0` with `dl=1`.

{% endtab %}
{% endtabs %}

## Configuration

### Adding the Download Link to the Server

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Minecraft" category and navigate to [Server Properties](https://client.falixnodes.net/server/properties).

4. Find and set `resource-pack` to the direct download link we obtained before.

5. To save your changes, click on "**Submit**{: .blue }" at the top of the list.

6. (Re)start your server.

{: .success}

> If you have successfully added the resource pack, you should be prompted with a "Download Resource Pack?" popup the next time you join the server.

### Enforcing the Resource Pack

By default, players will be prompted if they wish to download and install the resource pack, giving them the option to deny. If you wish all your players to use it, you may want to enforce it by follow the steps below:

1. Open and navigate back to the [Server Properties](https://client.falixnodes.net/server/properties) page.

2. Find and set `require-resource-pack` to `Enabled`.

3. To save your changes, click on "**Submit**{: .blue }" at the top of the list.

4. (Re)start your server.

### Verifying the Resource Pack Integrity

Although optional, you may want to verify the resource pack file integrity to make sure the correct file and all its contents are correctly downloaded. This can be done with a SHA1 hash by generating a string of characters from the downloaded resource pack on the server side and comparing it with the value specified. If the downloaded file is not integrally sound, a yellow "Invalid sha1 for resource-pack-sha1" text will be shown in the console when the server is started.

The SHA1 hash can be generated by any SHA1 generator of your preference. In this example we will be using [emn178's sha1checksum](https://emn178.github.io/online-tools/sha1_checksum.html).

1. Go to [emn178's sha1checksum](https://emn178.github.io/online-tools/sha1_checksum.html).

2. Upload your resource pack to website, make sure it is in the `.zip` format.

3. A string of characters will be generated, copy this as it is your SHA1 checksum.

4. Open and navigate back to [Server Properties](https://client.falixnodes.net/server/properties) page.

5. Find and set `resource-pack-sha1` to your SHA1 checksum.

6. To save your changes, click on "**Submit**{: .blue }" at the top of the list.

7. (Re)start your server.

### Adding Multiple Resource Packs

Although this isn't a feature, you may circumvent this by using a plugin, or by combining the resource packs either manually, or using tools such as [Elmakers's merge tool](https://merge.elmakers.com/)

{: .warning }

> It is generally not a good idea to combine resource packs as they may be incompatible with each other or override one another leading to missing or glitchy textures.
