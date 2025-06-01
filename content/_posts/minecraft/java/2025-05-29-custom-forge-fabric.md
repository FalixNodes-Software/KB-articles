---
title: Add Custom Forge Or Fabric Versions To Your Minecraft Java Server
tags: General
description: Find out how to use a custom version of forge, fabric and forks not available in the versions list.
keywords:
    - keyword: forge
      matches: ["install", "custom"]
permalink: /minecraft/java/general/custom-forge-fabric
author: TWIXhunter
---

Before proceeding with this guide, we recommend reading our [server software guide](/minecraft/java/general/server-software) to better understand the terms used below.

Often a user will want to use a specific version or software, either because of a modpack requirement or for specific features.

## Instalation
{% tabs softwareType %} 
{% tab softwareType forge  %}
1. Download the official forge installer [here](https://files.minecraftforge.net/net/minecraftforge/forge/).

2. Choose your minecraft and forge version in the menu and download the installer.

3. Do not click on anything in the download site, this is a third-party advertisement, wait for the countdown to fisish and press the skip button in the top right.

4. Create an empty folder.

5. Download and run the installer.

6. Select "server".

7. Enter the location of the temp folder you created.

8. Delete the files called "run.bat" and "run.sh" from the temp folder.

9. Go to "libraries/net/minecraftforge/forge/<version>/" and move the "unix_args.txt" file to the root folder.

10. Compress the temp folder into an archive like .zip or .tar.gz

11. Open the dashboard and navigate to The File Manager.

12. Delete all the content of the File Manager and upload the archive.

13. Unarchive the file by pressing the 3 dots at the end and selecting "unarchive".

   {: .error}
   > Make sure that the all the files are directly in the root folder of the File Manager, if they got added as a folder then open that folder, select all, press "move" in the mass actions bar and enter "/" in the destination field.

14. Start the server.
{% endtab %}




{% tab softwareType neoforge  %}
1. Download the official neoforge installer [here](https://projects.neoforged.net/neoforged/neoforge).

2. Select the wanted minecraft and neoforge version from the dropdowns and download the installer.

3. Create an empty folder.

5. Download and run the installer.

6. Select "server" and enable the "server starter jar" option"

7. Enter the location of the temp folder you created.

8. Delete the files called "run.bat" and "run.sh" from the temp folder.

9. Compress the temp folder into an archive like .zip or .tar.gz

10. Open the dashboard and navigate to The File Manager.

11. Delete all the content of the File Manager and upload the archive.

12. Unarchive the file by pressing the 3 dots at the end and selecting "unarchive".

   {: .error}
   > Make sure that the all the files are directly in the root folder of the File Manager, if they got added as a folder then open that folder, select all, press "move" in the mass actions bar and enter "/" in the destination field.

13. Start the server.
{% endtab %}




{% tab softwareType Fabric  %}
1. Visit the official fabric server download page [here](https://fabricmc.net/use/server/).

2. Select the wanted minecraft and fabric version in the dropdowns.

3. Click the "Executable Server (.jar)" button to start the download.

4. Rename the downloaded file to `server.jar`.

5. Open the dashboard and navigate to The File Manager.

6. Delete all the content of the File Manager and upload the server.jar file.

7. Start the server.
{% endtab %}



{% tab softwareType quilt  %}
1. Visit the official quilt server download page [here](https://quiltmc.org/en/install/client/).

2. Download the installer by clicking  `windows (.exe)` or `universal (.jar)`depending on your platform.

3. Create an empty folder.

3. Run the installer and select `server` at the top.

   {: .warning}
   > Windows Defender may show a warning, this is normal for unsigned third-party tools and it's safe to proceed if downloaded from the official Quilt website; however, since this is third-party software, we are not legally responsible for its use.

4. Select the wanted minecraft and quilt version from the dropdowns.

5. Enter the location of the temp folder you created.

5. Make sure that the "download server jar" option is enabled and press "install"

6. Wait for the instalation to complete.

7. Compress the temp folder into an archive like .zip or .tar.gz

9. Open the dashboard and navigate to The File Manager.

10. Delete all the content of the File Manager and upload the archive.

11. Unarchive the file by pressing the 3 dots at the end and selecting "unarchive".

   {: .error}
   > Make sure that the all the files are directly in the root folder of the File Manager, if they got added as a folder then open that folder, select all, press "move" in the mass actions bar and enter "/" in the destination field.

12. Start the server.
{% endtab %}