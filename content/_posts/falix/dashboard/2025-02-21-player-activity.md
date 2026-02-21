---
layout: post
title: "Player Activity"
tags: Server
permalink: falix/dashboard/server/player-activity
description: "How inactive servers are automatically stopped and how to configure auto-stop behavior."
keywords:
    - keyword: activity
      matches: ["player", "inactive", "idle", "empty", "auto-stop"]
    - keyword: auto-stop
      matches: ["inactive", "empty", "idle", "shutdown", "automatic"]
    - keyword: inactive
      matches: ["server", "stop", "shutdown", "empty", "players"]
author: Lily
---

## Introduction
Free-node servers are monitored for player activity. If your server sits empty with no players connected for too long, it shuts down automatically to free up resources for others. This happens quietly in the background -- there's no in-game warning or notification. Premium servers are not affected by this and will stay online regardless of player count.

## How It Works
The system regularly checks how many players are connected to your server. When the count drops to zero, a 10-minute grace period begins. If a player joins during that window, the countdown resets and your server keeps running like nothing happened. If nobody joins within those 10 minutes, the server stops automatically.

{: .info}
> This is separate from the [server timer](/falix/dashboard/server/timer). The timer is a manual countdown you renew yourself. Player activity monitoring is fully automatic and based on whether anyone is online.

## What Happens After Your Server Stops
When the grace period expires and your server shuts down, it goes back to an offline state in the dashboard. To get back online, just head to your server's console page and start it up again.

If you're not around to restart it yourself, your players can use the [external start page](https://falixnodes.net/startserver) to bring the server back online without needing access to your dashboard. All they need is your server's subdomain. Check out the [external start guide](/falix/dashboard/automation/external-start) for setup instructions.

## Keeping Your Server Running
The simplest way to avoid auto-stop is to have at least one player connected. As long as someone is online, the grace period never starts. Beyond that, upgrading to a premium plan removes player activity monitoring entirely -- your server stays online no matter what.

{: .warning}
> Do not attempt to bypass the activity system with fake players, bots, or any other method. This violates the [acceptable use policy](https://falixnodes.net/acceptable-use-policy) and can result in your server or account being suspended. Examples of prohibited behavior include connecting bots or AFK accounts to keep the player count above zero, and using plugins or mods designed to spoof player activity.

## Free vs Premium

| Feature | Free | Premium |
|---------|------|---------|
| Player activity monitoring | Yes | No |
| Auto-stop when empty | After 10 minutes | Never |
