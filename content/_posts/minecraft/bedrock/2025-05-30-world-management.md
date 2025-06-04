---
title: Upload or Download Your World From Your Minecraft Bedrock Server
tags: General
permalink: /minecraft/bedrock/general/world-management
description: An essential guide to manage, upload and download your world to and from your server.
keywords:
    - keyword: world
      matches: &world_matches ["upload", "download", "management"]
    - keyword: map
      matches: *world_matches
author:
    - TWIXhunter
---
## Uploading your world:

### Getting the world Files:
Your world might come with 2 types of files, the first one would be `.zip` (and other archives, such as `.gz`) and `.mcworld`. You may also upload a single player world.
Follow the instructions below on how to get the required server files.

{: .warning }
> This article was written for the "Minecraft for Windows" version of the game, installation for other versions (such as Pocket and Xbox editions) may differ slightly depending on your platform.

{% tabs filetypes %}


{% tab filetypes  Archive files %}

1. Select the .zip file on your computer and extract it

{: .warning }
> Make sure that the extracted folder does not have an extra folder inside, if it does then move it outside the main folder. 

{% endtab %}


{% tab filetypes .mcworld %}

1. Double-click the file to open it in Minecraft and add it to the game files.

2. Wait for Minecraft to open and import the file.

3. Go to your installation folder. You can easily open it by pressing `Win` + `R` and paste `%localAppdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\minecraftWorlds`.

4. Find the right folder. you can identify your world by opening the `levelname.txt`file inside the folder.

5. Copy the world folder to an easy location where you will find it back later.

{% endtab %}



{% tab filetypes existing singleplayer world %}

1. Go to your installation folder. You can easily open it by pressing `Win` + `R` and paste `%localAppdata%\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\minecraftWorlds`.

2. Find the right folder. you can identify your world by opening the `levelname.txt`file inside the folder.

3. Copy the world folder to an easy location where you will find it back later.

{% endtab %}


{% endtabs %}


### Uploading the world to the server:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Make sure your server is turned off, if not click on the "**Stop**{: .red }" button to the top right of the console.

4. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Open the `worlds` folder and delete the existing `bedrock_level` folder.

6. Upload the world folder by hovering over "upload" and selecting "upload folder".

7. Rename the folder you uploaded to `bedrock_level` by clicking on the 3 dots on the end and selecting "rename".

8. (Re)start the server.

## Downloading your world:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Within your server list, choose a server.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Make sure your server is turned off, if not click on the "**Stop**{: .red }" button to the top right of the console.

4. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Open the `worlds` folder.

6. Download the folder called `bedrock_level`.
