---
layout: post
title: "Startup Configuration"
tags: Setup
permalink: falix/dashboard/setup/startup-configuration
description: "Configure startup commands, stop commands, Docker images, Java versions, environment variables, and timezone."
keywords:
    - keyword: startup
      matches: ["command", "configure", "edit", "custom"]
    - keyword: stop command
      matches: ["custom", "change", "set", "configure"]
    - keyword: java
      matches: ["version", "change", "8", "11", "17", "21", "graalvm"]
    - keyword: environment
      matches: ["variable", "configure", "edit", "startup"]
    - keyword: timezone
      matches: ["change", "set", "server", "utc"]
    - keyword: docker
      matches: ["image", "change", "container"]
    - keyword: done message
      matches: ["startup", "ready", "detection", "change"]
author: Lily
---

## Introduction
The **Startup** and **Environment** tabs on your server's Settings page might not be the first place you visit, but they control some of the most important things about how your server actually runs. This is where you set the command that launches your server, choose which Java version it uses, configure environment variables, and more.

Getting these settings right matters. Picking the wrong Java version is one of the most common reasons a Minecraft server refuses to start. A misconfigured startup command can cause crashes before your server even loads. On the flip side, fine-tuning these settings lets you squeeze better performance out of your hardware and customize your server's behavior exactly the way you want it.

## Startup Command

{: .info}
> Editing the startup command is a **premium feature**. Free plan users can view the command but not modify it.

The startup command is the exact instruction that launches your server process. Think of it as the "ignition key" -- it tells the system what to run and with what settings.

For most users, the default command works perfectly and you won't need to touch it. But if you're a premium user and want to add custom JVM flags, tweak memory allocation, or pass specific arguments to your server software, this is where you do it.

1. Navigate to your server's **Settings** page.
2. Select the **Startup** tab.
3. Edit the command in the **Startup Command** text area.
4. Changes auto-save after you stop typing.

{: .warning}
> Be careful when editing the startup command. A typo or invalid flag can prevent your server from starting entirely. If that happens, just fix the command and try again -- your files are safe.

## Stop Command

{: .info}
> Custom stop commands are a **premium feature**.

When you click "Stop" on your server, Falix sends a stop command to gracefully shut it down. By default, this is the standard stop command for your server type, but you can customize it if your server software uses a different one.

1. On the **Startup** tab, click the **Stop Command** card.
2. Enter your custom stop command (maximum 255 characters).
3. Click **Save**.

Common stop commands include `stop`, `quit`, `exit`, and `end`. If you're not sure what your server needs, just leave this empty and the default will be used.

## Done Message

{: .info}
> Custom done messages are a **premium feature**.

The done message is how Falix knows your server has finished starting up. The system watches your console output for this specific text, and once it appears, your server is marked as "online" and ready for players.

Most of the time, the default done message works perfectly. You'd only need to change this if you're running custom server software that prints a different message when it finishes loading.

1. On the **Startup** tab, click the **Done Message** card.
2. Enter the text that appears in your console when the server is fully started (maximum 255 characters).
3. Click **Save**.

Common done messages: `Done (`, `Server is Ready!`, `Done! For help`

{: .warning}
> If the done message doesn't match what your server actually prints, Falix won't detect that the server has started. Your server will still be running, but it may show as "starting" indefinitely in the dashboard.

## Docker Image
Some server types (eggs) support multiple Docker images. If your server has this option, a Docker image dropdown will appear on the Startup tab.

1. Select a Docker image from the dropdown.
2. The change is saved automatically.

{: .info}
> This option only appears if your server's egg has multiple Docker image options configured. Most users won't see this at all and should use the Java version selector instead.

## Java Version
If you're running a Minecraft Java server, choosing the right Java version is one of the most important things you can do. Using the wrong version is the single most common cause of startup failures -- your server simply won't launch if the Java version doesn't match what your server software expects.

Not sure which version to pick? If you're running a modern Minecraft server (1.20.5 or newer), **Java 21** is your best bet. For older versions, check the table below.

1. Navigate to your server's **Settings** page.
2. Select the **Environment** tab.
3. Find the **Java Version** dropdown.
4. Select your version.
5. The change is saved automatically.

{: .warning}
> After changing the Java version, make sure to restart your server for the change to take effect. If your server fails to start after a version change, try switching back to the previous version.

### Available Versions

{% tabs java %}

{% tab java Standard %}

These are the standard HotSpot JVM versions. If you're not sure which type to pick, go with one of these.

| Version | Use Case |
|---------|----------|
| Java 8 | Legacy servers and plugins (1.12.2 and older). Only use this if you specifically need it. |
| Java 11 | Some older modded servers, particularly older Forge versions. |
| Java 16 | Minecraft 1.17 specifically. Not commonly needed anymore. |
| Java 17 | Minecraft 1.18 through 1.20.4. A solid, stable choice for these versions. |
| Java 21 | Minecraft 1.20.5 and newer. This is the recommended choice for most modern servers. |
| Java 22 | The latest Java release. Use this if you're experimenting or a specific plugin requires it. |

**Quick recommendation:** If your server is on Minecraft 1.20.5 or newer, pick Java 21. If it's between 1.18 and 1.20.4, pick Java 17. For anything older, you probably need Java 8 or 11.

{% endtab %}

{% tab java OpenJ9 %}

OpenJ9 variants use significantly less memory than standard HotSpot JVM. They're available for Java 8, 11, 16, 17, 21, and 22.

This is a great choice if your server is tight on RAM. OpenJ9 can reduce memory overhead noticeably, which means more of your allocated RAM goes toward actually running the game rather than Java itself.

The trade-off is that OpenJ9 can sometimes have slightly different performance characteristics than HotSpot, so if you run into any compatibility issues with specific plugins or mods, switch back to the standard version.

{% endtab %}

{% tab java GraalVM %}

GraalVM variants use advanced JIT (Just-In-Time) compilation to deliver better runtime performance. They're available for Java 17, 21, and 22.

If your server is CPU-bound and you want to squeeze out the best possible performance, GraalVM is worth trying. It's particularly effective for servers with many players or heavy computational loads.

Keep in mind that GraalVM uses a bit more memory than standard HotSpot, so it's best suited for servers that have RAM to spare.

{% endtab %}

{% tab java Other %}

These options are for non-Java Minecraft servers or other applications:

| Version | Use Case |
|---------|----------|
| Vanilla Bedrock | Bedrock Dedicated Server |
| PocketMineMP | PocketMine-MP (Bedrock PHP servers) |
| Other Game/Application | A multi-application image for running non-Minecraft software. **Premium only.** |

{% endtab %}

{% endtabs %}

{: .info}
> For servers with less than 1500 MB of RAM, memory settings are automatically adjusted when you change Java versions. Falix handles this for you so you don't have to worry about out-of-memory errors on smaller plans.

## Environment Variables
Environment variables let you configure your server's behavior without editing config files directly. Think of them as settings that your server software reads when it starts up. The variables you see here depend on your server type (egg), so they'll look different for a Minecraft server versus a Terraria server, for example.

1. Navigate to your server's **Settings** page.
2. Select the **Environment** tab.
3. Modify variables using the form fields.
4. Changes auto-save after you stop typing.

Variables show up as different input types -- text fields, number inputs, dropdowns, or toggles -- depending on what kind of value they expect. Some variables are read-only and can't be changed from here.

Required variables are marked with a red asterisk (*). Make sure these are filled in, or your server may not start properly.

## Timezone
By default, your server uses UTC for any time-related display. If you'd like times to match your local timezone instead, you can change that here.

1. On the **Environment** tab, find the **Timezone** dropdown.
2. Select your timezone from the list (all IANA timezones are available).
3. The change is saved automatically.

{: .info}
> The timezone setting affects how times are displayed in the server context. It won't change when scheduled tasks run if you're using cron-based tools -- those typically use their own timezone configuration.
