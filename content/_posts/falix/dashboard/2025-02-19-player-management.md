---
layout: post
title: "Player Management"
tags: Players
permalink: falix/dashboard/players/player-management
description: "View online and offline players, manage your whitelist, operators, and bans."
keywords:
    - keyword: player
      matches: ["list", "view", "online", "offline", "manage"]
    - keyword: whitelist
      matches: ["add", "remove", "enable", "disable", "player"]
    - keyword: operator
      matches: ["op", "deop", "admin", "player"]
    - keyword: ban
      matches: ["player", "ip", "unban", "pardon", "reason"]
    - keyword: op
      matches: ["add", "remove", "operator", "player"]
author: Lily
---

## Introduction
Running a server is a lot of fun, but keeping it safe and enjoyable for everyone takes a bit of work. The Player Management page on your dashboard is where you handle all of that. It gives you the tools to see who is on your server, control who can join, hand out admin permissions, and deal with troublemakers -- all without ever needing to type a single in-game command.

Whether you want to run a tight-knit private server for your friend group or a larger community server open to the public, this page has you covered.

{: .info}
> Player management features are designed for **Minecraft Java** servers. Bedrock and PMMP servers have limited functionality, and Hytale servers use a different data structure with a reduced command set.

## Player List

Head over to the **Players** page from your server dashboard to see everyone who has ever connected to your server.

### Overview Cards

At the top of the page, you will find two summary cards. The **Online Players** card shows how many people are currently connected and playing right now, while the **Total Players** card shows the all-time count of every player who has ever joined your server. These are a quick way to get a snapshot of your server's activity at a glance.

Both counts auto-refresh every 60 seconds. The full player list itself refreshes every 10 minutes, but you can always click the **Refresh** button if you want an update right away.

### Player Cards

Every player appears as their own card in the list. You will see their in-game skin or avatar, their username, and a status badge showing whether they are **Online** or **Offline**. If a player has been given operator permissions, they will have an **Op** badge next to their name, and banned players are clearly marked with a **Banned** badge. Each card also shows a "last seen" timestamp so you can tell when someone was last active.

Click on any player card to open their [full player details](falix/dashboard/players/player-details) page, where you can take a closer look at their history and manage them individually.

### Searching

Looking for a specific player? Use the search box at the top of the list. You can search by username or UUID, and results will filter in real-time as you type. Autocomplete suggestions will pop up to help you find the right person faster. If you want to clear your search and go back to the full list, just click the clear button.

### Pagination

The player list displays 20 players per page. You can move between pages using the **First**, **Previous**, **Next**, and **Last** buttons, or jump directly to a specific page by entering the page number.

## Whitelist

The **Whitelist** tab is your go-to tool for controlling exactly who is allowed to join your server. When the whitelist is turned on, only the players you have specifically added to the list can connect -- everyone else will be turned away at the door.

{: .info}
> Use the whitelist if you want a private server for just your friends or a specific group. It is the simplest way to keep your server invite-only without any extra plugins or mods.

### Enabling the Whitelist

At the top of the Whitelist tab, there is a toggle switch. Flip it on to activate the whitelist, or flip it off to let anyone join again. It takes effect right away.

### Adding Players

1. Type a username into the input field. Autocomplete will suggest players who have already joined your server.
2. Click **Add** to put them on the whitelist.

### Removing Players

Click the **remove button** (the X icon) next to any whitelisted player to take them off the list. They will no longer be able to join while the whitelist is active.

The tab also shows you the total number of whitelisted players and includes a **Refresh** button to reload the list.

## Operators

The **Operators** tab is where you manage who has admin-level permissions on your server. Operators (often called "ops") can run server commands, change settings, and generally keep things running smoothly.

{: .warning}
> Be careful about who you give operator status to. Operators have a lot of power, including the ability to modify the world, kick players, and change server settings. Only promote people you trust.

### Promoting a Player

1. Type the player's username into the input field.
2. Click **Op** to grant them operator permissions.

### Demoting an Operator

If you need to remove someone's operator status, click the **Deop** button next to their name. They will go back to being a regular player.

The tab displays each operator's username along with their operator level.

## Banned Players

The **Banned Players** tab is where you deal with players who have broken your rules. Banning a player prevents them from connecting to your server using their Minecraft account.

### Banning a Player

1. Type the player's username into the input field.
2. Optionally, enter a **ban reason** to explain why they were banned.
3. Click **Ban**.

{: .info}
> Always provide a ban reason so you remember why someone was banned. Weeks or months later, when a friend asks you to unban someone, you will be glad you wrote down what happened.

Each banned player entry displays their username and ban reason (if one was provided).

### Unbanning a Player

Changed your mind, or think someone deserves a second chance? Click the **Unban** (pardon) button next to a banned player to lift the ban and allow them to join again.

## Banned IPs

The **Banned IPs** tab takes moderation a step further by banning an entire IP address rather than just a single player account.

### Understanding the Difference Between a Player Ban and an IP Ban

A **player ban** blocks one specific Minecraft account from joining your server. If the person has a second account, they could technically connect with that instead. An **IP ban**, on the other hand, blocks the network address itself, which means that any account trying to connect from that IP address will be denied. This is useful when someone keeps creating new accounts to get around a regular ban.

{: .warning}
> Keep in mind that IP bans can sometimes affect other people. If the banned player is on a shared network (like a college dorm or a household with multiple players), everyone on that network could be blocked. Use IP bans only when a regular player ban is not enough.

### Banning an IP

1. Enter the IP address in the input field.
2. Optionally, enter a **ban reason**.
3. Click **Ban IP**.

### Unbanning an IP

Click the **Unban** button next to a banned IP to remove the ban and allow connections from that address again.

Each entry shows the IP address, the ban reason, and who issued the ban, so you always have a clear record of your moderation actions.
