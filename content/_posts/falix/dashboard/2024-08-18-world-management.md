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

## How to upload the world to the server using the File Manenger.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and click on the server you want the world uploaded to.

3. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage" and pressing "File Mananger.

4. Locate the existing world folders named "world", "world_nether", and "world_the_end".

5. Select and delete these folders to remove the current generated world (Make sure to create a backup of any important data you wish to keep).

6. Compress your custom world folders into a zip file.

7. Click the "Upload Files" button in the file manager.

8. Select the zip file containing your custom world from your local machine.

9. Once the upload is complete, click the three dots next to the uploaded zip file and click "Unarchive" to extract the contents.

10. Make sure to rename the extracted world folders to world, world_nether, and world_the_end. (If they are named correctly, you can skip this step).

11. Restart your server for the changes to take effect.

The server will now use your uploaded world as the new game world, replacing the previously generated one. Make sure your custom world files are correctly formatted and compatible with your server's version and type to ensure proper functioning.

## How to upload the world to the server using SFTP.

{: .info}

> Access via SFTP is only available to Premium users.

{: .info}

> You will need an SFTP client, such as [FileZilla](https://filezilla-project.org/download.php?type=client) or [WinSCP](https://winscp.net/eng/download.php).

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and locate your server, then click on the server you want to upload the world to.

4. Navigate to the [FTP Access](https://client.falixnodes.net/server/sftp) tab by hovering over "Advanced" and pressing "FTP Access".

5. Press "Launch SFTP" or input the credentials manually in your SFTP client.

4. Locate the existing world folders named "world", "world_nether", and "world_the_end".

5. Select and delete these folders to remove the current generated world (Make sure to create a backup of any important data you wish to keep).

6. Make sure to rename your world folders to "world", "world_nether", and "world_the_end". (If they are named correctly, you can skip this step).

7. Upload the world folders to the server 

8. Restart your server for the changes to take effect.

The server will now use your uploaded world as the new game world, replacing the previously generated one. Make sure your custom world files are correctly formatted and compatible with your server's version and type to ensure proper functioning.

# How to download a world from the server.

## How to download the world from the server using the File Manenger.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and click on the server you want the world uploaded to.

3. Navigate to the [File Manager](https://client.falixnodes.net/server/filemanager) by hovering over "Manage" and pressing "File Mananger.

4. Locate the existing world folders named "world", "world_nether", and "world_the_end".

5. select these folders and press "archive" in the mass-actions pop-up.

6. download the archive to your computer by hovering over the 3 dot's and pressing "download"

7. extract the downloaded file

{: .warning}
> You might need to install archiving software (like WinRAR or 7zip) to unarchive the .tar.gz file

## How to download the world from the server using SFTP.

{: .info}

> Access via SFTP is only available to Premium users.

{: .info}

> You will need an SFTP client, such as [FileZilla](https://filezilla-project.org/download.php?type=client) or [WinSCP](https://winscp.net/eng/download.php).

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Scroll down and locate your server, then click on the server you want to upload the world to.

4. Navigate to the [FTP Access](https://client.falixnodes.net/server/sftp) tab by hovering over "Advanced" and pressing "FTP Access".

5. Press "Launch SFTP" or input the credentials manually in your SFTP client.

6. Locate the existing world folders named "world", "world_nether", and "world_the_end".

7. Download the folders to your client.