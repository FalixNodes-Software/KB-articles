---
title: Add Custom Server Software or Version To Your Minecraft Java Server
tags: Setup
description: Find out how to use a custom or modified software or version not available in the versions list.
keywords:
    - keyword: custom
      matches: ["software", "jar", "core"]
permalink: /minecraft/java/setup/custom-software
author: 
   - TWIXhunter
---

Before proceeding with this guide, we recommend reading our [server software guide](/minecraft/java/general/server-software) to better understand the terms used below.

Often a user will want to use a specific version or software, either because of a modpack requirement or for specific features. Fortunately, this can be easily done with a custom jar. Custom jars come in two forms: a standalone `.jar` file, or a `.jar` file, a library folder and sometimes other files.

Please be aware that we are not affiliated with any of the third-party tools mentioned below. Use them at your own discretion.

Some installation processes (like NeoForge and Spigot) might require you to have a Java JRE/JDK package installed. You can find downloads for Java 21 [here](https://adoptium.net/temurin/releases/?os=any&arch=any&version=21).

## Installation
{% tabs softwareType %} 
{% tab softwareType Forge (1.17 and above)  %}
   {: .warning}
   > These instructions are written for version 1.17 and above, installation for older versions might differ.

1. Download the official Forge installer [here](https://files.minecraftforge.net/net/minecraftforge/forge/).

2. Select the desired Minecraft and Forge version in the menu and download the installer.

   {: .warning}
   > Do not click on anything in the download page as these are third-party ads. Wait for the countdown to finish and press the "Skip" button in the top right.

3. Create an empty temporary folder where the installer can generate the server files.

4. Download and run the installer.

5. Select "Install server".

6. Enter the location of the temporary folder you created.

7. Press "OK" and wait for the installer to finish.

8. Delete the files called `run.bat` and `run.sh` from the temporary folder.

9. Go to the `libraries/net/minecraftforge/forge/<version>/` folder and move the `unix_args.txt` file to the root of the temporary folder.

10. Compress the temporary folder into an archive like `.zip` or `.tar.gz`.

11. Open the Dashboard and navigate to the File Manager.

12. Delete all content from the File Manager and upload the archive.

13. Unarchive the file by pressing the 3 dots at the end and selecting "Unarchive".

   {: .error}
   > Make sure that all the files are directly in the root of the File Manager. If they got added as a folder, then open that folder, select all, press "Move" in the mass actions bar and enter "/" in the destination field.

14. Start the server.
{% endtab %}
{% tab softwareType Forge (1.16.5 and below)  %}
   {: .warning}
   > These instructions are written for version 1.16.5 and below, installation for newer versions might differ.

1. Download the official Forge installer [here](https://files.minecraftforge.net/net/minecraftforge/forge/).

2. Select the desired Minecraft and Forge version in the menu and download the installer.

   {: .warning}
   > Do not click on anything in the download page as these are third-party ads. Wait for the countdown to finish and press the "Skip" button in the top right.

3. Create an empty temporary folder where the installer can generate the server files.

4. Download and run the installer.

5. Select "Install server".

6. Enter the location of the temporary folder you created.

7. Press "OK" and wait for the installer to finish.

8. Open the temporary folder and rename the file called `forge-<version>.jar` to `server.jar`.

9. Compress the temporary folder into an archive like `.zip` or `.tar.gz`.

10. Open the Dashboard and navigate to the File Manager.

11. Delete all content from the File Manager and upload the archive.

12. Unarchive the file by pressing the 3 dots at the end and selecting "Unarchive".

   {: .error}
   > Make sure that all the files are directly in the root of the File Manager. If they got added as a folder, then open that folder, select all, press "Move" in the mass actions bar and enter "/" in the destination field.

13. Start the server.
{% endtab %}

{% tab softwareType NeoForge  %}
1. Download the official NeoForge installer [here](https://projects.neoforged.net/neoforged/neoforge).

2. Select the desired Minecraft and NeoForge version from the dropdowns and download the installer.

3. Create an empty temporary folder where the installer can generate the server files.

4. Download and run the installer.

5. Select "Server" and make sure that the "Server starter jar" option is enabled.

6. Enter the location of the temporary folder you created.

7. Press "Proceed" and wait for the installer to finish.

8. Delete the files called `run.bat` and `run.sh` from the temporary folder.

9. Compress the temporary folder into an archive like `.zip` or `.tar.gz`

10. Open the Dashboard and navigate to the File Manager.

11. Delete all content from the File Manager and upload the archive.

12. Unarchive the file by pressing the 3 dots at the end and selecting "Unarchive".

   {: .error}
   > Make sure that all the files are directly in the root of the File Manager. If they got added as a folder, then open that folder, select all, press "Move" in the mass actions bar and enter "/" in the destination field.

13. Start the server.
{% endtab %}


{% tab softwareType Fabric  %}
1. Visit the official Fabric server download page [here](https://fabricmc.net/use/server/).

2. Select the desired Minecraft and Fabric version in the dropdowns.

3. Click the "Executable Server (.jar)" button to start the download.

4. Rename the downloaded file to `server.jar`.

5. Open the Dashboard and navigate to the File Manager.

6. Delete all content from the File Manager and upload the `server.jar` file.

7. Start the server.
{% endtab %}


{% tab softwareType Quilt  %}
1. Visit the official Quilt server download page [here](https://quiltmc.org/en/install/client/).

2. Download the installer by clicking  `windows (.exe)` or `universal (.jar)` depending on your platform.

3. Create an empty temporary folder where the installer can generate the server files.

4. Run the installer and select `server` at the top.

   {: .warning}
   > Windows Defender may show a warning. This is normal for unsigned third-party tools and it's safe to proceed if downloaded from the official Quilt website; however, since this is third-party software, we are not legally responsible for its use. NEVER download content from suspicious websites!

5. Select the desired Minecraft and Quilt version from the dropdowns.

6. Enter the location of the temporary folder you created.

7. Make sure that the "Download server jar" option is enabled and press "Install".

8. Wait for the installation to complete.

9. Open the Dashboard and navigate to the File Manager.

10. Delete all content from the File Manager and upload the `server.jar` file created in the temporary folder.

11. Start the server.
{% endtab %}


{% tab softwareType Spigot  %}
   {: .warning}
   > We recommend using Paper or Purpur instead of Spigot, as they offer better performance and increased stability.

1. Download the official Spigot Buildtools [here](https://www.spigotmc.org/wiki/buildtools/).

2. Create an empty temporary folder where BuildTools can generate the server files.

3. Run the installer and select the desired Minecraft version.

   {: .warning}
   > Windows Defender may show a warning. This is normal for unsigned third-party tools and it's safe to proceed if downloaded from the official Quilt website; however, since this is third-party software, we are not legally responsible for its use. NEVER download content from suspicious websites!

4. Enter `server.jar` in the "final name" field.

5. Set the "Output directory" to the temporary folder you created.

6. Click the "Compile" button and wait for the installation to complete. This may take several minutes.

7. Open the Dashboard and navigate to the File Manager.

8. Delete all content from the File Manager and upload the `server.jar` file created in the temporary folder.

9. Start the server.
{% endtab %}


{% tab softwareType Paper, Purpur, Pufferfish %}
1. Visit the official website of the wanted software:
   - [Paper (by the PaperMC team)](https://papermc.io/downloads/paper) ([looking for older versions?](https://papermc.io/downloads/all))
   - [Purpur (by the PurpurMC team)](https://purpurmc.org/download/purpur)
   - [Pufferfish (by the pufferfish.host team)](https://pufferfish.host/downloads)
   - [LeafMC (by Winds-Studio)](https://www.leafmc.one/download)

2. Select the desired Minecraft version.

3. Download the wanted build.

4. Rename the downloaded file to `server.jar`.

5. Open the Dashboard and navigate to the File Manager.

6. Delete all content from the File Manager and upload the `server.jar` file.

7. Start the server.
{% endtab %}


{% tab softwareType Sponge, Mohist, Arclight %}
1. Open the official website of the wanted software:
   - [SpongeVanilla (by spongepowered)](https://spongepowered.org/downloads/spongevanilla)
   - [SpongeForge (by spongepowered)](https://spongepowered.org/downloads/spongeforge)
   - [SpongeNeo (by spongepowered)](https://spongepowered.org/downloads/spongeneo)
   - [Mohist (by mohistMC)](https://mohistmc.com/downloadSoftware?project=mohist)
   - [Banner (by mohistMC)](https://mohistmc.com/downloadSoftware?project=banner)
   - [Youer (by MohistMC)](https://mohistmc.com/downloadSoftware?project=youer)
   - [Arclight (by izzel.io)](https://arclight.izzel.io/)

2. Select the desired version in the dropdown(s).

3. Download your preferred build.

4. Rename the downloaded file to `server.jar`.

5. Open the Dashboard and navigate to the File Manager.

6. Delete all content from the File Manager and upload the `server.jar` file.

7. Start the server.
{% endtab %}


{% tab softwareType Velocity %}
1. Visit the official Velocity server download page [here](https://papermc.io/downloads/velocity).

3. Download the latest build.

4. Rename the downloaded file to `server.jar`.

5. Open the Dashboard and navigate to the File Manager.

6. Delete all content from the File Manager and upload the `server.jar` file.

7. Start the server.
{% endtab %}

{% tab softwareType BungeeCord %}
1. Visit the official BungeeCord server download page [here](https://ci.md-5.net/job/BungeeCord/).

3. Download the latest build by clicking `BungeeCord.jar` under the `lastSuccessfulArtifacts` category.

4. Rename the downloaded file to `server.jar`.

5. Open the Dashboard and navigate to the File Manager.

6. Delete all content from the File Manager and upload the `server.jar` file.

7. Start the server.
{% endtab %}


{% endtabs %}