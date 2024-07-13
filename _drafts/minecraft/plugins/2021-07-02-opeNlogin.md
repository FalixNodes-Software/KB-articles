---
layout: help/article
title:  "Configure plugin OpeNLogin - Falix"
categories: Minecraft
icon: <i class='fa-light fa-puzzle'></i>
tags: plugins
permalink: /help/minecraft/plugins/openlogin.*
gitURL: _posts/minecraft/plugins/2021-07-02-opeNlogin.md
description: "Configure plugin OpeNLogin for your Minecraft Server at Falix"

author: Korbs
authorGitHub: korbsstudio
---

<div class="install-plugin">
    <img src="https://www.spigotmc.org/data/resource_icons/57/57272.jpg?1617128675">
    <h2>OpeNLogin</h2>
    <h3>Developer: NickUltracraft</h3>
    <a href="https://www.spigotmc.org/resources/openlogin-1-7x-1-17x.57272">Download this Plugin</a>
</div>

# What is OpeNLogin

Using this plugin will allow your players to authenticate the ownership of their account, keeping someone else from entering the server as the player.

# Installation Process

Like any other plugin, you’ll need to download the __.jar__ file of OpeNLogin, then add it to your plugins folder. Once you’ve added OpeNLogin to your plugins folder, fully restart the server, and all configuration files will be generated for OpeNLogin.

# Configuration

After you’ve joined the server for the first time after installing OpeNLogin, you’ll see a message from the plugin in the chat. The message will ask you whether you want to install nLogin or OpeNLogin. Open the chat, and click on the yellow text that says “OpeNLogin”, and confirm it by clicking on it again. The plugin will kick you out of the server so that the plugin installation can be completed. Simply join back, and you’ll now be asked to register your account. After you’ve registered your account, you will have full access to the server. Next time you enter the server, you’ll be asked to log in. To log in, use the credentials you’ve used to register your account.

![image](/assets/images/posts/plugins/openlogin/install-choice.png)

## Extra Configuration

If you would like to change some other things about the plugin, such as time to login or setting a small password size, you can do that by editing the file `config.yml` which is saved in `/plugins/OpeNLogin/`