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

# how to upload a world to the server.

## How to upload your world using the worlds page

//work in progress

## How to upload your world using the File Manenger.

{: .warn}
> paper servers use a diffrent storage method for worlds then vanilla, forge or fabric, if you are using a paper server then you need to upload the folders called: "world", "world_nether" and "world_the_end" seperatly.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and click on the server you want the world uploaded to.

3. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage" and pressing "File Mananger.

4. Locate and select the existing world folder named "world" (and world_nether and world_the_end for paper servers)

5. Delete these folders to remove the current generated world (Make sure to create a backup of any important data you wish to keep).

6. Compress your custom world folder into a zip file.

{: .warn}
> If the world you are uploading is a non-paper world and you are uploading it to a paper server then follow [this guide](https://docs.papermc.io/paper/migration#from-vanilla) to turn the world into a paper compatible world

{: .warn}
> If the world you are uploading is a paper world and you are uploading it to a non-paper server then follow [this guide](https://docs.papermc.io/paper/migration#to-vanilla) to turn the world into a vanilla compatible world

7. Click the "Upload Files" button in the file manager.

8. Select the zip file containing the custom world from your local machine.

9. Once the upload is complete, click the three dots next to the uploaded zip file and click "Unarchive" to extract the contents.

10. Make sure to rename the extracted world folder to "world", ("world", "world_nether", and "world_the_end" for paper servers). (If they are already named correctly then you can skip this step).

11. Restart your server for the changes to take effect.

The server will now use your uploaded world as the new game world, replacing the previously generated one. Make sure your custom world files are correctly formatted and compatible with your server's version and type to ensure proper functioning.



# How to download a world from the server.

## How to download your world using the worlds page

//work in progress

## How to download the world from the server using the File Manenger.

{: .warn}
> paper servers use a diffrent storage method for worlds then vanilla, forge or fabric, if you are using a paper server then you need to download the folders called: "world", "world_nether" and "world_the_end" seperatly.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and click on the server you want the world uploaded to.

3. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage" and pressing "File Mananger.

4. Locate the existing world folder named: "world" (for paper servers: "world" "world_nether", and "world_the_end").

5. select these folders and press "archive" in the mass-actions pop-up.

6. download the archive to your computer by hovering over the 3 dot's and pressing "download"

7. extract the downloaded file

{: .warning}
> You might need to install archiving software (like WinRAR or 7zip) to unarchive the .tar.gz file

{: .info}
> If you have a paper server (and you downloaded the 3 world files) then you might want to follow [this guide](https://docs.papermc.io/paper/migration#to-vanilla) if you are using the world as a singleplayer-world or if you are migrating to a non-paper server.