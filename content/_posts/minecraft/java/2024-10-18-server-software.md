---
title: How To Pick the Best Minecraft Java Server Software
tags: Setup
description: Explore different server flavors and software to find the best fit for mod, plugin, hybrid or proxy setups.
keywords:
    - keyword: server
      matches: ["software", "jar", "core"]
permalink: /minecraft/java/setup/server-software
author:
    - Lovinoes
    - Mocab

getting-started-tag: Minecraft
post_order: 2
---

Selecting the right Minecraft server jar is essential for optimizing performance, game-play features, and ensuring compatibility with plugins and mods. Each server jar offers unique benefits and trade-offs, making the choice dependent on your specific needs. This guide covers a wide-range of options. Whether you're looking for high performance, extensive mod support, or hybrid software, this guide will help you make an informed decision.

Before we proceed, the terms "fork" and "based off" must be explained. Software that is forked or is based on another contains all additions and changes from the upstream software. Therefore, any plugin or mod designed for upstream software can also be run on forked software. For example, Paper is a fork of Spigot (upstream), and so any changes, optimizations and configurations in Spigot are included in Paper, and any plugins made for Spigot will work when using Paper. And by extension, these changes and plugin support also apply and extend to software forked from other forked software, such as Spigot and Paper changes and plugins being supported in Purpur (fork of Paper).

## Official Minecraft Software:

{% tabs official %}
{% tab official <i class="java-software java"></i> Vanilla %}

[Vanilla](https://www.minecraft.net/en-us/download/server) is the default software provided by Minecraft. It does not contain any modifications, nor does it support plugins or mods. We recommend using other, better alternatives.

{% endtab %}
{% tab official <i class="java-software snapshot"></i> Snapshot %}

Snapshots are a testing version of Minecraft released by Mojang. They contain new features and additions to the game. They are released to the public in order for players to try out the new features and test if they function as intended. We **do not** advise using this software, as it may contain bugs or game-breaking changes.

{% endtab %}
{% endtabs %}

## Plugins:

{% tabs plugin %}
{% tab plugin <i class="java-software spigot"></i> Spigot %}

[Spigot](https://www.spigotmc.org/) is a modified version of Bukkit with improvements and optimizations. We **do not** recommend using this software as there are many better alternatives, such as Paper and Purpur. Furthermore, it changes many aspects of the game, which may be a deal breaker for admins looking for a vanilla experience.

{% endtab %}
{% tab plugin <i class="java-software paper"></i> Paper <i class="recommended"></i> %}

[Paper](https://papermc.io/) is an extremely popular and widely used server software based on Spigot, offering improved performance, extensive plugin support and more configurations. It is recommended to use this software both due to its performance gains and its support for Bukkit, Spigot and its own plugin API. The only downside is that Paper aims to fix many of the game's bugs and inconsistencies, providing a slightly non-vanilla experience. However, many of these changes can still be configured to be more vanilla-like and often only affect very technical players.

{% endtab %}
{% tab plugin <i class="java-software purpur"></i> Purpur <i class="recommended"></i> %}

[Purpur](https://purpurmc.org/) is a fork of Paper; however, it also includes Pufferfish's optimizations on top of its own configuration additions. Making it a great choice for administrators looking for more customizable server software with the added bonus of both the optimizations from Paper and Pufferfish. In addition, it provides support for Spigot, Bukkit, and Paper plugins. We recommend using this server software. Unfortunately just like Paper, Purpur does not provide a true vanilla experience although the changes are minute and can be adjusted.

{% endtab %}
{% tab plugin <i class="java-software pufferfish"></i> Pufferfish <i class="recommended"></i> %}

[Pufferfish](https://github.com/pufferfish-gg/Pufferfish) is a server software based on Paper, designed to tremendously enhance server performance while maintaining parity with Bukkit, Spigot and Paper plugins and features. Unfortunately, just like Paper and Purpur, Pufferfish does not provide a true vanilla experience, but as mentioned before, these changes are minute and can be adjusted.

{% endtab %}
{% tab plugin <i class="java-software sponge"></i> SpongeVanilla %}

[SpongeVanilla](https://spongepowered.org/) is a standalone server jar that implements the SpongeAPI without Forge mods, offering a pure plugin-based experience similar to other plugin-oriented jars; however, only Sponge plugins will work.

{% endtab %}
{% endtabs %}

## Modded Server Jars:

{% tabs mod %}
{% tab mod <i class="java-software fabric"></i> Fabric <i class="recommended"></i> %}

[Fabric](https://fabricmc.net/) is a lightweight and modern modding framework designed for Minecraft, known for its large ecosystem of game-optimizing mods, its support for a wide range of complex mods and its regular updates. We recommend using this software in addition to a few optimization mods for the best vanilla experience.

{% endtab %}
{% tab mod <i class="java-software neoforge"></i> NeoForge <i class="recommended"></i> %}

[NeoForge](https://neoforged.net/) is a modern continuation of the Forge project, tailored to be more modular and maintainable. It's built to ensure compatibility with older Forge mods while improving performance and maintaining stability.

{% endtab %}
{% tab mod <i class="java-software forge"></i> Forge %}

[Forge](https://files.minecraftforge.net/) is the classic modding framework for Minecraft, widely used for extensive mod-pack ecosystem and its vast array of mods, offering a rich selection of features and functionalities.

{% endtab %}
{% tab mod <i class="java-software quilt"></i> Quilt %}

[Quilt](https://quiltmc.org/en/) is a lightweight, modular modding framework that builds on Fabric, offering enhanced mod compatibility.

{% endtab %}
{% endtabs %}

## Hybrid Server Jars:

Hybrid servers combine the capabilities of both mod and plugin servers, allowing for a versatile environment where both can coexist.

{: warning}

> Plugins and mods are in no way designed to work together, and running them side by side will cause many compatibility and performance issues. If you want to avoid hours of troubleshooting and never-ending issues, it is best to stay away from hybrid software.

{% tabs hybrid %}
{% tab hybrid <i class="java-software sponge"></i> SpongeForge %}

[SpongeForge](https://spongepowered.org/) is a well-engineered solution combines the SpongeAPI with Forge, allowing you to run Sponge plugins alongside Forge mods.

{% endtab %}
{% tab hybrid <i class="java-software arclight"></i> Arclight %}

[Arclight](https://github.com/IzzelAliz/Arclight) provides a hybrid environment that supports Forge, Fabric or NeoForge mods and Spigot plugins with a few extra unique features and tweaks.

{% endtab %}
{% tab hybrid <i class="java-software mohist"></i> Mohist %}

[Mohist](https://mohistmc.com/) combines the capabilities of Forge, Fabric or NeoForge mods and Spigot, allowing for the use of a mod-loader and Bukkit and Spigot plugins.

{% endtab %}
{% tab hybrid <i class="java-software magma"></i> Magma %}

[Magma](https://github.com/magmafoundation/Magma) is a hybrid server software that allows the combination of Forge mods with Spigot plugins. It’s compatible with a broad range of Minecraft versions, making it suitable for both newer and older mod-packs.

{: .warning}

> As of **November 15, 2023**, the owner of MagmaFoundation has decided to shut down the project.

{% endtab %}
{% endtabs %}

## Proxies:

Proxies are server software that allow multiple Minecraft servers to be linked together, providing features like server networks, cross-server communication, and improved player management. Here are some of the most popular proxies:

{% tabs proxy %}
{% tab proxy <i class="java-software velocity"></i> Velocity <i class="recommended"></i> %}

[Velocity](https://papermc.io/software/velocity) is a modern, high performance proxy designed with performance and stability in mind, a solid alternative to Waterfall or BungeeCord with its own plugin ecosystem. We recommend using this server software.

{% endtab %}
{% tab proxy Waterfall %}

[Waterfall](https://github.com/PaperMC/Waterfall) is a fork of BungeeCord that offers additional performance improvements and bug fixes. It's designed to provide a more stable and efficient proxy experience.

{: .warning}

> Waterfall has reached its end of life, and it is recommended to transition to Velocity instead.

{% endtab %}
{% tab proxy <i class="java-software bungeecord"></i> BungeeCord %}

[BungeeCord](https://www.spigotmc.org/wiki/bungeecord/) is one of the most widely used Minecraft proxies, enabling the linking of multiple Minecraft servers into a single network. It achieves this by allowing players to switch between servers seamlessly without disconnecting.

{% endtab %}
{% endtabs %}

## Conclusion (TLDR):

-   If you do not mind slight game-play changes in return for more performance, plugin support and more configuration, use **Paper**.
-   If you want a combination of Paper's features with even more performance, use **Pufferfish**.
-   If you want a merge of Paper's and Pufferfish's features and performance, in addition to even more configuration options, use **Purpur**.
-   For the best vanilla experience while having good performance, use **Fabric** and a few optimization mods.
-   For mods and mod-packs, use optimization mods with either **Fabric** or **NeoForge**, depending on your mod choices.
-   If you want both mods and plugins, choose either **Arclight** or **SpongeForge** based on your specific needs.
-   For proxies, use **Velocity**.
