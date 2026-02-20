---
title: Migrating Your Minecraft Java World Between Vanilla and Spigot
tags: Worlds
description: Convert a vanilla world to or from Spigot or any of its forks.
keywords:
    - keyword: convert
      matches: &convert_matches ["world", "map"]
    - keyword: migrate
      matches: *convert_matches
permalink: /minecraft/java/worlds/migrate-world
author: Mocab
---

Server software such as Spigot, Paper, Purpur and any of their forks use a different world folder structure than the standard vanilla structure. To increase customisation and add the ability to use a different seed or generation setting for each dimension, they move the `DIM-1` and `DIM1` sub-folders to `world_nether` and `world_the_end` respectively.

## Converting to the Spigot Format

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Make sure your server is turned off by clicking on "**Stop**{: .red }" at the top right of the console.

4. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Click on "**Create Folder**{: .green }" and type `world_nether` in the "Folder Name" field.

6. Once again click on "**Create Folder**{: .green }" to make your folder.

7. Repeat the same steps to create a folder, but this time call it `world_the_end`.

8. Locate and open your world folder, this is usually just called [world](https://client.falixnodes.net/server/filemanager?dir=/world/).

9. Locate the "DIM-1" folder and click on the three dots to its right, then click on "Move".

10. To move the folder into the "world_nether" folder, type `/world_nether/DIM-1/` then click "**Move File**{: .green }".

11. Repeat the same steps for "DIM1", but use `/world_the_end/DIM1/` instead.

## Converting to the Vanilla Format

{: .warning }

> Make a backup before proceeding. We **do not** recommend doing this if you have different seeds set for each dimension.

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Make sure your server is turned off by clicking on "**Stop**{: .red }" at the top right of the console.

4. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

5. Locate and open the nether world folder, this is usually just called [world_nether](https://client.falixnodes.net/server/filemanager?dir=/world_nether/).

6. Locate the "DIM-1" folder and click on the three dots to its right, then click on "Move".

7. To move the folder into the "world" folder, type `/world/DIM-1/` then click "**Move File**{: .green }".

8. Navigate back to the [root directory](https://client.falixnodes.net/server/filemanager) by clicking on the "Go Back" button at the top of the file list or by returning to the [File Manager](https://client.falixnodes.net/server/filemanager).

9. Locate and open the end world folder, this is usually just called [world_the_end](https://client.falixnodes.net/server/filemanager?dir=/world_the_end/).

10. Locate the "DIM1" folder and click on the three dots to its right, then click on "Move".

11. To move the folder into the "world" folder, type `/world/DIM1/` then click "**Move File**{: .green }".
