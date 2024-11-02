---
layout: post
title: Using Custom Server Software or Version
category: Bedrock
tags: General
description: Find out how to use a custom or modified software or version not available in the versions list.
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

-   [Official Bedrock Dedicated Server (BDS)](https://www.minecraft.net/en-us/download/server/bedrock)
-   [PocketMine-MP (PMMP)](https://github.com/pmmp/PocketMine-MP/releases)
-   [NukkitX](https://ci.opencollab.dev/job/NukkitX/job/Nukkit/job/master)

## Installing the Latest BDS

1. Download the Dedicated Server Software for Ubuntu (Linux) from the [Minecraft Bedrock website](https://www.minecraft.net/en-us/download/server/bedrock).

2. If you wish to install a preview version, download Dedicated Server Software for Ubuntu (Linux) Preview instead.

3. Login to the [Dashboard](https://client.falixnodes.net/).

4. Choose a server from your server list.

5. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console). Ensure your server is offline by pressing the "**Stop**{: .red }" button at the top of the console.

6. In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

### Downloading an Older Version of BDS

1. Replace `x` with the version you are looking for: `minecraft.azureedge.net/bin-linux/bedrock-server-x.zip`

    - For example, if you are downloading the server files for `1.20.81.01`, the link would be this: `minecraft.azureedge.net/bin-linux/bedrock-server-1.20.81.01.zip`

2. Open the link. The download should be a `.zip` archive with the server files.

### Making a Server From Scratch

1. Select all files using the tickbox on top left of the file manager ribbon.

2. Delete all files, if you have any, using the Mass Actions dialog box which appears after you select all the files.

3. Press the "**Upload Files**{: .blue }" button and select the `.zip` archive with the BDS files.

4. Locate the file, press the three dots and select Unarchive.

5. After unarchiving, navigate back to the [Console](https://client.falixnodes.net/server/console) and start your server.

### Updating your BDS Server

{: .warning }

> Make sure to make a backup of your server to prevent any data loss.

1. Get an archive with a newer version of BDS. Only need the `bedrock_server` file is necessary for updating, so you can unarchive it on your device. Refer to ["Installing the Latest BDS"](#installing-the-latest-bds).

2. Select the `bedrock_server` file in your server's File Manager.

3. Press the "**Delete**{: .red }" button to delete your old server executable.

4. Press the "**Upload Files**{: .blue }" button and select the `bedrock_server` file.

5. Navigate back to the [Console](https://client.falixnodes.net/server/console) and start your server.

## Installing a PMMP Server

{: .warning }

> Manual installation for PMMP is broken as of now, but the installing from the Versions page is still available.

1. Login to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server from your server list.

3. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console). Ensure your server is offline by click on the "**Stop**{: .red }" button at the top of the console.

4. In the top navigation bar, hover over "Server" then navigate to the [Versions page](https://client.falixnodes.net/server/versions).

5. Locate PocketMine - Bedrock in the Minecraft: Bedrock/Mobile Edition category and select the version you want to install.

6. Press the "**Install**{: .green }" button and wait for the installation process to finish.

7. Navigate back to the [Console](https://client.falixnodes.net/server/console) and start your server.

## Installing a NukkitX Server

1. Download the required `.jar` file from the links provided above.

2. Login to the [Dashboard](https://client.falixnodes.net/).

3. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console). Ensure your server is offline by click on the "**Stop**{: .red }" button at the top of the console.

4. In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

5. Select your old server jar and press the "**Delete**{: .red }" button. This step is necessary only if you have a `.jar` file already in your files as this may cause the installation to break. You can ignore this step if you don't have any files.

6. Press the "**Upload Files**{: .blue }" button and select your downloaded `.jar` file.

7. Ensure the uploaded file is named `server.jar`. If it is not, press the 3 dots to its right and select "Rename".

8. Navigate to the [Settings](https://client.falixnodes.net/server/settings) and locate Environment.

9. Ensure it is set to the latest available Java version.

10. Navigate back to the [Console](https://client.falixnodes.net/server/console) and start your server.

11. Language codes will appear in the console. Select your preferred language by typing it's code. For example, if you want to select English, type `eng`.
