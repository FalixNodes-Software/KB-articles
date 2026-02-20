---
layout: post
title: "How To Switch Applications"
tags: Setup
permalink: falix/dashboard/setup/switch-application
description: "Change your server's game or application type."
keywords:
    - keyword: switch
      matches: ["application", "game", "change", "server"]
    - keyword: application
      matches: ["switch", "change", "game", "type"]
    - keyword: game
      matches: ["change", "switch", "application", "type"]
author: Lily
---

## Introduction
One of the best things about having a Falix server is that you are not locked into a single game or application forever. Maybe you started with a Minecraft Java server to play survival with friends, but now you want to try out Minecraft Bedrock so everyone on console can join too. Or maybe your Minecraft world has wound down and you would rather repurpose that server slot for a Discord bot, a Terraria world, or a web application. Whatever the reason, Falix lets you switch your server's application at any time without needing to delete anything and start over.

Switching applications changes the underlying **server egg**, which is the template that controls how your server starts up, what software it runs, and what configuration options are available to you. Think of it like swapping the engine in a car — the chassis (your server slot, your files on disk) stays the same, but the way the server actually runs changes completely.

## When Should You Switch?
Here are some common scenarios where switching applications makes sense:

- **Trying a different edition of Minecraft** — You have been running a Java Edition server but want to switch to Bedrock so friends on mobile or console can join.
- **Moving to a different game entirely** — Your group is done with Minecraft for now and wants to spin up a Terraria or Hytale server instead.
- **Repurposing a server slot** — You have a free or premium server slot that you would rather use for a Discord bot, a web server, or another custom application.
- **Testing something new** — You just want to experiment with a different application to see how it works before committing to it long-term.

## Before You Switch: Back Up Your Files

{: .warning}
> Switching applications changes how your server starts and what software it runs. Your existing files will stay on disk, but they almost certainly will not be compatible with the new application. A Minecraft world file means nothing to a Terraria server, for example. **Always create a backup before switching** so you can restore your data if you ever want to go back.

If you are not sure how to create a backup, check out the [Server Backups](/falix/dashboard/files/backups) article. It only takes a moment and can save you a lot of headache later.

## How to Switch Applications

1. Navigate to your server's **Settings** page.
2. Select the **Operations** tab.
3. Click the **Switch Application** card.
4. Browse the available applications by category (see below).
5. Select the application you want to switch to.
6. Click **Switch Application**.

That is all there is to it. Your server's egg will be updated, which means its startup command, Docker image, and available configuration options will all change to match the new application.

## What Happens Behind the Scenes

When you confirm the switch, a few things happen on the backend:

- **The server egg is replaced.** The egg defines the startup script, the Docker image your server runs inside, and the configuration variables available on your Settings page. All of these are swapped out for the new application's versions.
- **Your files remain on disk.** Falix does not automatically delete your existing files when you switch. They will still be sitting in your File Manager afterward. However, the new application will likely ignore them entirely since they belong to a different piece of software.
- **The server may need to be reinstalled.** Depending on the application, the new egg's installation script may need to run in order to download the correct server software. If prompted, follow the on-screen instructions.
- **Some settings are preserved automatically.** Your timezone and memory configuration carry over to the new application, so you do not need to reconfigure those after switching.

{: .info}
> If you switch back to your original application later, your old files should still be there (assuming you have not deleted them). This means you can often pick up right where you left off, though it is always safest to restore from a backup rather than relying on leftover files.

## Available Application Categories

Applications are organized into categories to make browsing easier:

- **Games** — This is where you will find all the game servers Falix supports, including Minecraft Java Edition, Minecraft Bedrock Edition, Terraria, Hytale, and more. If you are here to run a game server, this is the category to look through.
- **Apps** — This category covers everything that is not a game. Web servers, Discord bots, custom applications, and other software all live here. If you want to repurpose your server slot for something outside of gaming, check this section out.

{: .info}
> Free plan users can only switch between Minecraft Java and Hytale. All other applications require a premium plan.

## Tips and Things to Keep in Mind

- **You can switch as many times as you like.** There is no limit on how often you change your server's application. Feel free to experiment. The only restriction is that you cannot switch to the application your server is already running.
- **Switching does not affect your server slot or plan.** Your server keeps the same resources (RAM, disk space, etc.) regardless of which application is running.
- **Old files can pile up.** Since switching does not delete files, you might end up with leftover data from previous applications cluttering your File Manager. It is a good idea to clean up files you no longer need after a switch.
- **Check your startup configuration after switching.** The new application will have different startup variables and settings. Head over to your server's **Startup Configuration** page after switching to make sure everything looks right.
- **If something goes wrong, you can always switch back.** Restore your backup and switch the application back to what it was before. You will be right back where you started.
