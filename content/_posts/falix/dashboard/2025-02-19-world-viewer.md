---
layout: post
title: "World Viewer"
tags: Files
permalink: falix/dashboard/files/world-viewer
description: "Visualize your Minecraft world in the browser -- explore a top-down map, inspect regions and chunks, and view blocks in 3D."
keywords:
    - keyword: world viewer
      matches: ["map", "visualize", "region", "chunk", "3d"]
    - keyword: world map
      matches: ["view", "region", "overview", "top-down"]
    - keyword: chunk
      matches: ["view", "3d", "delete", "inspect", "map"]
    - keyword: x-ray
      matches: ["ore", "hidden", "underground", "blocks"]
    - keyword: bulk delete
      matches: ["chunk", "inhabited", "time", "cleanup"]
    - keyword: region
      matches: ["file", "view", "map", "mca"]
author: Lily
---

## Introduction

Ever wanted to see what your Minecraft world looks like from above without launching the game? The World Viewer lets you do exactly that -- right from the dashboard. You can explore a full top-down map of your world, zoom into individual regions to see block-level detail with actual Minecraft textures, and even inspect chunks in 3D.

It is also a practical tool for server maintenance. You can use it to find unexplored areas eating up disk space and bulk-delete chunks that players have barely visited.

{: .info}
> The World Viewer is available for **Minecraft Java Edition** servers only. It reads the `.mca` region files that Java Edition uses to store world data.

## How to Access

There are two ways to open the World Viewer:

1. **From the File Manager** -- Navigate into any world's `region` folder (for example, `world/region`). When the File Manager detects you are in a region folder, a globe icon button appears in the toolbar. Click it to open the World Viewer.

2. **From the Worlds page** -- Click the map icon next to any Java world's name on the [Worlds](/falix/dashboard/content/worlds) page, and it will open the viewer for that world.

## World Map

The World Map is the first thing you see when you open the World Viewer. It displays all your region files stitched together into a single top-down overview of the entire world. Each region covers a 512x512 block area, and they are rendered using actual Minecraft block colors, so you can recognize terrain types at a glance -- green for grass and forests, blue for water, yellow for deserts, white for snow, and so on.

### Navigation

- **Pan** -- Click and drag anywhere on the map to move around
- **Zoom** -- Scroll the mouse wheel to zoom in and out, or use the **+** and **-** buttons in the bottom-right corner
- **Reset View** -- Click the reset button (the arrows icon) to snap back to a view that fits the entire world on screen

The zoom range goes from 0.1x (very zoomed out) up to 4x (zoomed in close).

### Coordinate Display

As you move your mouse across the map, the coordinate display at the bottom shows which region file you are hovering over. For example, you might see **r.0.0.mca** or **r.-3.2.mca**. A checkmark appears next to the name if that region's image has already loaded.

### Stats Panel

The stats panel in the top-left corner shows:

- **Total regions** -- How many region files your world has
- **Loaded** -- How many region images have been rendered so far
- **Progress bar** -- A visual indicator of the loading progress

### Lazy Loading

The World Map does not try to load every region at once. Instead, it only loads the regions that are currently visible on your screen. As you pan and zoom to new areas, those regions load automatically. This keeps things fast and responsive, even for worlds with hundreds of regions.

Regions that have been viewed before are cached, so they load almost instantly the next time you visit them.

### Selecting a Region

Click on any region to select it. A blue highlight border appears around the selected region, and an action panel shows the region file name along with an **Open Region** button. Click **Open Region** to drill into that region and see its chunks in detail using the Chunk Map view.

### Help Bar

A help bar at the bottom of the map reminds you of the controls: click a region to select it, drag to pan, and scroll to zoom.

## Chunk Map

The Chunk Map shows a single region file in much greater detail. Instead of the simplified color view from the World Map, the Chunk Map renders each block using actual Minecraft textures. Height-based shading makes hills appear brighter and valleys darker, giving you a sense of the terrain's shape.

Each region contains up to 32x32 chunks (1,024 chunks total), and each chunk is 16x16 blocks. The full region view is 512x512 blocks.

### How to Access

You reach the Chunk Map by selecting a region in the World Map and clicking **Open Region**. You can also get there by clicking on a `.mca` region file directly from the File Manager.

### Navigation

The Chunk Map uses the same controls as the World Map:

- **Pan** -- Click and drag
- **Zoom** -- Scroll wheel or the +/- buttons (zoom range is 0.5x to 8x)
- **Reset View** -- Click the reset button to center the map

### Chunk Grid

When you zoom in to 2x or higher, a grid overlay appears showing the boundaries of each chunk. This makes it easy to see exactly where one chunk ends and another begins.

### Coordinate Display

The coordinate display at the bottom shows two pieces of information as you hover:

- **Chunk coordinates** -- Which chunk within the region you are pointing at (for example, "Chunk: (12, 7)")
- **Block coordinates** -- The exact block position in world coordinates (for example, "Block: (204, 119)")

### Selecting a Chunk

Click on any chunk that contains data to select it. A blue highlight appears over the selected chunk. Once a chunk is selected, the info panel on the right side of the screen shows details about that chunk, including its position, size, and last modified date. From there, you can:

- **Edit** -- Open the chunk's raw data in the NBT editor
- **3D** -- View the chunk in the 3D Chunk Viewer
- **Delete** -- Remove the chunk from the region file

## 3D Chunk Viewer

The 3D Chunk Viewer lets you explore a single 16x16 chunk as a fully rendered 3D model. Every block in the chunk is displayed with its Minecraft texture, so you can see exactly what is underground, where caves are, and what ores are hidden in the stone.

### How to Access

Select a chunk in the Chunk Map, then click the **3D** button in the info panel. The 3D viewer opens in a modal window on top of the current page.

### Camera Controls

- **Orbit** -- Click and drag to rotate the camera around the chunk
- **Zoom** -- Scroll the mouse wheel to move closer or farther away
- **Reset Camera** -- Click the reset button (the circular arrow icon) to snap back to the default overhead angle

The camera automatically positions itself based on where the blocks are in the chunk, so you do not have to hunt around to find the terrain.

### Y-Level Sliders

Two sliders let you control which vertical layers of the chunk are visible:

- **Min Y** -- The lowest layer shown (default: -64, which is bedrock level)
- **Max Y** -- The highest layer shown (default: 320, which is the build limit)

Adjust these to focus on specific parts of the chunk. For example:

- Set the range to **-64 to 0** to see just the deepslate layer and caves
- Set the range to **60 to 100** to see the surface and a bit above
- Set the range to **-64 to 64** to look at everything below sea level

The label between the sliders updates to show your current range, like "-64 to 120".

### X-Ray Mode

Click the gem icon to toggle X-Ray Mode. This hides all the common "filler" blocks -- stone, dirt, grass, gravel, sand, deepslate, netherrack, water, ice, snow, and many other natural blocks -- leaving behind only the interesting stuff like ores, structures, chests, spawners, and anything players have built.

X-Ray Mode is great for:

- **Finding ores** -- Diamonds, emeralds, iron, gold, copper, and other ores become immediately visible
- **Spotting caves and structures** -- With the surrounding stone removed, cave systems, mineshafts, and strongholds stand out clearly
- **Seeing underground builds** -- Any blocks placed by players (wood, bricks, glass, etc.) remain visible

When X-Ray Mode is active, the gem button is highlighted to remind you it is on. Click it again to go back to the normal view.

### Info Panel

A small info panel at the bottom of the 3D viewer shows:

- The chunk coordinates (for example, "Chunk (12, 7)")
- How many different block types are in the chunk
- The total number of blocks rendered

## Bulk Delete Chunks

Over time, Minecraft worlds can grow very large as players explore in all directions. Much of that space is occupied by chunks that were briefly loaded but never actually played in -- maybe a player ran through the area once or the server pre-generated terrain nearby. These chunks take up disk space without contributing much to the world.

The Bulk Delete Chunks feature lets you clean up your world by removing chunks based on **Inhabited Time** -- a value Minecraft tracks for each chunk that measures how long players have actually spent inside it (in game ticks).

### How to Access

Click the **Bulk Delete Chunks** button in the stats panel on the World Map view. The button has a trash can icon and is located below the loading progress bar.

### The Scanning Process

When you open the bulk delete dialog, it scans all the region files in your world to read the inhabited time for every chunk. A spinner shows the progress while this happens. For worlds that have been scanned before, the results are cached, so it loads much faster on repeat visits.

Once scanning is complete, you will see:

- **Total region count** -- How many region files were scanned
- **Total chunk count** -- How many chunks exist across all regions

### Time Ranges

The dialog presents several time range options, each showing how many chunks fall within that range:

| Range | What it Means |
|-------|---------------|
| **0 seconds (never visited)** | Chunks that were generated but no player has ever been inside them |
| **< 5 seconds** | Chunks a player passed through very briefly |
| **< 30 seconds** | Chunks with minimal player activity |
| **< 1 minute** | Chunks with light player activity |
| **< 5 minutes** | Chunks with moderate player activity |
| **< 30 minutes** | Chunks with significant player activity |

Each option shows the number of matching chunks next to it. Options with zero matching chunks are grayed out.

### Choosing What to Delete

Select one of the time ranges by clicking it. This tells the system to delete all chunks where the inhabited time is at or below that threshold. For example, selecting "< 5 seconds" will delete every chunk where players spent less than 5 seconds total.

{: .info}
> Start with the lowest threshold (0 seconds -- never visited) if you are unsure. These chunks have never had a player in them at all, so they are the safest to remove. Minecraft will regenerate them fresh if a player visits that area later.

### Confirming the Deletion

After selecting a range, click **Delete Selected**{: .red }. A confirmation dialog appears showing the total number of chunks that will be removed. You must confirm again before the deletion proceeds.

{: .warning}
> This action cannot be undone. Always make a backup of your world before performing a bulk delete. You can create a backup from the [Backups](/falix/dashboard/files/backups) page or by downloading the world from the [Worlds](/falix/dashboard/content/worlds) page.

### After Deletion

Once the deletion finishes, you will see a summary of what was removed -- the total number of deleted chunks and how many region files were modified. The World Map then reloads automatically to reflect the changes.

The deleted chunks are not gone forever in-game -- Minecraft will regenerate them with fresh terrain the next time a player explores those areas. This means any player-made builds in those chunks will be lost, but natural terrain will come back.

## Tips and Notes

- **Performance** -- Very large worlds with many regions may take a moment to fully load in the World Map. The lazy loading system keeps things smooth, but you might notice a brief "loading" state as you pan to new areas.
- **Caching** -- Region images are cached on the server after the first time they are generated. If you modify your world (for example, by playing on the server), the cache updates automatically based on file changes.
- **Nether and End** -- The World Viewer works with any dimension that uses the region file format. To view the Nether, navigate to the `DIM-1/region` folder inside your world directory. For the End, use `DIM1/region`.
- **File format** -- The viewer reads `.mca` (Minecraft Anvil) and `.mcr` (older McRegion) files. These are the standard region file formats used by Minecraft Java Edition.
