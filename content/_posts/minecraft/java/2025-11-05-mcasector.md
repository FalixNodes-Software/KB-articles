---
title: How To Clear Unused Chunks Of Your Minecraft Java Server
tags: General
permalink: /minecraft/java/general/world-management
description: A guide on how to save diskspace by deleting unused chucks using MCAselector.
keywords:
    - keyword: mcaselector
      matches: ["how", "use"]
    - keyword: diskspace
      matches: ["full", "server", "error"]
    - keyword: chucks
      matches: ["delete", "remove", "unused"]
author:
    - TWIXhunter
    - Ely
---

Chucks that have been loaded for less than a few minutes are usually only loaded for players traveling through them, but they still take up a lot of space in your world.

Deleting these chunks will:
- Significantly reduce your world size (by up to 90%)
- Preserve all important and actively used areas

### Download your world
1. Download your world folder by following our [World Management Guide](https://kb.falixnodes.net/minecraft/java/general/world-management#downloading-your-world).

2. Unarchive or unzip your world file.

### How to download and install MCAselector
1. Go to the [release page](https://github.com/Querz/mcaselector/releases).

2. Scroll down to the Assets section.

3. Click on the `MCA_Selector_Setup.exe` file to download.

{: .warning }
> Windows flags this 3rd-party program as 'untrusted' because it isn't signed by a trusted dev, please proceed with care.
> You can dismiss the popup by pressing "read more" and "install anyway".

4. Run and complete the installer.

5. Open MCAselector

### Edit your world
1. In the top left-hand corner, hover over "file" and select "open world".

2. Open the world you have just downloaded.

3. At the top, hover over "tools" and select "filter chunks".

4. Change the default `InhabitedTime` section to (at least) `2 minutes`.

> Setting this to more than 2 minutes can cause a destructive selection for a small gain and should only be selected if you know what you are doing.

5. Press "ok" and wait for the selection to complete.

6. Verify that you haven't deleted any important chunks (such as those near spawn).

7. Select or deselect chunks manually using the following keybinds. You might need to zoom in to edit individual chunks:

| Keybind      	| Description    	|
|--------------	|----------------	|
| Arrows       	| Move camera    	|
| WASD         	| Move camera    	|
| Right-Click  	| Deselect chunk 	|
| Left-Click   	| Select chunk   	|
| Scroll       	| Zoom in/out    	|

8. At the top, hover over "Selection" and click on "Delete selected chunks".

9. Close MCAselector, your progress is automatically saved to the folder you selected.

### Upload your world
Upload your world folder by following our [World Management Guide](https://kb.falixnodes.net/minecraft/java/general/world-management#uploading-your-world).

{: .error }

> Make sure you empty the recycle bin after deleting the old world.