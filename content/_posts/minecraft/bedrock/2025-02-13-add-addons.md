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

{: .warning }
> this article was written for the "minecraft for windows" version of the game, installation from other versions (like Pocket and Xbox edition) might slightly differ depending on your platform.

### .mcpack
these files only contain resource packs, for a more detailed guide on how to add them to your server see our [How To Add Resource Packs To Your Minecraft Bedrock Server](https://kb.falixnodes.net/minecraft/bedrock/configuration/resource-pack) article.

### .mcaddon

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

1. Login to the [Dashboard](https://client.falixnodes.net/).

2. Select a server from your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server . In the top navigation bar, hover over "Manage", then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [resource_packs](https://client.falixnodes.net/server/filemanager?dir=/resource_packs/) folder.

5. Upload your resource pack to this folder by dragging it to the top of the File Manager or by using the Upload Folder button.

6. Return to the File Manager home folder.

7. Go to 'Worlds' and open the 'Bedrock Level' folder.

8. Create a new file called `world_resource_packs.json` if it doesn't already exist.

9. Paste the following info into the file:
```json
[
  {
    "pack_id" : "UUID HERE",
    "version" : [version, number, here]
  }
]
```
    > To add multiple resource packs, simply add a comma (`,`) after the closing curly brackets (`}`) and paste in all the content between and including the curly brackets (`{` `}`).
10. Back in your addons resource pack folder on your device, open the `manifest.json` file.

11. Copy the UUID and version from the header section and paste them into your server's `world_resource_packs.json` file under pack_id and version.

12. Save the file and get back to the Home folder of the filemanager.

13. Locate and open the [behavior_packs](https://client.falixnodes.net/server/filemanager?dir=/behavior_packs/) folder.

14. Upload your behavior pack to this folder by dragging it to the top of the File Manager or using the Upload Folder button.

15. Return to the File Manager's home folder.

16. Go to 'Worlds' and open the 'Bedrock Level' folder.

17. Create a new file called `world_behavior_packs.json` if it doesn't already exist.

18. Paste the following info into the file:
```json
[
  {
    "pack_id" : "UUID HERE",
    "version" : [version, number, here]
  }
]
```
    > To add multiple behavior packs, simply add a comma (`,`) after the closing curly brackets (`}`) and paste in all the content between and including the curly brackets (`{` `}`).

19. Back in your addons behaviore pack folder on your device, open the `manifest.json` file.

20. Copy the UUID and version from the header section and paste them into your server's `world_behavior_packs.json` file under pack_id and version.