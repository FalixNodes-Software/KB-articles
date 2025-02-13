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

Minecraft Bedrock addons are build-in modifications or additions to the game that enhance or change the gameplay experience, downloadable from the in-game marketplace or from other online sources. Addons can range from simple adjustments to game mechanics to more complex additions, such as new mobs, items, behaviors, and custom features, all designed to work seamlessly within the Bedrock Edition framework.

## getting the Server files
There are 3 main types of files that can contain addons, these are:
 - .mcpack
 - .mcadddon
 - .zip (or other archives)
Follow the steps below of converting them into the needed server files.


### .mcpack and .mcaddon

1. double-click the file to open it in Minecraft and add it to the game's files.

2. Wait for minecraft to open and import the file

3. Go to your instalation folder, for windows this is: `C:\Users\(your_pc_username)\AppData\Local\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\`

> You can easly open this folder by pressing `WIN` + `R` and pasting `%localAppdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\`

4. Open the `behavior_packs`, inside you will find a list of all imported packs

5. Find the folder with the name of the pack you want and copy-paste it to your desktop

6. Repeat step 4 and 5 for the `resource_packs` folder
> make sure to add `_BP` and `_RP` to the end of their name if both folders have the same name.


### .zip (and other archives)

1. download the file to your computer

2. Unarchive it by selecting it in your file explorer and pressing `extract all`

3. Inside you will find 2 folders representing `resource_packs` and `behavior_packs`,


## Adding the Addon to your server

### adding the resource pack

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [resource_packs](https://client.falixnodes.net/server/filemanager?dir=/resource_packs/) folder.

5. Upload your resource pack to that folder by dragging it on top of the file manager or using the "upload folder" button.

6. Get back to the Home folder of the file manager.

7. Go to the `worlds` and open the `Bedrock level` folder

8. Create a new file called `world_resource_packs.json` if it doesn't already exist.

9. Back in your addons resource pack folder on your device, open the `manifest.json` file

10. Copy the contests of the `manifest.json` file to the `world_resource_packs.json` file in the File Manager.

### adding the behaviour pack

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [behavior_packs](https://client.falixnodes.net/server/filemanager?dir=/behavior_packs/) folder.

5. Upload your behavior pack to that folder by dragging it on top of the file manager or using the "upload folder" button.

6. Get back to the Home folder of the file manager.

7. Go to the `worlds` and open the `Bedrock level` folder

8. Create a new file called `world_behavior_packs.json` if it doesn't already exist.

9. Back in your addons behavior pack folder on your device, open the `manifest.json` file

10. Copy the contests of the `manifest.json` file to the `world_behavior_packs.json` file in the File Manager.