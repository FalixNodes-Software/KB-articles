---
layout: post
title: "Crash Detection & Auto-Restart"
tags: Monitoring
permalink: falix/dashboard/monitoring/crash-detection
description: "Configure restart policies, rate limiting, health monitoring, and OOM handling for your server."
keywords:
    - keyword: crash
      matches: ["detection", "restart", "auto", "policy"]
    - keyword: restart
      matches: ["auto", "crash", "policy", "health"]
    - keyword: health
      matches: ["check", "monitor", "server", "status"]
    - keyword: oom
      matches: ["memory", "out", "kill", "policy"]
author: Lily
---

## Introduction
Servers crash -- it happens. Maybe your Minecraft world ran out of memory during a big TNT explosion, or a plugin update went sideways. The real question isn't whether your server will ever crash, but how quickly and gracefully it recovers when it does. That's exactly what crash detection is for. These settings let you control automatic restart behavior, prevent runaway restart loops, and set up health checks that keep an eye on your server so you don't have to.

{: .info}
> Crash detection is a **premium feature**. Free plan users will need to upgrade to use it.

## Restart Settings

To get started, navigate to your server's **Settings** page, select the **Crash Detection** tab, and click the **Restart Settings** card.

### Restart Policy

Your restart policy tells the system what to do when your server goes down. Here are the available options:

| Policy | Description |
|--------|-------------|
| **Default (on-failure)** | Restart only when the server exits with an error. This is selected when you leave the dropdown on its default value. |
| **Never restart** | Never auto-restart regardless of exit status |
| **Always restart** | Always restart after any shutdown |
| **Restart on failure** | Restart only on non-zero exit code |
| **Restart on abnormal exit** | Restart on abnormal exits (signals, timeouts) |
| **Unless manually stopped** | Restart unless you manually stopped the server yourself |

{: .info}
> Most servers should stick with the default **on-failure** policy. It restarts your server when something actually goes wrong, but won't interfere when you shut it down intentionally. If you're running a production server that needs maximum uptime, **unless manually stopped** is a solid alternative -- it keeps the server running through almost anything, unless you explicitly stop it yourself.

### Rate Limiting

If your server keeps crash-looping (crashing, restarting, crashing again), rate limiting prevents it from burning through resources by capping how many restarts can happen in a given time window.

| Setting | Range | Default |
|---------|-------|---------|
| **Max restarts** | 1--20 | 5 |
| **Interval** | 10--3,600 seconds | 60 seconds |

Toggle **Rate Limiting** on to activate it. Once the restart limit is reached, the server stays stopped until the interval resets. This gives you time to investigate what's going wrong instead of letting the server spin its wheels endlessly.

{: .warning}
> If your server hits the rate limit repeatedly, that's a sign something deeper is wrong -- check your logs, recent plugin or mod changes, or memory allocation before restarting again.

### Timeouts

Timeouts control how patient the system is when waiting for your server to start up or shut down.

| Setting | Range | Default | Description |
|---------|-------|---------|-------------|
| **Start Timeout** | 10--600 seconds | 90 seconds | How long to wait for the server to start before considering it failed |
| **Stop Timeout** | 10--1,800 seconds | 600 seconds | How long to wait for the server to stop gracefully before force killing |

The defaults work well for most setups. If you have a heavily modded server that takes a while to load, you may want to increase the start timeout so the system doesn't mistakenly think it crashed during a slow boot. Similarly, if your server needs extra time to save world data on shutdown, bumping the stop timeout can prevent data loss.

### OOM Policy

Sometimes your server simply runs out of memory. The OOM (Out of Memory) policy determines what happens next:

- **Default (stop)** -- Stops the server cleanly and lets crash detection handle the restart. This is the safest choice for most users since it gives the system a chance to recover properly.
- **Continue** -- Keeps the server running and lets Docker handle the OOM event. This can be unpredictable, so only use it if you know what you're doing.
- **Kill** -- Immediately kills the server process. Fast, but not graceful -- use this if you'd rather cut things off quickly than risk a hung process.

## Health Monitoring

Health monitoring goes beyond crash detection by actively checking whether your server is actually working, not just running. You'll find it on the **Health Monitoring** card under the Crash Detection tab.

### Enabling Health Checks

Flip the **Enable Health Monitoring** toggle to turn it on. Once enabled, the system periodically checks if your server is responsive and can take action automatically if something seems off.

### Check Types

Different check types work better for different situations. Pick the one that makes sense for your server:

| Type | What It Checks |
|------|---------------|
| **Process** | Whether the server process is running |
| **TCP** | Whether a port is accepting connections |
| **HTTP** | Whether an HTTP endpoint responds |
| **Minecraft** | Pings the Minecraft server protocol (Java or Bedrock) |

For **TCP**, **HTTP**, and **Minecraft** checks, you'll need to specify a **port** (1--65535).

For **Minecraft** checks, you also select the **edition** (Java or Bedrock), which determines the default port (25565 for Java, 19132 for Bedrock).

{: .info}
> The **Minecraft** health check type is the most reliable option for game servers. Unlike a simple process or TCP check, it actually speaks the Minecraft protocol -- so it can tell the difference between a server that's technically running and one that's actually accepting players.

### On Failure Action

When a health check fails, the system needs to know how you want to respond. You have three choices:

- **Notify** -- Sends you an alert but doesn't take any automatic action. Good if you want to stay informed but prefer to handle issues manually.
- **Restart** -- Automatically restarts the server. This is the most hands-off option and works well when paired with rate limiting to prevent restart loops.
- **Stop** -- Stops the server entirely. Useful if you'd rather keep things offline until you can look into the problem yourself.

### Status Display

The Health Monitoring card gives you a live overview so you can see what's happening at a glance. It shows the **current health status** of your server, **when the last check ran**, the **number of consecutive failures** (so you can spot patterns), and whether **monitoring is enabled or disabled**. If you're troubleshooting an issue, this is a great place to start.
