---
layout: post
title: Using Custom Server Software or Version
category: Bedrock
tags: General
description: Guide on how to install a Bedrock Server or use a custom software or version not available in the versions list.
keywords:
    - keyword: custom
      matches: ["software", "core", "bedrock", "server"]
    - keyword: bedrock
      matches: ["server"]
    - keyword: pocketmine
    - keyword: nukkit
permalink: /minecraft/java/general/custom-software
author: Dynamic_Slayer
---

Before proceeding with this guide, we recommend reading our [server software guide](/minecraft/java/general/server-software) to better understand the terms used below.

For Minecraft Bedrock Edition servers, several popular server software options offer unique features, plugin support, and cross-play capabilities.

## :cook: Preparing the Server Software:

Bedrock softwares are standalone and can be often downloaded directly. Here’s a rundown of the most commonly used Bedrock server software and their download websites:

{: .warning }

> **NEVER** download shady or untrusted server software, or software from unofficial websites. Malicious developers can use them to easily gain backdoor access to your server and reck havoc.

-   [Official Bedrock Dedicated Server](https://www.minecraft.net/en-us/download/server/bedrock)
-   [PocketMine-MP](https://github.com/pmmp/PocketMine-MP/releases)
-   [NukkitX](https://ci.opencollab.dev/job/NukkitX/job/Nukkit/job/master/)

### Downloading an Older Official Version of Bedrock

1. Copy this link exactly: https://minecraft.azureedge.net/bin-linux/bedrock-server-version.zip

2. Paste it inside your browser and then replace the version with the version you are looking for.

    - For example, if you are downloading the server files for 1.20.81.01, you will enter the link like this: https://minecraft.azureedge.net/bin-linux/bedrock-server-1.21.81.01.zip

3. Download will start automatically and you will get your desired files on your device.

## Installing Official Bedrock Server

1. Download Minecraft Dedicated Server Software for Ubuntu (Linux) from the official Minecraft bedrock website. A `.zip` file will be downloaded.

2. If you wish to install a preview version, download Minecraft Dedicated Server Software for Ubuntu (Linux) Preview instead of the one above.

3. Login to the [Dashboard](https://client.falixnodes.net/).

4. Choose a server from your server list.

5. You will be redirected to your server's [Console Page](https://client.falixnodes.net/server/console). Ensure your server is offline by click on the "**Stop**{: .red }" button at the top of the console.

6. In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

### Creating a Server From Scratch

1. Select all the files using the tickbox on top left of the file manager ribbon.

2. Delete all the files, if you have any, using the Mass Actions dialog box which appears after you select all the files.

3. Click on `"**Upload Files**{: .blue }"` button and select the downloaded `.zip` file.

4. Locate the file and click on the three dots to its right and click on Unarchive.

5. Navigate back to the [Console Page](https://client.falixnodes.net/server/console) and start your server.

### Updating the Previous Server

1. On your device, extract the `.zip` file which you downloaded.

2. Locate the `bedrock_server` file in your server's File Manager and click on the 3 dots to its right.

3. Click on "**Delete**{: .red }" to delete your old server software.

4. Click on `"**Upload Files**{: .blue }"` button. Navigate to the folder where you extracted the downloaded `.zip` file.

5. Locate the `bedrock_server` file and upload it.

6. Navigate back to the [Console Page](https://client.falixnodes.net/server/console) and start your server.

## Installing PocketMineMP Bedrock Server

{: .warning }

> Manual installation for PocketMine MP is broken as of now, but the installation from versions page has the important softwares you need.

1. Login to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server from your server list.

3. You will be redirected to your server's [Console Page](https://client.falixnodes.net/server/console). Ensure your server is offline by click on the "**Stop**{: .red }" button at the top of the console.

4. In the top navigation bar, hover over "Server" then navigate to the [Versions Page](https://client.falixnodes.net/server/versions).

5. Locate PocketMine - Bedrock inside the Minecraft: Bedrock/Mobile Edition category and select the version you want to install.

6. Click on install and wait a few seconds till you get a confirmation.

7. Navigate back to the [Console Page](https://client.falixnodes.net/server/console) and start your server.

## Installing NukkitX Bedrock Server

1. Download the required `.jar` file from the links provided above.

2. Login to the [Dashboard](https://client.falixnodes.net/).

3. You will be redirected to your server's [Console Page](https://client.falixnodes.net/server/console). Ensure your server is offline by click on the "**Stop**{: .red }" button at the top of the console.

4. In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

5. Click on "**Delete**{: .red }" to delete your old server jar. This step is necessary only if you have a `.jar` file already in your files as this may cause the installation to break. You can ignore this step if you don't have any files.

6. Click on the "**Upload Files**{: .blue }" button and select the downloaded `.jar` file.

7. Ensure the uploaded file is named `server.jar`. If it is not, click on the 3 dots to its right and click on "Rename".

8. Head to [Settings](https://client.falixnodes.net/server/settings) and navigate to Environment.

9. Ensure it is set to the latest Java version.

10. Navigate back to the [Console Page](https://client.falixnodes.net/server/console) and start your server.

11. Language codes will appear in the console. Select the language you want by typing its code. For example, if you want english, type `eng` and press enter.

12. Your server is now ready to play in.