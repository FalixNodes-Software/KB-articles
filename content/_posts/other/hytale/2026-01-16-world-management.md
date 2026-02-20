---
layout: post
title: Managing Your Hytale Server World
category: Hytale
tags: Essentials
permalink: /other/hytale/essentials/world-management
description: Learn how to upload, download, and manage your Hytale server world files, including singleplayer worlds.
keywords:
    - keyword: hytale
      matches: ["world", "upload", "download", "singleplayer"]
author: TWIXhunter
---


## Uploading Your World

To upload a world to your Hytale server, follow these steps. We recommend compressing your world folder to `.zip` format first, as it significantly reduces upload time.

1. Zip the world folder into an archive (like .zip or .tar.gz) or get a singleplayer world like explained [here](#getting-your-singleplayer-world-files)

2. Log in to the [Dashboard](https://client.falixnodes.net/).

3. Choose a server within your server list.

4. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Delete all files from the server (except the 'hytale-downloader' file/folder if present)

6. Click on **Upload File** (or the upload icon in the top-right).

8. Select your world archive and click **Upload**.

9. After the upload completes, locate your world archive in the file list.

8. Click on the 3 dots to the right of the archive file.

9. Click on **Unarchive** to extract the world files.

10. Start your server to load the uploaded world!

{: .note }
> You can also use [SFTP](/falix/dashboard/file-management/sftp) for faster and more reliable file transfers.

## Downloading Your World

To back up or download your Hytale server world:

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to the [Console Page](https://client.falixnodes.net/server/console)  of your server. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

4. Select the "Select All" box at the top of the Filemanager.

5. Click on the **Download** button.

6. Wait for the world to be archived and downloaded.

{: .success}
> Your world archive should now have been downloaded, you can add it as single-player like explained [here](#Adding-Downloaded-Worlds-Back-to-Singleplayer)

{: .note }
> You can also use [SFTP](https://help.falixnodes.net/falix/general/sftp/) to download your world folder directly without archiving!

## Managing Singleplayer Worlds

### Getting Your Singleplayer World Files

If you want to upload your singleplayer Hytale world to your server, you'll first need to locate the world files on your computer.

{% tabs os-locate %}

{% tab os-locate Windows %}

1. Press **Windows Key + R** to open the Run dialog.

2. Type `%APPDATA%\Hytale\UserData\Saves` and press Enter.

3. You'll see folders for each of your singleplayer worlds. Each world is stored in its own folder.

4. Identify the world you want to upload by checking the folder name or opening the world in-game to confirm.

5. Right-click on the world folder and select **Compress to** → **ZIP file** to create a `.zip` archive.

6. Follow the [Uploading Your World](#uploading-your-world) steps above to upload this archive to your server.

{% endtab %}

{% tab os-locate macOS %}

1. Open **Finder**.

2. Press **Command + Shift + G** to open the "Go to Folder" dialog.

3. Type `~/Library/Application Support/Hytale/UserData/Saves` and press Enter.

4. You'll see folders for each of your singleplayer worlds. Each world is stored in its own folder.

5. Identify the world you want to upload by checking the folder name or opening the world in-game to confirm.

6. Right-click on the world folder and select **Compress** to create a `.zip` archive.

7. Follow the [Uploading Your World](#uploading-your-world) steps above to upload this archive to your server.

{% endtab %}

{% tab os-locate Linux %}

1. Open your file manager or terminal.

2. Navigate to `~/.config/hytale/UserData/Saves`

3. You'll see folders for each of your singleplayer worlds. Each world is stored in its own folder.

4. Identify the world you want to upload by checking the folder name or opening the world in-game to confirm.

5. Right-click on the world folder and select **Compress** (or use the command `zip -r worldname.zip worldname/` in terminal).

6. Follow the [Uploading Your World](#uploading-your-world) steps above to upload this archive to your server.

{% endtab %}

{% endtabs %}

### Adding Downloaded Worlds Back to Singleplayer

If you've downloaded a world from your server and want to play it in singleplayer:

{% tabs os-add %}

{% tab os-add Windows %}

1. Download your world archive from the server following the [Downloading Your World](#downloading-your-world) steps.

2. Press **Windows Key + R** to open the Run dialog.

3. Type `%APPDATA%\Hytale\UserData\Saves` and press Enter.

4. Extract the downloaded archive into the Saves folder.

5. Make sure the extracted folder contains all the necessary world files.

6. If the folder name contains special characters, rename it to something more descriptive.

7. Launch Hytale and check your singleplayer world list. Your downloaded world should now appear!

{% endtab %}

{% tab os-add macOS %}

1. Download your world archive from the server following the [Downloading Your World](#downloading-your-world) steps.

2. Open **Finder** and press **Command + Shift + G**.

3. Type `~/Library/Application Support/Hytale/UserData/Saves` and press Enter.

4. Extract the downloaded `.zip` archive into the Saves folder.

5. Make sure the extracted folder contains all the necessary world files.

6. If the folder name contains special characters, rename it to something more descriptive.

7. Launch Hytale and check your singleplayer world list. Your downloaded world should now appear!

{% endtab %}

{% tab os-add Linux %}

1. Download your world archive from the server following the [Downloading Your World](#downloading-your-world) steps.

2. Navigate to `~/.config/hytale/UserData/Saves` using your file manager or terminal.

3. Extract the downloaded `.zip` archive into the Saves folder (you can use `unzip worldname.zip` in terminal).

4. Make sure the extracted folder contains all the necessary world files.

5. If the folder name contains special characters, rename it to something more descriptive.

6. Launch Hytale and check your singleplayer world list. Your downloaded world should now appear!

{% endtab %}

{% endtabs %}

{: .warning }
> Always create backups of your existing singleplayer worlds before adding new ones or making changes!