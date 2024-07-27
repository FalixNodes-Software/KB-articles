---
layout: help/article
title:  "How to use Plugin Management - Falix"
categories: Minecraft
icon: <i class='fa-light fa-puzzle'></i>
tags: plugins
permalink: /help/minecraft/plugins/management.*
gitURL: _posts/minecraft/plugins/2022-02-28-plugin-management.md
yt: https://youtu.be/BjU7DU1_Sa0
description: "Use Plugin Management for your Minecraft Server at Falix"

author: Korbs
authorGitHub: korbsstudio
---

<div class="watch-video-tutorial">
    <h1>Video Tutorial</h1>
    <iframe id="video-tutorial" width="560" height="315" src="https://www.youtube-nocookie.com/embed/BjU7DU1_Sa0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    <hr>
    <style>section#video-tutorial {display: inherit !important;}</style>
</div>

## Explanation

### What Exactly Are They?

Plugins are similar to browser extensions in Minecraft. These are used by third-party developers to write additional code and plug it into the server. Since they do not change the game itself, as mods do, they are more constrained in what they can do. This, however, implies that they only need to be installed on the server's side. There are no changes required in your own game files to achieve this result.

Plugins perform a number of functions and do not have a particular purpose. They can add a wide assortment of extra commands to help control the server and add in fun and useful mechanics, such as the ability to set who can access and construct in specific areas, add prefixes and suffixes to names, create different ranks with access to different commands, add RPG elements, add virtual economies, and much more.

To spice up your server, there are thousands of plugins available in the Bukkit and Spigot repositories. However, since most of these plugins are created by different developers, incompatibility issues and bugs can spring up whenever a large number of plugins are installed. Sticking to the most widely known plugins is the right alternative since they've been in development for years, are far more mature, and have no compatibility problems with other plugins.

## What Is the Difference Between Plugins and Mods?

Plugins are used to modify and/or improve existing Minecraft server content and can be run using CraftBukkit/Spigot/Paper. They are only used on the server, so players will not have to take any extra steps to connect to a server that's already running plugins.

Mods, which are usually run from Forge, are used to add new items/features to Minecraft and/or improve the existing gameplay. Mods are often required from both the client and server sides (for example, "Biomes O' Plenty"), but some mods are only designed for the client (such as "Optifine" or "Damage Indicators"). Mods can also be put together to form what is known as a modpack (such as "All The Mods 3" or "Sky Factory").

Overall, mods and plugins often don't get along, so it's unlikely that you'll be able to successfully start operating a server for both. However, it is possible, notably if you are willing to run an older version of Minecraft (the most popular for plugin/mod compatibility are 1.7.10 or 1.6.4).

### Installation

## Where to Download?

There are a lot of websites that provide plugins for server administrators.

Here are the websites that we've approved:

- <i class='fa-solid fa-badge-check'></i> [Spigot](https://www.spigotmc.org/)
- <i class='fa-solid fa-badge-check'></i> [Bukkit](https://dev.bukkit.org/)
- <i class='fa-solid fa-badge-check'></i> [CurseForge](https://www.curseforge.com/minecraft/bukkit-plugins)

Some plugins may have their own website.

## Plugin Installation

{: .note }
> Make sure your server software supports plugins.

1. Go to the File Manager.
2. Open the __Plugins__ folder.
3. Upload the plugin, the plugin's file usually ends with __.jar__.
4. Restart your server.

## Configuration

{: .note }
> Only some plugins are configurable.

In the plugins folder, there should be a folder with the plugin's name which contains the configuration files.

Some plugins, like LuckPerms, have a GUI you can use in your browser to configure the plugin.
