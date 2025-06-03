---
title: Add Custom Server Software or Version To Your Minecraft Java Server
tags: General
description: Find out how to use a custom or modified software or version not available in the versions list.
keywords:
    - keyword: custom
      matches: ["software", "jar", "core"]
permalink: /minecraft/java/general/custom-software
author: 
   - Mocab
   - TWIXhunter
---

Before proceeding with this guide, we recommend reading our [server software guide](/minecraft/java/general/server-software) to better understand the terms used below.

Often a user will want to use a specific version or software, either because of a modpack requirement or for specific features. Fortunately, this can be easily done with a custom jar. Custom jars come in two forms: a standalone `.jar` file, or a `.jar` file, a library folder and sometimes other files.

Some Installation processes (like (neo)forge and spigot) might require you to have a Java JRE/JDK package installed. You can find downloads for Java 21 [here](https://adoptium.net/temurin/releases/?os=any&arch=any&version=21)

## Installation
{% tabs softwareType %} 
{% tab softwareType Forge  %}
1. Download the official Forge installer [here](https://files.minecraftforge.net/net/minecraftforge/forge/).

2. Select the desired Minecraft and Forge version in the menu and download the installer.

   {: .warning}
   > Do not click on anything in the download page as this is a third-party ad. Wait for the countdown to finish and press the "Skip" button in the top right

3. Create an empty temporary folder where the installer can generate the server files.

4. Download and run the installer.

5. Select "server".

6. Enter the location of the temporary folder you created.

7. Delete the files called "run.bat" and "run.sh" from the temporary folder.

8. Go to "libraries/net/minecraftforge/forge/<version>/" and move the "unix_args.txt" file to the root of the temporary folder.

9. Compress the temporary folder into an archive like .zip or .tar.gz

10. Open the dashboard and navigate to The File Manager.

11. Delete all the content of the File Manager and upload the archive.

12. Unarchive the file by pressing the 3 dots at the end and selecting "unarchive".

   {: .error}
   > Make sure that all the files are directly in the root folder of the File Manager, if they got added as a folder then open that folder, select all, press "move" in the mass actions bar and enter "/" in the destination field.

13. Start the server.
{% endtab %}




{% tab softwareType NeoForge  %}
1. Download the official NeoForge installer [here](https://projects.neoforged.net/neoforged/neoforge).

2. Select the desired Minecraft and NeoForge version from the dropdowns and download the installer.

3. Create an empty temporary folder where the installer can generate the server files.

4. Download and run the installer.

5. Select "Server" and make sure the "Server starter jar" option is enabled.

6. Enter the location of the temporary folder you created.

7. Delete the files called "run.bat" and "run.sh" from the temporary folder.

8. Compress the temporary folder into an archive like .zip or .tar.gz

9. Open the dashboard and navigate to The File Manager.

10. Delete all the content of the File Manager and upload the archive.

11. Unarchive the file by pressing the 3 dots at the end and selecting "unarchive".

   {: .error}
   > Make sure that all the files are directly in the root folder of the File Manager, if they got added as a folder then open that folder, select all, press "move" in the mass actions bar and enter "/" in the destination field.

12. Start the server.
{% endtab %}




{% tab softwareType Fabric  %}
1. Visit the official Fabric server download page [here](https://fabricmc.net/use/server/).

2. Select the desired Minecraft and Fabric version in the dropdowns.

3. Click the "Executable Server (.jar)" button to start the download.

4. Rename the downloaded file to `server.jar`.

5. Open the dashboard and navigate to The File Manager.

6. Delete all the content of the File Manager and upload the server.jar file.

7. Start the server.
{% endtab %}



{% tab softwareType Quilt  %}
1. Visit the official Quilt server download page [here](https://quiltmc.org/en/install/client/).

2. Download the installer by clicking  `windows (.exe)` or `universal (.jar)` depending on your platform.

3. Create an empty temporary folder where the installer can generate the server files.

4. Run the installer and select `server` at the top.

   {: .warning}
   > Windows Defender may show a warning, this is normal for unsigned third-party tools and it's safe to proceed if downloaded from the official Quilt website; however, since this is third-party software, we are not legally responsible for its use.

5. Select the desired Minecraft and Quilt version from the dropdowns.

6. Enter the location of the temporary folder you created.

7. Make sure that the "download server jar" option is enabled and press "install".

8. Wait for the installation to complete.

9. Open the dashboard and navigate to The File Manager.

10. Delete all the content of the File Manager and upload the server.jar file created in the temporary folder.

11. Start the server.
{% endtab %}

{% tab softwareType Spigot  %}
   {: .warning}
   > We recommend using Paper or Purpur instead of Spigot, as they offer better performance and increased stability.

1. Download the official Spigot Buildtools [here](https://www.spigotmc.org/wiki/buildtools/).

2. Create an empty temporary folder where BuildTools can generate the server files.

3. Run the installer and select the desired Minecraft version.

   {: .warning}
   > Windows Defender may show a warning, this is normal for unsigned third-party tools and it's safe to proceed if downloaded from the official Spigot website; however, since this is third-party software, we are not legally responsible for its use.

4. Enter `server.jar`in the "final name" field.

5. Set the "output directory" to the temporary folder you created.

6. Click the "compile" button and wait for the installation to complete, This may take several minutes.

7. Open the dashboard and navigate to The File Manager.

8. Delete all the content of the File Manager and upload the server.jar file created in the temporary folder.

9. Start the server.
{% endtab %}

{% tab softwareType Paper and forks  %}
1. Open the official website of the wanted software:
   - [Paper (by the PaperMC team)](https://papermc.io/downloads/paper) ([looking for older versions?](https://papermc.io/downloads/all))
   - [Purpur (by the PurpurMC team)](https://purpurmc.org/download/purpur)
   - [Pufferfish (by the pufferfish.host team)](https://pufferfish.host/downloads)

2. Select the desired Minecraft version.

3. Download the server jar

4. rename the downloaded file to `server.jar`

5. Open the dashboard and navigate to The File Manager.

6. Delete all the content of the File Manager and upload the server.jar file.

7. start the server.
{% endtab %}

{% tab softwareType Mohist  %}
1. Visit the official Mohist server download page [here](https://mohistmc.com/downloadSoftware?project=mohist&projectVersion=1.20.1).

2. Select the desired Minecraft version in the dropdown at the right.

3. Click on the Download button of the wanted build and press "mirror download"

4. Rename the downloaded file to `server.jar`

5. Open the dashboard and navigate to The File Manager.

6. Delete all the content of the File Manager and upload the server.jar file.

7. start the server.
{% endtab %}

{% tab softwareType Sponge  %}
1. Visit the official Sponge server download page [here](https://spongepowered.org/downloads/).

2. Choose the wanted sponge project (vanilla, Forge, NeoForge).

3. Select the desired Minecraft version in the dropdown at the right.

4. Click on the Download button of the wanted build.

5. Rename the downloaded file to `server.jar`

6. Open the dashboard and navigate to The File Manager.

7. Delete all the content of the File Manager and upload the server.jar file.

8. start the server.
{% endtab %}

{% tab softwareType Arclight  %}
1. Visit the official Arclight server download page [here](https://arclight.izzel.io/).

3. Select the desired Minecraft version in the dropdown.

4. Choose the wanted Loader (Forge, Fabric, NeoForge).

4. Click on the Download button of the wanted build.

5. Rename the downloaded file to `server.jar`

6. Open the dashboard and navigate to The File Manager.

7. Delete all the content of the File Manager and upload the server.jar file.

8. start the server.
{% endtab %}



{% endtabs %}