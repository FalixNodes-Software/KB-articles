---
layout: post
title: "Choosing the Right Minecraft Server Jar"
category: Java
tags: General
description: "Choosing the right Minecraft server jar is crucial for optimizing performance, features, and compatibility with plugins and mods. Explore options for hybrid, modded, and proxy servers to find the best fit for your setup."
permalink: /minecraft/java/configuration/choosing-the-right-minecraft-server-jar
author:
    - Lovinoes
---

## Introduction
Selecting the right Minecraft server jar is essential for optimizing performance, gameplay features, and ensuring compatibility with plugins and mods. Each server jar offers unique benefits and trade-offs, making the choice dependent on your specific needs. This guide covers a range of options including Pufferfish, Paper, Purpur, Spigot, and Vanilla, alongside specialized jars like Quilt, NeoForge, Mohist, Magma, Arclight, and proxies such as BungeeCord, Waterfall, and Velocity. Whether you're looking for high performance, extensive mod support, or hybrid solutions, this guide will help you make an informed decision.

<!-- Let's start with the normal ones: Pufferfish, Paper, Purpur, Spigot, SpongeVanilla -->
<!-- chaotic version: https://luminescent.dev/forks/ -->

## Server Jars Overview
### Pufferfish
Pufferfish is a high-performance server jar based on Paper, designed to enhance server efficiency while maintaining compatibility with Paper-based plugins and features.

### Paper
Paper is a widely-used server jar built on Spigot/Bukkit, offering improved performance and extensive plugin support while balancing vanilla Minecraft compatibility.

### Purpur
Purpur is a fork of Pufferfish that adds additional non-vanilla gameplay features and extensive customization options, while retaining Pufferfish’s performance benefits.

### Spigot
Spigot is an early server jar derived from Bukkit, known for its performance optimizations and support for a wide range of plugins, though not as advanced as Paper.

### Vanilla
The Vanilla server jar is the unmodified, default Minecraft server software, providing the pure Minecraft experience without additional performance optimizations or features.

### SpongeVanilla
SpongeVanilla is a standalone server jar that implements the SpongeAPI without Forge mods, offering a pure plugin-based experience similar to other plugin-oriented jars.
- **Plugin-Only Server**: SpongeVanilla is ideal if you only need Sponge plugins and do not require the extensive mod support of Forge.
- **API Features**: Provides access to Sponge's plugin API for advanced server customization and performance improvements.


<!-- Modded Servers: Fabric, Forge, NeoForge, Quilt, SpongeForge -->


## Modded Servers
### Fabric
Fabric is a modern modding framework designed for Minecraft, known for its large ecosystem of game-optimizing mods. Here’s why you might consider Fabric:
- **Extensive Modding Capabilities**: Fabric supports a wide range of complex mods, offering additional features and functionality.
- **Performance Improvements**: Known for its performance-enhancing mods, Fabric can sometimes provide a smoother experience compared to Vanilla.
- **Regular Updates**: Fabric is frequently updated to support the latest Minecraft versions and snapshots, making it ideal for those wanting to stay current.

**Opposing View**:
- **Mod Library Size**: While Fabric’s library is growing, it still lags behind Forge in terms of the number of available mods.
- **Compatibility**: Fabric is often better suited for newer versions of Minecraft and may not be the best choice for older versions. Modpacks can also require multiple mods, increasing the complexity.


### Forge
Forge is the classic modding framework for Minecraft, widely used for extensive modpacks. Here’s why Forge might be right for you:
- **Extensive Mod Ecosystem**: Forge supports a vast array of mods, offering a rich selection of features and functionalities.
- **Well-Documented Modpacks**: Many popular modpacks, especially for older Minecraft versions, use Forge and are well-documented online.
- **Feature-Rich Mods**: Forge mods tend to be packed with a wide range of features, enhancing gameplay.

**Opposing View**:
- **Update Frequency**: Forge updates less frequently than Fabric, and its community for older versions can be less active.
- **Performance**: Forge can be heavier on resources compared to Vanilla, which may impact performance.


### NeoForge
NeoForge is a modern continuation of the Forge project, tailored to be more modular and maintainable. It's built to ensure compatibility with older Forge mods while improving performance and maintaining stability.
- **Compatibility with Legacy Mods**: NeoForge is designed to work with existing Forge mods, making it a good choice for those with legacy modpacks.
- **Active Development**: NeoForge is under active development, ensuring better support for modern Minecraft versions.


### Quilt
Quilt is a lightweight, modular modding framework that builds on Fabric, offering enhanced stability and mod compatibility. It’s a good choice if you’re looking to experiment with modding on newer versions of Minecraft while using Fabric mods seamlessly.
- **Enhanced Mod Compatibility**: Quilt focuses on improving mod compatibility and reducing conflicts between mods.
- **Modular Design**: Its modular approach allows for a more customizable server setup, potentially improving performance.

### SpongeForge
SpongeForge combines the SpongeAPI with Forge, allowing you to run Sponge plugins alongside Forge mods. Here’s what you should know:
- **Plugin and Mod Integration**: SpongeForge enables you to use Sponge plugins with Forge mods, providing a flexible environment for modding and plugin use.
- **Customizable Server**: With SpongeForge, you can leverage the extensive modding capabilities of Forge while incorporating Sponge's powerful plugin API.


<!-- Hybrid Servers: Mohist, Magma, Arclight -->


## Hybrid Servers
Hybrid servers combine the capabilities of both modded and plugin-based servers, allowing for a versatile environment where both can coexist.

### Mohist
Mohist is a server jar that combines the capabilities of Forge and Bukkit, allowing for the use of both Forge mods and Bukkit plugins. It’s ideal for servers that need to blend the extensive modding capabilities of Forge with the versatility of Bukkit plugins.
- **Mod and Plugin Support**: Run both mods and plugins simultaneously, which makes Mohist a flexible option for heavily customized servers.
- **Community Support**: Mohist has a strong community backing, providing regular updates and fixes.

{: .info}
> **PSA: Do not use Mohist.** It has a history of malicious behavior and security risks. Running untrusted code can compromise your server: [EssentialsX - Why You Shouldn't Use Mohist](https://essentialsx.net/do-not-use-mohist.html)


### Magma
Magma is another hybrid server jar that allows the combination of Forge mods with Bukkit/Spigot/Paper plugins. It focuses on providing a stable environment where both mods and plugins can coexist without major conflicts.
- **Stability**: Magma prioritizes stability, reducing the risk of crashes and conflicts when using mods and plugins together.
- **Wide Compatibility**: It’s compatible with a broad range of Minecraft versions, making it suitable for both newer and older modpacks.

{: .info}
> **Note on Magma**: As of **November 15, 2023**, the owner of **MagmaFoundation** decided to **shut down the project**.

### Arclight
Arclight is similar to Mohist, providing a hybrid environment that supports both Forge mods and Spigot plugins. It is particularly known for its performance optimizations and compatibility with large modpacks.
- **Performance-Oriented**: Arclight is optimized for better performance, especially when running large modpacks alongside plugins.
- **Custom Features**: Offers some unique features and tweaks that are not available in other hybrid jars, making it a good choice for custom servers.


<!-- Proxies: Bungee, Waterfall, Velocity -->


## Proxies
Proxies are server software that allow multiple Minecraft servers to be linked together, providing features like server networks, cross-server communication, and improved player management. Here are some of the most popular proxies:

### BungeeCord
BungeeCord is one of the most widely used Minecraft proxies, enabling the linking of multiple Minecraft servers into a single network. It allows players to switch between servers seamlessly without disconnecting.
- **Ease of Use**: BungeeCord is straightforward to set up and manage, making it a popular choice for networked servers.
- **Cross-Server Features**: Supports cross-server chat, global player lists, and more.


### Waterfall
Waterfall is a fork of BungeeCord that offers additional performance improvements and bug fixes. It's designed to provide a more stable and efficient proxy experience.
- **Performance and Stability**: Waterfall improves upon BungeeCord's performance and stability, making it a better choice for larger networks.

{: .info}
> **Note on Waterfall**: Waterfall has reached its end of life, and it is recommended to transition to Velocity. For more information, see the announcement on the [PaperMC website](https://forums.papermc.io/threads/1088/).


### Velocity
Velocity is the modern, high-performance proxy designed with performance and stability in mind. It’s a full alternative to Waterfall with its own plugin ecosystem.
- **High Performance**: Velocity is known for its low-latency performance, making it ideal for large, busy networks.
- **Enhanced Security**: It includes advanced security features, helping to protect your network from attacks and exploits.
- **Active Development and Ecosystem**: Velocity is actively maintained and has its own plugin ecosystem, making it a forward-looking choice for modern Minecraft server networks.

<!-- END -->

## Conclusion
- **For Optimal Performance**: Choose **Pufferfish** for a performance-focused server that remains close to Paper's behavior.
- **For a Stable and Supported Server**: Opt for **Paper** if you want a balance of performance and compatibility with a wide range of plugins.
- **For Extra Features**: Use **Purpur** if you want additional gameplay features and customization while maintaining the performance base of Pufferfish.
- **For Basic Performance and Broad Plugin Support**: Use **Spigot** if you need a reliable server with broad plugin support.
- **For a Sponge Focused Server**: Choose **SpongeVanilla** if you want to use Sponge plugins without the need for Forge mods, ensuring a streamlined plugin experience.
- **For Modern Modding**: Choose **Fabric** for a large modding ecosystem with performance benefits, **Forge** for extensive mod support and classic modded gameplay, or **SpongeForge** for integrating Sponge plugins with Forge mods.
- **For Combining Plugins and Mods**: Consider **Mohist**, **Magma**, **Arclight**, **NeoForge**, or **Quilt** based on your specific needs for modding and plugin compatibility.
- **For Networking Multiple Servers**: Use **Velocity** a modern, high-performance proxy with its own plugin ecosystem. **Waterfall** has reached its end of life, and it is recommended to transition to Velocity. For more details, see the announcement on the [PaperMC website](https://forums.papermc.io/threads/1088/). **BungeeCord** is laden with bugs, exploits, and other issues, and receives very little maintenance. For these reasons, we highly recommend against running BungeeCord proxies.

<!-- SpongeForge can be considered hybrid as it combines the capabilities of Forge, which is a modding platform, with Sponge which is a plugin API -->
{: .info}
> **Note**: We suggest against promoting the usage of hybrid server software, except for **SpongeForge**, to avoid potential issues with compatibility and stability.

Select the server jar or proxy that best fits your needs to ensure an optimized and enjoyable Minecraft server experience.
