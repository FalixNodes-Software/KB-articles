---
layout: help/article
title:  "Troubleshooting and Errors about your Minecraft Server - Falix"
categories: Falix
tags: support
icon: <i class='fa-light fa-question'></i>
permalink: /help/falix/support/troubleshooting.*
gitURL: _posts/falix/support/2023-02-10-troubleshooting.md
redirect_from:
  - /falix/general/troubleshooting/
description: "How to troubleshoot and figure out errors related to your Minecraft Server at Falix"

author: Korbs
authorGitHub: korbsstudio
---

# Troubleshooting
## Corrupted Bungeecord JAR File
Delete the <u>bungeecord.jar</u> and <u>bungeecord.server</u> file in your file manager, then upload the <u>BungeeCord.jar</u> file from the official [Jenkins](https://ci.md-5.net/job/BungeeCord/) build and rename it to <u>custom.jar</u>. Then try booting your server again.

## BungeeCord IP Forwarding
Error Message: If you wish to use IP forwarding, please enable it in your BungeeCord config as well!
If this error appears when attempting to connect to your BungeeCord server, you should then edit the configuration file in your proxy server.

Edit the <u>config.yml</u> file, make sure that **ip_forward** is set to **true**.

Simply restart the proxy server upon saving the configuration.

# Errors
## Error 137
This error indicates that your server is using too much CPU to the point of overloading. The server automatically turns off to prevent overload of the whole node.

## Server Creation Error
There are a vast array of reasons why you may be unable to create a new server.

### Resource Limitation
You may not have enough resources left to create a server which may be caused by the limit of RAM, CPU cores, server slots, etc.

### Node is at Full Compacity
The node for the location you've preferred might have been full.

### Server Creation is Disabled
For the time being, we may have disabled server creation. Simply refer to our [Discord](https://discord.gg/FalixNodes) announcements channel.

## Connection Issue
Every now and then you may see an error that says "We're having some trouble connecting to your server, please wait...".
You'll have to keep refreshing the page or wait until the connection is established.

## User Limit of Inotify Istances Reached or to Many Files
This is an error that you will receive when we have too many servers online on a node. Unfortunately, we are unable to fix this issue. Please wait 20-30 minutes, then try again.
