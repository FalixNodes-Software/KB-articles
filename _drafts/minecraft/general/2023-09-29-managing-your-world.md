---
layout: help/article
title:  "Managing Your Minecraft Server World"
categories: Minecraft
icon: <i class='fa-light fa-memo'></i></span>
tags: mcgeneral
permalink: /help/minecraft/general/managing-your-world.*
gitURL: _posts/minecraft/general/2023-09-29-managing-your-world.md
description: "Create, manage and delete your Minecraft server world in Falix"

author: Mocab
authorGitHub: mocab
---

 <div class="minecraft-edition-picker-placeholder">
    <i class="fa-duotone fa-slider"></i>
    <h2>Please select an edition</h2>
    <p>There are two versions of this article. One for Minecraft's Java edition and another for Minecraft's Bedrock edition.</p>
</div>
<style>.minecraft-edition-picker {display: contents !important;}</style>

<div style="display: none" id="java" markdown=1>

## Managing Your World

## Uploading Your World (1)

In the method below you will be asked to compress/archive your world folder in the `.zip` format before uploading it to your server. Although you may still upload the folder directly, we recommend archiving it first as it requires a shorter time to upload.

{: .note }
> Make sure your server is offline while following the steps below.

1. Log in to the [Dashboard](https://client.falixnodes.net/).
2. Scroll down and locate your server, then click on "Play".
3. On the top navbar, hover over "Server Management", then navigate to "File Manager".
4. Scroll down, then click on "Upload File".
5. Click on "Choose Files".
6. Make sure you have already archived your world folder in the `.zip` format. Select it, and click on "Upload".
7. After it is done uploading, locate your world archive and click on the 3 dots to its right.
8. Click on "Unarchive".
9. Your world folder should appear, make sure that it is named `world` (case sensitive).
10. Your world should be uploaded!

{: .note }
> You can also use [SFTP](https://help.falixnodes.net/falix/general/sftp/)!

## Downloading Your World (1)

1. Log in to the [Dashboard](https://client.falixnodes.net/).
2. Scroll down and locate your server, then click on "Play".
3. On the top navbar, hover over "Server Management", then navigate to "File Manager".
4. Locate your world folder, it is usually called `world`.
5. Select the folder by click on the checkbox to its left.
6. Set the "Mass Action" to "Archive", then click on "Run".
7. A new archive should be created, locate it and click on the 3 dots to its right.
8. Click on "Download".
9. Your world folder should be downloaded!

{: .note }
>
> - Some server software such as Spigot, Paper and Purpur, separate the world folder into 3 different folders called `world`, `world_nether` and `world_the_end`, you will also need to download these.
> - You can also use [SFTP](https://help.falixnodes.net/falix/general/sftp/)!

</div>

<div style="display: none" id="bedrock" markdown=1>

## Uploading Your World (2)

This guide explains how to upload a world to your server!

{: .note }
> Make sure your server is turned off while following the steps below.

1. Open any type of file explorer application on your device.
2. Navigate to your Minecraft Client world folder.<br>

PC (Windows 10 Edition):

```java
- \Users\USERNAME\AppData\Local\Packages\Microsoft.MinecraftUWP_8wekyb3d8bbwe\LocalState\games\com.mojang\minecraftWorlds
```

{: .note }
> "USERNAME" is your own Windows username. <br>

Android:

```java
Internal storage/Android/com.mojang.minecraftpe/files/games/com.mojang/minecraftWorlds
```

IOS:

```java
Apps/com.mojang.minecraftpe/Documents/games/com.mojang/minecraftWorlds
```

1. There will be a folder (or multiple folders, one for each world if you have Windows 10 Edition or Pocket Edition) with a random name like "BQUAAIFxEAA=", find the world file you want to put on your dedicated server by checking `levelname.txt`.
2. Archive your world folder.
3. Go to the [Game Panel](https://panel.falixnodes.net) and click on your server.
4. Click on "File Manager" at the top of the page.
5. Navigate to the `worlds` folder and open it.
6. Click on "Upload", it is a big blue button located at the top right of the page.
7. Select your world archive.
8. After it is done uploading, locate your world archive and click on the 3 dots to its right.
9. Click on "Unarchive".
10. Remove the `=` symbol from the world folder name by clicking the "Rename" button from the 3 dots.
11. Open the `server.properties` file on your server. Find the `level-name=` line and enter the name of the folder you uploaded in step 8, (spaces are allowed) so that it looks something like `level-name=My Server Level`. This must match the folder name.
12. Start your server. It should now be running your imported world.

{: .note }
> If you have a compressed/archived world (ending in ".zip", ".rar" or others), then follow steps from step 5.

## Downloading Your World (2)

This guide explains how to download a world from your server!

1. Go to the [Game Panel](https://panel.falixnodes.net).
2. Click on your server.
3. Click on "File Manager" at the top of the page.
4. Navigate to the `worlds` folder, open it.
   ![image](/assets/images/posts/minecraft/managing-your-world/step-3-4-bedrock.png)
5. Click on the 3 dots to the right of your world folder.
6. Click on "Archive".
   ![image](/assets/images/posts/minecraft/managing-your-world/step-5-6-bedrock.png)
7. A new file should be created, locate it and click on the 3 dots to its right.
8. Click on "Download".
   ![image](/assets/images/posts/minecraft/managing-your-world/step-5-6-bedrock.png)
9. Your world folder should be downloaded!

{: .note }
> You can also use [SFTP](https://help.falixnodes.net/falix/general/sftp/)!

</div>
