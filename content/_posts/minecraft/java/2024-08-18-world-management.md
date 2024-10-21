---
layout: post
title: Learn how to upload and download your world
category: Dashboard
tags: Server
permalink: /minecraft/java/general/world-management
description: Learn how to upload and download your world.
author: TheTWIXhunter
toc: true
---

# Uploading a world to your server

## Using the Worlds page

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Navigate to the server you want to upload your world to.

3. Navigate to the [Worlds page](https://client.falixnodes.net/server/worlds) by hovering over "Server" and pressing "Worlds".

4. Press the "Upload World" button and upload your world folder.

{: .info}
> If your world is archived, you need to unarchive it before uploading.

5. Press "Make Primary" to make your world the default one.

6. If you had previous worlds, you may delete them.


## Using the File Manager

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Navigate to the server you want to upload your world to.

3. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage" and pressing "File Manager".

4. Locate the `world`, `world_nether`, and `world_the_end` folders.

{: .info}
> Some server software may use only one folder for all dimensions (`world`).

5. If you want to replace the world, delete these folders to remove the current ones (make sure to create a backup of any data you want to keep).

6. Archive the world folder you want to upload.

7. Press the "Upload Files" button.

8. Select the archive containing your world.

9. Once the upload is complete, press the three dots next to the uploaded archive file and select "Unarchive" to extract the contents.

{: .info}
> Make sure the world folders are named as `world`, `world_nether` and `world_the_end`.

{: .success}
> The server will now use your world, replacing the previously generated one. Make sure your custom world files are correctly named and were not created on a newer than your server's version.


# Downloading a world from the server

## Using the File Manager

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Navigate to the server you want to upload your world to.

3. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage" and pressing "File Manager".

4. Locate the `world`, `world_nether`, and `world_the_end` folders.

5. Select the folders and press the "Download" button in the Mass Actions menu.

{: .success}
> The archive containing your world should begin downloading to your device.
