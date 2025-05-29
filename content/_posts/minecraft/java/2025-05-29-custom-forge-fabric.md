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

2. Choose your minecraft version in the menu and download the installer.

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
