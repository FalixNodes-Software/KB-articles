---
layout: help/article
title:  "Adding a Minecraft Server Resource Pack - Falix"
categories: Minecraft
icon: <i class="fa-light fa-sword"></i>
tags: mcgeneral
permalink: /help/minecraft/general/adding-a-server-resource-pack.*
gitURL: _posts/minecraft/general/2021-11-24-adding-server-resource-pack.md
description: "Setup your own resource pack for your Minecraft Server at Falix"

author: Korbs
authorGitHub: korbsstudio
---

## What is a resource pack and why use it on my server?

A resource pack enables you and other players to customize and change the appearance of the game by customizing and changing textures, sound, fonts, and much more without altering the game code directly. This could be used on your Minecraft server to showcase the genuine beauty of your server.

## Adding a Resource Pack

To add a resource pack to your server, you have to provide a 'direct' link to the resource pack as a ZIP file, which is generally a download link from the author's website.

You'll add this link next to the `resource-pack=` property in the <u>server.properties</u> file.

## Options

Other options are available for the resource packs property, which can also be accessed in the <u>server.properties</u> file.

| Property                    | Description              |
|:----------------------------|:-------------------------|
| resource-pack-prompt        | Optional, adds a custom message to be shown on resource pack prompt when `require-resource-pack` is used. Expects chat component syntax, can contain multiple lines. |
| resource-pack-sha1          | Optional SHA-1 digest of the resource pack, in lowercase hexadecimal. It is recommended to specify this, because it is used to verify the integrity of the resource pack. Note: If the resource pack is any different, a yellow message "Invalid sha1 for resource-pack-sha1" appears in the console when the server starts. Due to the nature of hash functions, errors have a tiny probability of occurring, so this consequence has no effect. |
| require-resource-pack       | When this option is enabled (set to true), players will be prompted for a response and will be disconnected if they decline the required pack. |
