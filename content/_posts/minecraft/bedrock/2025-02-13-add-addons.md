---
title: How To add addons to your Minecraft Bedrock Server
tags: General
permalink: minecraft/bedrock/general/add-addons
description: How to add addons to your minecraft bedrock server.
keywords:
    - keyword: addons
      matches: ["bedrock", "bedrockedition", "mobile"]
author: TWIXhunter
---

Minecraft Bedrock Addons are integrated modifications or additions to the game that enhance or change the gameplay experience and can be downloaded from the in-game marketplace or other online sources. Addons can range from simple tweaks to game mechanics to more complex additions such as new mobs, items, behaviors, and custom features, all designed to work seamlessly within the Bedrock Edition framework.

## Getting the Server Files
There are 3 main types of files that can contain addons, these are
 - .mcpack
 - .mcadddon
 - .zip (or other archives)
Follow the steps below to convert them into the required server files.


### .mcpack and .mcaddon

1. double-click the file to open it in Minecraft and add it to the game files.

2. Wait for Minecraft to open and import the file.

3. Go to your installation folder, for Windows this is `C:\Users\(your_pc_username)\AppData\Local\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\`

> You can easily open this folder by pressing `WIN` + `R` and paste `%localAppdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\`.

4. Open the `behavior_packs`, inside you will find a list of all imported packs

5. Find the folder with the name of the pack you want and copy it to your desktop.

6. Repeat steps 4 and 5 for the resource_packs folder.
> Make sure you add `_BP` and `_RP` to the end of the name if both folders have the same name.


### .zip (and other archives)

1. download the file to your computer

2. Unarchive it by selecting it in your file explorer and pressing `extract all`.

3. Inside you will find 2 folders representing `resource_packs` and `behavior_packs`.


## Adding the addon to your server

### Adding the resource pack

1. Login to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server . In the top navigation bar, hover over "Manage", then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [resource_packs](https://client.falixnodes.net/server/filemanager?dir=/resource_packs/) folder.

5. Upload your resource pack to this folder by dragging it to the top of the File Manager or by using the Upload Folder button.

6. Return to the File Manager home folder.

7. Go to 'Worlds' and open the 'Bedrock Level' folder.

8. Create a new file called `world_resource_packs.json` if it doesn't already exist.

9. Back in your addons resource pack folder on your device, open the `manifest.json` file.

10. Copy the contests from the `manifest.json` file to the `world_resource_packs.json` file in the file manager.

### Adding the Behavior Pack

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the top navigation bar, hover over "Manage", then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [behavior_packs](https://client.falixnodes.net/server/filemanager?dir=/behavior_packs/) folder.

5. Upload your behavior pack to this folder by dragging it to the top of the File Manager or using the Upload Folder button.

6. Return to the File Manager's home folder.

7. Go to 'Worlds' and open the 'Bedrock Level' folder.

8. Create a new file called `world_behavior_packs.json' if it doesn't already exist.

9. Back in your addons behavior pack folder on your device, open the `manifest.json` file.

10. Copy the competitions from the manifest.json file into the world_behavior_packs.json file in the file manager.