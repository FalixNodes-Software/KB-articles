---
title: Upload or Download Your World From Your Minecraft Bedrock Server
tags: Customization
permalink: /minecraft/bedrock/customization/world-management
description: An essential guide to manage, upload and download your world to and from your server.
keywords:
    - keyword: world
      matches: &world_matches ["upload", "download", "management"]
    - keyword: map
      matches: *world_matches
author:
    - TWIXhunter
    - Deka
---
## Uploading Your World

### Getting The World Files

{% tabs filetypes %}

{% tab filetypes Archive files %}

Extract the archive to a folder on your device.

{: .warning }
> Make sure that the extracted folder does not have an extra folder inside. If it does, move it outside the main folder. 

{% endtab %}

{% tab filetypes .mcworld file %}

{: .warning }
> These instructions presume you are using the "Minecraft for Windows" version of the game, install locations for other editions (such as Pocket and Xbox) may differ depending on your platform.

1. Double-click the file to open it in Minecraft.

2. Wait for Minecraft to open and import the world.

3. Go to the `minecraftworlds` folder in your Minecraft install location. You can open it for the "Minecraft for Windows" version of the game by pressing `Win` + `R` and pasting `%localAppdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\minecraftWorlds`.

4. Find the world you want to use. You can identify your world by opening the `levelname.txt` file inside the folder.

5. Copy the world folder to another location for further use.

{% endtab %}

{% tab filetypes Existing singleplayer world %}

{: .warning }
> These instructions presume you are using the "Minecraft for Windows" version of the game, install locations for other editions (such as Pocket and Xbox) may differ depending on your platform.

1. Go to the `minecraftworlds` folder in your Minecraft install location. You can open it for the "Minecraft for Windows" version of the game by pressing `Win` + `R` and pasting `%localAppdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\minecraftWorlds`.

2. Find the world you want to use. You can identify your world by opening the `levelname.txt` file inside the folder.

3. Copy the world folder to another location for further use.

{% endtab %}

{% endtabs %}

### Uploading The World To The Server

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Make sure your server is stopped. If not, stop your server by pressing the "**Stop**{: .red }" button.

4. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Open the `worlds` folder and delete the existing `bedrock_level` folder.

6. Upload the world folder by hovering over "Upload" and selecting "Upload Folder".

7. Rename the folder you uploaded to `bedrock_level` by pressing the 3 dots and selecting "Rename".

8. Start the server.

## Downloading Your World

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Make sure your server is stopped. If not, stop your server by pressing the "**Stop**{: .red }" button.

4. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Open the `worlds` folder.

6. Download the `bedrock_level` folder.