---
layout: post
title: "Resource Packs"
tags: Content
permalink: falix/dashboard/content/resource-packs
description: "Browse and install server-side resource packs from Modrinth and CurseForge."
keywords:
    - keyword: resource pack
      matches: ["texture", "install", "download", "server"]
    - keyword: texture pack
      matches: ["resource", "install", "download", "server"]
author: Lily
---

## Introduction
Resource packs change the way Minecraft looks and sounds. They can replace textures, swap out sound effects, tweak models, update fonts, and completely transform the visual and audio experience of the game -- all without changing any gameplay mechanics. You've probably used one yourself in singleplayer, but server-side resource packs take things a step further.

When you set a resource pack on your server, every player who joins is prompted to download it automatically. That means everyone sees the same custom textures, hears the same custom sounds, and gets a consistent experience -- no manual setup on their end. This is especially powerful for themed servers, RPG worlds, custom adventure maps, or any server where you want a unified visual identity that goes beyond vanilla Minecraft.

The **Resource Packs** page on the dashboard makes this whole process painless. You can browse packs from both Modrinth and CurseForge in one place, pick the one you like, and install it with a single click. Falix handles the rest -- uploading the pack to a CDN, generating the SHA1 hash, and updating your `server.properties` automatically so players are prompted to download it when they connect.

{: .info}
> Resource packs are great for themed servers, RPG worlds, PvP arenas with custom item textures, or just giving your server a unique visual identity that sets it apart.

## Browsing Resource Packs

### Search

Type a name in the search bar to find resource packs. Results are fetched from both Modrinth and CurseForge at the same time and automatically deduplicated, so you won't see the same pack listed twice from different sources.

### Advanced Filters

Click the filter button to narrow down your results. You have several options to work with:

- **Sort By** -- Choose how results are ordered. You can sort by Relevance, Downloads (the default), Follows, Newest, or Recently Updated.
- **Categories** -- Filter by pack type: Adventure, Decoration, Utility, or leave it on Any to see everything.
- **Game Version** -- Narrow results to packs compatible with a specific Minecraft version. This is helpful if you're running an older version and want to make sure the pack will work.
- **Featured Only** -- Toggle this on to see only packs that have been highlighted as featured on their respective platforms.
- **Open Source Only** -- Toggle this on if you want to browse only open-source resource packs.

If you've changed a bunch of filters and want to start fresh, just click **Reset Filters** to go back to the defaults.

### View Modes

You can switch between two layouts depending on how you like to browse:

- **Card View** (the default) -- A 3-column grid that shows each pack's icon, name, description, and stats at a glance. Great for visual browsing.
- **List View** -- A more compact row-based layout if you prefer scanning through a lot of results quickly.

Your preference is saved across sessions, so you won't have to toggle it every time you visit the page.

### Pagination

Results are shown 9 resource packs per page. You can navigate using the first, previous, and next buttons, or jump directly to a specific page if you know roughly where you're headed.

## Resource Pack Details

Click on any resource pack to open a detail modal where you can learn more before installing. The modal has three tabs:

### Overview

This is where you'll find the full description of the pack, information about the author, download and follower statistics, categories, the license it's published under, and any external links the author has provided (like a GitHub repo, wiki, or Discord server).

### Gallery

If the pack author has uploaded screenshots or preview images, you'll find them here. Click on any image to view it fullscreen -- this is a good way to see exactly what the textures look like before committing to an install.

### Versions

A paginated list of every version the pack has released (20 per page). You can filter versions by game version and version type (Release, Beta, or Alpha) to find exactly the right one for your server. Each entry shows the version name, release date, which Minecraft versions it supports, how many times it's been downloaded, and an **Install** button.

{: .info}
> If you're not sure which version to pick, start with the latest Release version that matches your server's Minecraft version. Beta and Alpha versions may have unfinished textures or known issues.

## Installing Resource Packs

Installing a resource pack is a one-click process. Just find the version you want and hit the **Install** button. Here's what happens behind the scenes:

1. The resource pack file is downloaded from its source (Modrinth or CurseForge).
2. It's uploaded to Falix's CDN, giving it a fast, reliable download URL that your players will use.
3. Your server's `server.properties` file is automatically updated with the `resource-pack` URL and the `resource-pack-sha1` hash.

That's it. The next time a player joins your server, their Minecraft client will prompt them to download and apply the resource pack. You don't need to manually edit any config files, upload anything yourself, or fiddle with hash values -- it's all handled for you.

{: .info}
> The SHA1 hash ensures that players download the correct, unmodified version of the resource pack. Minecraft uses this hash to verify the file integrity, so if the pack ever gets corrupted during download, the client will know and can retry.

## Tips for Using Resource Packs

Here are a few things worth keeping in mind:

- **Test before you commit.** Join your server after installing a pack to make sure everything looks right. Some packs may conflict with mods or not cover every texture you expect.
- **Check the game version.** Make sure the resource pack version matches your server's Minecraft version. A pack built for 1.20 might look off on a 1.21 server if new blocks or textures were added.
- **Players can decline.** By default, Minecraft asks players if they want to download the server's resource pack. They can say no. If you want to require it, you'll need to set `require-resource-pack=true` in your `server.properties` file.
- **One pack at a time.** Your server can only have one server-side resource pack set in `server.properties`. Installing a new one will replace the previous one.

## Partial Results Warning

The Resource Packs page pulls results from both Modrinth and CurseForge simultaneously. If one of those sources is temporarily unavailable or slow to respond, you'll see a warning banner at the top of the page letting you know that some results may be missing. This doesn't mean anything is broken on your end -- just that one data source had a hiccup. You can try again in a few minutes or browse what's available in the meantime.
