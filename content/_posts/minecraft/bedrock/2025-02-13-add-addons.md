---
title: How To Add Addons To Your Minecraft Bedrock Server

tags: General
permalink: minecraft/bedrock/general/add-addons
description: Learn how to add addons to your Bedrock server

keywords:
    - keyword: addons
      matches: ["bedrock", "bedrockedition", "mobile"]
author: TWIXhunter
---

Minecraft Bedrock addons are integrated modifications or additions to the game that enhance or change the gameplay experience and can be downloaded from the in-game marketplace or other online sources. Addons can range from simple tweaks to game mechanics to more complex additions such as new mobs, items, behaviors, and custom features, all designed to work seamlessly within the Bedrock Edition framework. If you wish, you can also make an addon by yourself!




## Getting the Server Files
There are 3 main types of files that can contain addons, these are:

 - `.mcpack`

 - `.mcadddon`

 - `.zip` (or other archives)

Follow the steps below to convert them into the required server files.

{: .warning }
> This article was written for the "Minecraft for Windows" version of the game, installation for other versions (such as Pocket and Xbox editions) may differ slightly depending on your platform.

### .mcpack
These files only contain resource packs. For a more detailed guide on how to add them to your server, see [this](https://kb.falixnodes.net/minecraft/bedrock/configuration/resource-pack) article.


### .mcaddon

1. Double-click the file to open it in Minecraft and add it to the game files.


2. Wait for Minecraft to open and import the file.

3. Go to your installation folder. For Windows this is `C:\Users\(your_pc_username)\AppData\Local\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\`.


> You can easily open this folder by pressing `WIN` + `R` and paste `%localAppdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\`.

4. Open the `behavior_packs`, inside you will find a list of all imported packs.

5. Find the folder with the name of the pack you want and copy it to your desktop.

6. Repeat steps 4 and 5 for the resource_packs folder.
> Make sure you add `_BP` and `_RP` to the end of the name if both folders have the same name.


### .zip (and other archives)

1. download the file to your computer

2. Unarchive it by selecting it in your file explorer and pressing `extract all'.

3. Inside you will find 2 folders representing `resource_packs` and `behavior_packs`.


## Adding the addon to your server

1. Login to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server from your server list.
> Be sure to start the server at least once to generate all the necessary files before continuing.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console) of your server. In the top navigation bar, hover over "Manage", then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Locate and open the [resource_packs](https://client.falixnodes.net/server/filemanager?dir=/resource_packs/) folder.

5. Upload your resource pack to this folder by dragging it to the top of the File Manager or by using the Upload Folder button.

6. Return to the File Manager home folder.

7. Open the "Worlds" folder and open the folder called "Bedrock Level".

8. Create a new file called `world_resource_packs.json` if it doesn't already exist.

{% tabs RSmanifest %}
{% tab RSmanifest Single Addon %}

9. Add the following information to the file, keep the file open so we can fill in the details later:
```json
[
  {
    "pack_id" : "UUID HERE",
    "version" : [version, number, here]
  }
]
```

{% endtab %}
{% tab RSmanifest Multiple addons %}


9. Add the following information to the file, keep the file open so we can fill in the details later:
```json
[
  {
    "pack_id" : "FIRST UUID HERE",
    "version" : [version, number, here]
  },
  {
    "pack_id" : "MIDDLE UUID HERE",
    "version" : [version, number, here]
  },
  {
    "pack_id" : "LAST UUID HERE",
    "version" : [version, number, here]
  }
]
```
> Make sure to ad a `,` after each `}` **except** for the last one.
> Repeat the second section after eachother to add more then 3 packs, delete it for 2 packs

{% endtab %}


10. Back on your device, open the folder you uploaded and open the `manifest.json` file.

11. Copy the UUID and version from the header and paste them into the `world_resource_packs.json` file on your server under `pack_id:` and `version:` like explained in the following examples:


![screenshot of manifest.json](content/assets/images/posts/add-adons/behavior-resource_packs_manifest.png)
![screenshot of world_resource_packs.json](content/assets/images/posts/add-adons/world_behavior-resource_packs.png)

12. Save the file and return to the home folder of the File Manager.


13. Locate and open the [behavior_packs](https://client.falixnodes.net/server/filemanager?dir=/behavior_packs/) folder.


14. Upload your behavior pack to this folder by dragging it to the top of the File Manager or using the Upload Folder button.

15. Return to the File Manager home folder.

16. Go to the 'Worlds' folder and open the folder called 'Bedrock Level'.

17. Create a new file called `world_behavior_packs.json` if it doesn't already exist.

{% tabs BHmanifest %}
{% tab BHmanifest Single Addon %}

18. Add the following information to the file, keep the file open so we can fill in the details later:
```json
[
  {
    "pack_id" : "UUID HERE",
    "version" : [version, number, here]
  }
]
```

{% endtab %}
{% tab BHmanifest Multiple addons %}
18. Add the following information to the file, keep the file open so we can fill in the details later:
```json
[
  {
    "pack_id" : "FIRST UUID HERE",
    "version" : [version, number, here]
  },
  {
    "pack_id" : "MIDDLE UUID HERE",
    "version" : [version, number, here]
  },
  {
    "pack_id" : "LAST UUID HERE",
    "version" : [version, number, here]
  }
]
```
> Make sure to ad a `,` after each `}` **except** for the last one.
> Repeat the second section after eachother to add more then 3 packs, delete it for 2 packs
{% endtab %}

19. Back on your device, open the folder you uploaded and open the `manifest.json` file.

20. Copy the UUID and version from the header section and paste them into your server's `world_behavior_packs.json` file under `pack_id:` and `version:` like explained in the following examples:


![screenshot of manifest.json](content/assets/images/posts/add-adons/behavior-resource_packs_manifest.png)
![screenshot of world_behavior_packs.json](content/assets/images/posts/add-adons/world_behavior-resource_packs.png)

21. Save the file and navigate back to your servers console.

22. (Re)start your server.