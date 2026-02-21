---
layout: post
title: "Server Timer"
tags: Server
permalink: falix/dashboard/server/timer
description: "Understand the server timer on free nodes and how to renew it to keep your server online."
keywords:
    - keyword: timer
      matches: ["renew", "extend", "countdown", "expire", "expiration"]
    - keyword: renew
      matches: ["timer", "extend", "time", "add"]
    - keyword: free
      matches: ["timer", "node", "limit", "auto-stop"]
author: Lily
---

## Introduction
Some servers on free nodes come with a countdown timer. When it reaches zero, your server automatically shuts down. It's how free nodes stay available for everyone -- but all you have to do is renew the timer every now and then and your server keeps running without interruption. Not every server has one, though. Whether your server uses a timer depends on its game type. Premium servers never have a timer at all.

## How the Timer Works
If your server has a timer, it starts counting down as soon as the server comes online. The timer page shows a live countdown in hours, minutes, and seconds so you always know exactly how much time you have left.

When the countdown hits zero, your server stops automatically. No data is lost -- your files are still there and you can start it back up whenever you want -- but any players online will be disconnected.

{: .info}
> Premium servers don't have a timer. If your server is on a premium node, none of this applies to you.

## Renewing Your Timer
There's no link to the timer page in the dashboard sidebar. Instead, you'll get clickable messages in your server's in-game chat when time is running low. Click the link in one of those messages to open the timer page, then:

1. Complete the **CAPTCHA** verification.
2. Click **Add Time**{: .blue }.

Each renewal extends your timer, up to a maximum of 1 hour. You can renew as many times as you need to -- there's no daily limit.

{: .info}
> Don't wait until the last minute. Renew when your timer drops below 20 minutes so you have a comfortable buffer.

### Opening the Timer Page Manually
If you missed the in-game warning or want to renew from outside the game, you can build the URL yourself:

```
https://client.falixnodes.net/timer?id=YOUR_SERVER_ID
```

Replace `YOUR_SERVER_ID` with your server's ID. You can find it in the **Support Info** section of your server's console page sidebar.

## In-Game Warnings
Your server sends chat warnings as the timer gets low, so you don't have to keep checking manually:

| Time Remaining | What Happens |
|----------------|--------------|
| 10 minutes | First warning with a clickable link to the timer page |
| 5 minutes | Second warning with the same link |
| 0 minutes | Server shuts down automatically |

The warnings show up as clickable messages in your server's chat. Clicking the link takes you straight to the timer renewal page for that server.

{: .warning}
> Once the timer hits zero, the server stops immediately. Make sure to renew before then if you want to stay online.

## Free vs Premium

| Feature | Free | Premium |
|---------|------|---------|
| Timer required | Some servers | No |
| Auto-stop on expiry | Yes | N/A |
| In-game warnings | Yes | N/A |
| Renewal via CAPTCHA | Yes | N/A |
