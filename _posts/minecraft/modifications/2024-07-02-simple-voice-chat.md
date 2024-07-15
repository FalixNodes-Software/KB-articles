---
layout: post
title: Installing and configuring Simple Voice Chat
category: Modifications
tags:
    - Plugins
    - Mods
permalink: minecraft/modifications/mods/simple-voice-chat
description: Getting started with Simple Voice Chat.
author: Naoki & Deka
toc: true
---

# Explaining Simple Voice Chat
---

## What is Simple Voice Chat?

Simple Voice Chat is a mod/plugin that introduces proximity-based voice chat. It allows players to communicate with each other in-game. It also has a variety of addons that offer additional features. Simple Voice Chat requires you to have the mod installed on your client, which is only available on Minecraft: Java Edition. If you don't have it installed on your client, you can still join the server, but you can't use the voice chat features.


## Prerequisites

- Install the same version of the mod/plugin on the server and client.


# Installation
---

## Installing on Forge/Fabric

1. Download the mod from [modrinth.com](https://modrinth.com/plugin/simple-voice-chat/versions).

2. On Falix, go to `Manage` > `File Manager` and upload the downloaded .jar file into the `mods` folder.

3. Start/restart your server.


## Installing on Paper

1. Download the plugin from [modrinth.com](https://modrinth.com/plugin/simple-voice-chat/versions).

2. On Falix, go to `Manage` > `File Manager` and upload the downloaded .jar file into the `plugins` folder.

3. Start/restart your server.


# Configuration
---

{: .info}
> Please refer to [this](/falix/dashboard/server/extra-port) on how to create an extra port for your server.


## Forge/Fabric Configuration

1. Go to `Manage` > `File Manager` and open the `config` > `voicechat` folder.

2. Open `voicechat-server.properties` and change the following values:

  | Option              | Default  | Change To                         |
  | ------------------- | -------- | --------------------------------- |
  | port                | `24454`  | `<a port you have created>`       |


---
## Paper/Purpur Configuration

1. Go to `Manage` > `File Manager` and open the `plugins` > `voicechat` folder.

2. Open `voicechat-server.properties` and change the following values:

  | Option              | Default  | Change To                         |    
  | ------------------- | -------- | --------------------------------- |
  | port                | `24454`  | `<a port you have created>`       |

{: .info}
> Make sure to restart the server after changing the `port` value to apply the changes.