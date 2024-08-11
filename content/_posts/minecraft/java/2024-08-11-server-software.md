---
layout: post
title: Choosing Minecraft Server Software
category: Java
tags: General
description: Explore options for mod, plugin, hybrid and proxy servers to find the best fit for your setup.
permalink: /minecraft/java/configuration/server-software
author: Lovinoes
---

## Introduction
Selecting the right Minecraft server jar is essential for optimizing performance, gameplay features, and ensuring compatibility with plugins and mods. Each server jar offers unique benefits and trade-offs, making the choice dependent on your specific needs. This guide covers a wide-range of options. Whether you're looking for high performance, extensive mod support, or hybrid software, this guide will help you make an informed decision.

<!-- Let's start with the normal ones: Pufferfish, Paper, Purpur, Spigot, SpongeVanilla -->
<!-- chaotic version: https://luminescent.dev/forks/ -->
## Server Jars Overview
1. [Paper](https://papermc.io/) *(The most widely used, high performance Minecraft server that aims to fix gameplay and mechanics inconsistencies )*
2. [Purpur](https://purpurmc.org/) *(Purpur is a drop-in replacement for Paper servers designed for configurability and new, fun, exciting gameplay features. )*
3. [Pufferfish](https://github.com/pufferfish-gg/Pufferfish) *(A highly optimized Paper fork designed for large servers requiring both maximum performance, stability, and "enterprise" features.)*
4. [Spigot](https://www.spigotmc.org/) *(Spigot is a modified version of CraftBukkit with hundreds of improvements and optimizations that can only make CraftBukkit shrink in shame.)*
5. [SpongeVanilla](https://spongepowered.org/) *(SpongeVanilla is the implementation of the Sponge API on top of Vanilla Minecraft.)*


### Paper
Paper is an extremely popular and widely used server software based on Spigot, offering improved performance, extensive plugin support and more configurations.

### Purpur
Purpur is a fork of Pufferfish that adds many additional features and extensive customization options, while retaining Pufferfish's performance benefits.

### Pufferfish
Pufferfish is a server software based on Paper, designed to enhance server performance while maintaining parity with Paper plugins and features.

### Spigot
Spigot is the most widely used server software based on Bukkit, known for its performance optimizations, configuration options and features, serving as a stable base.

### SpongeVanilla
SpongeVanilla is a standalone server jar that implements the SpongeAPI without Forge mods, offering a pure plugin-based experience similar to other plugin-oriented jars.



## Modded Server Jars
1. [Fabric](https://fabricmc.net/) *(Fabric is a modular, lightweight mod loader for Minecraft)*
2. [NeoForge](https://neoforged.net/) *(NeoForge is a fork of Forge that adds modding features such as capabilities, events, and registry.)*
3. [Forge](https://files.minecraftforge.net/net/minecraftforge/forge/) *(Forge is a free, open-source modding API and loader designed to simplify compatibility between community-created mods.)*
4. [Quilt](https://quiltmc.org/) *(Quilt is an open-source, community-driven modding toolchain designed primarily for Minecraft. Focusing on speed, ease of use, and modularity, Quilt aims to provide a sleek and modern modding toolchain with an open ecosystem.)*

### Fabric
Fabric is a modern modding framework designed for Minecraft, known for its large ecosystem of game-optimizing mods.
- **Extensive Modding Capabilities**: Fabric supports a wide range of complex mods, offering additional features and functionality.
- **Regular Updates**: Fabric is frequently updated to support the latest Minecraft versions and snapshots, making it ideal for those wanting to stay current.

### NeoForge
NeoForge is a modern continuation of the Forge project, tailored to be more modular and maintainable. It's built to ensure compatibility with older Forge mods while improving performance and maintaining stability.
- **Compatibility with Legacy Mods**: NeoForge is designed to work with existing Forge mods, making it a good choice for those with legacy modpacks.
- **Active Development**: NeoForge is under active development, ensuring better support for modern Minecraft versions.

### Forge
Forge is the classic modding framework for Minecraft, widely used for extensive modpacks.
- **Extensive Mod Ecosystem**: Forge supports a vast array of mods, offering a rich selection of features and functionalities.
- **Well-Documented Modpacks**: Many popular modpacks, especially for older Minecraft versions, use Forge and are well-documented online.

### Quilt
Quilt is a lightweight, modular modding framework that builds on Fabric, offering enhanced stability and mod compatibility.
- **Enhanced Mod Compatibility**: Quilt focuses on improving mod compatibility and reducing conflicts between mods.
- **Modular Design**: Its modular approach allows for a more customizable server setup, potentially improving performance.




## Hybrid Server Jars
Hybrid servers combine the capabilities of both mod and plugin servers, allowing for a versatile environment where both can coexist.

{: warning}
> Hybrid server software combining modloaders with Bukkit/Sponge may cause issues.

1. [SpongeForge](https://spongepowered.org/) *(SpongeForge integrates Forge so you can also run Forge mods. It’s more like Sponge itself is a Forge mod that then loads Sponge plugins)*
2. [Arclight](https://github.com/IzzelAliz/Arclight) *(A Bukkit server implementation in modding environment using Mixin.)*
3. [Mohist](https://mohistmc.com/) *(Minecraft Forge Hybrid server implementing the Spigot/Bukkit API, formerly known as Thermos/Cauldron/MCPC+)*
4. [Magma](https://github.com/magmafoundation/Magma) *(Minecraft Forge Hybrid server implementing the Spigot/Bukkit API (Cauldron for 1.12))*

### SpongeForge
SpongeForge combines the SpongeAPI with Forge, allowing you to run Sponge plugins alongside Forge mods. Here’s what you should know:
- **Stability**: SpongeForge is a mature and well-engineered solution that integrates Sponge with Forge.

### Arclight
Arclight is similar to Mohist, providing a hybrid environment that supports either Forge or Fabric mods and Spigot plugins.
- **Custom Features**: Offers some unique features and tweaks that are not available in other hybrid jars.

### Mohist
Mohist is a server jar that combines the capabilities of Forge and Bukkit, allowing for the use of both Forge mods and Bukkit plugins. It’s ideal for servers that need to blend the extensive modding capabilities of Forge with the versatility of Bukkit plugins.
- **Mod and Plugin Support**: Run both mods and plugins simultaneously, which makes Mohist a flexible option for heavily customized servers.
- **Community Support**: Mohist has a strong community backing, providing regular updates and fixes.

{: .warning}
> **Do not use Mohist.** It has a history of malicious behavior and security risks. Running untrusted code can compromise your server: [EssentialsX - Why You Shouldn't Use Mohist](https://essentialsx.net/do-not-use-mohist.html)

### Magma
Magma is a hybrid server software that allows the combination of Forge mods with Spigot plugins.
- **Wide Compatibility**: It’s compatible with a broad range of Minecraft versions, making it suitable for both newer and older modpacks.

{: .warning}
> **Note on Magma**: As of **November 15, 2023**, the owner of **MagmaFoundation** decided to **shut down the project**.




## Proxies
Proxies are server software that allow multiple Minecraft servers to be linked together, providing features like server networks, cross-server communication, and improved player management. Here are some of the most popular proxies:

1. [Velocity](https://papermc.io/) *(Velocity is a ridiculously scalable, flexible Minecraft proxy.)*
2. [Waterfall](https://papermc.io/) *(Waterfall is the BungeeCord fork that aims to improve performance and stability.)*
3. [BungeeCord](https://www.spigotmc.org/) *(BungeeCord is a server software that enables players to create a network of Minecraft servers.)*

### Velocity
Velocity is a modern, high performance proxy designed with performance and stability in mind, a solid alternative to Waterfall or BungeeCord with its own plugin ecosystem.
- **High Performance**: Velocity is known for its low latency, making it ideal for large, busy networks.
- **Enhanced Security**: It includes advanced security features, helping to protect your network from attacks and exploits.
- **Active Development**: Velocity is actively maintained and has its own plugin ecosystem, making it a forward-looking choice for modern Minecraft server networks.

### Waterfall
Waterfall is a fork of BungeeCord that offers additional performance improvements and bug fixes. It's designed to provide a more stable and efficient proxy experience.
- **Performance and Stability**: Waterfall improves upon BungeeCord's performance and stability, making it a better choice for larger networks.

{: .warning}
> Waterfall has reached its end of life, and it is recommended to transition to Velocity. For more information, see the announcement on the [PaperMC website](https://forums.papermc.io/threads/1088/).

### BungeeCord
BungeeCord is one of the most widely used Minecraft proxies, enabling the linking of multiple Minecraft servers into a single network. It allows players to switch between servers seamlessly without disconnecting.
- **Ease of Use**: BungeeCord is straightforward to set up and manage, making it a popular choice for networked servers.
- **Cross-Server Features**: Supports cross-server chat, global player lists, and more.


{: .warning}
> BungeeCord is no longer actively maintained and has many exploits or issues. It is recommended to use Velocity instead.



## Conclusion
- **Stable**: Opt for **Paper** if you want a balance of performance and compatibility with a wide range of plugins.
- **Best Performance**: Choose **Pufferfish** for a performance focused server.
- **Extra Features**: Use **Purpur** if you want additional gameplay features and customization while maintaining the performance base of Pufferfish.
- **Modloaders**: Choose **Fabric** for a large modding ecosystem with performance benefits, **NeoForge** for extensive mod support and classic modded gameplay.
- **Hybrid**: Choose **Arclight** or **SpongeForge** based on your specific needs for modding and plugin compatibility.
- **Proxies**: Use **Velocity** - a modern, high performance proxy with its own plugin ecosystem.

<!-- SpongeForge can be considered hybrid as it combines the capabilities of Forge, which is a modding platform, with Sponge which is a plugin API -->
