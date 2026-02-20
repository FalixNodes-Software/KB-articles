---
layout: post
title: "Server Monitoring"
tags: Monitoring
permalink: falix/dashboard/monitoring/server-monitoring
description: "Monitor your server's performance with real-time charts, health scores, crash reports, predictive alerts, and player activity tracking."
keywords:
    - keyword: monitor
      matches: ["performance", "cpu", "ram", "disk", "network"]
    - keyword: health
      matches: ["score", "server", "grade", "monitor"]
    - keyword: crash
      matches: ["report", "log", "oom", "restart"]
    - keyword: cpu
      matches: ["usage", "monitor", "performance", "chart"]
    - keyword: memory
      matches: ["ram", "usage", "monitor", "performance"]
    - keyword: uptime
      matches: ["monitor", "server", "session", "restart"]
    - keyword: player activity
      matches: ["online", "retention", "leaderboard", "peak"]
author: Lily
---

## Introduction
Server problems rarely show up out of nowhere. Usually, there are warning signs -- CPU creeping up, memory slowly filling, restarts happening more often than they should. The Monitor page helps you spot those patterns before they turn into real issues.

From here, you can track your server's resource usage in real time, see a health score that summarizes how things have been going over the past week, dig into crash reports when something does go wrong, and -- if you're running a Minecraft server -- keep tabs on player activity and retention. Think of it as your server's dashboard for understanding what's happening under the hood.

## Health Score

{: .info}
> The health score is a **premium feature**.

Your health score is a quick way to know how your server has been doing lately. It looks at the past 7 days and gives you a rating from 0 to 100, along with a letter grade from A+ down to F.

A high score means your server is running smoothly with low resource usage and few (or no) crashes. A low score is a signal that something needs attention -- maybe memory is consistently too high, or the server has been restarting more than it should.

### Score Breakdown

The score is a weighted average of five metrics, so some things matter more than others:

| Metric | Weight | What It Measures |
|--------|--------|-----------------|
| **CPU** | 20% | Average CPU usage -- starts degrading above 50% |
| **Memory** | 25% | Average RAM usage -- starts degrading above 60% |
| **Crashes** | 20% | Crash frequency -- each crash per day brings the score down |
| **Uptime** | 20% | Session duration and how often restarts happen |
| **Players** | 15% | Player retention rate (Minecraft servers only) |

Memory carries the most weight because running out of RAM is one of the most common causes of crashes and poor performance.

### What the Grades Mean

- **Green (90--100, grades A+ through A-)** -- Your server is in great shape. Keep doing what you're doing.
- **Orange (60--89, grades B+ through D-)** -- Things are okay, but there's room for improvement. Worth checking which metric is dragging the score down.
- **Red (0--59, grade F)** -- Your server needs attention. Check the crash reports and resource charts to figure out what's going wrong.

You'll also see a trend indicator that tells you whether your score has gone up or down compared to last week, so you can tell at a glance if things are getting better or worse.

{: .success}
> If your health score is dropping, the crash reports section (further down the page) is usually the best place to start investigating.

## Performance Charts

The main chart shows your server's resource usage over time and auto-refreshes every 2 minutes, so you can keep it open and watch things in near real-time.

### Metrics

Use the tabs below the chart controls to switch between different metrics:

- **CPU (%)** -- How much processor power your server is using.
- **Memory (GB)** -- RAM usage, with a percentage overlay so you can see how close you are to your limit.
- **Disk (GB)** -- How much storage space your server is taking up.
- **Network (MB/s)** -- Incoming (RX) and outgoing (TX) traffic, useful for spotting unusual activity.
- **Uptime (Online/Offline)** -- A stepped chart showing when your server was running and when it wasn't.

### Time Ranges

You can zoom in or out on different time windows. Shorter ranges give you more granular data, while longer ranges help you spot trends over days.

| Range | Data Interval |
|-------|--------------|
| 15 minutes | 30-second intervals |
| 1 hour | 1-minute intervals |
| 6 hours | 2-minute intervals |
| 24 hours (default) | 5-minute intervals |
| 3 days | 15-minute intervals |
| 7 days | 30-minute intervals |

### View Modes

{% tabs viewmode %}

{% tab viewmode Single %}

This is the default view. It shows one metric at a time, and you switch between them using the tabs. Great for focusing on a specific resource.

{% endtab %}

{% tab viewmode Combined %}

Combined mode overlays multiple metrics on the same chart, which is really helpful when you want to see how different resources relate to each other. For example, you might notice that CPU spikes whenever memory is nearly full.

When combined mode is enabled, checkboxes appear so you can toggle individual metrics on and off:

- CPU Usage (%)
- Memory Usage (GB)
- Disk Usage (GB)
- Network Total (MB/s)

{% endtab %}

{% endtabs %}

### Uptime Statistics

When you select the **Uptime** tab, four stat cards appear above the chart to give you a quick summary:

- **Current Session** -- How long the server has been running since it last started.
- **Uptime Percentage** -- The percentage of time your server has been online during the selected time range. Anything below 95% is worth looking into.
- **Total Restarts** -- How many times the server restarted in the selected range. A high number here could point to crash loops or configuration issues.
- **Longest Session** -- The longest continuous stretch your server has been running. If this is much shorter than expected, something may be causing periodic crashes.

## Predictive Alerts

This is one of the most useful features on the monitoring page. The system watches your CPU and memory trends and uses that data to predict when you might hit resource limits. If things are trending toward 80--90% usage, a tip banner appears at the top of the page letting you know before it becomes a problem.

{: .success}
> Predictive alerts can save you from surprise outages. If you see one, it's a good time to check whether you need to optimize your server, reduce plugins, or upgrade your plan.

## Player Activity (Minecraft Only)

If you're running a Minecraft server, you'll see a second tab at the top of the Monitor page called **Player Activity**. This tab gives you a detailed look at who's playing on your server, when they're playing, and how well you're retaining them over time.

### Overview Cards

At the top, a hero card shows the number of **players currently online**, along with quick stats for **peak** players, **average** online count, **unique** players, and **new** players for the selected time range.

Below that, four insight cards give you a snapshot of your server's community health:

- **Growth Rate** -- How your player count is trending compared to the previous period.
- **Retention Rate** -- The percentage of players who come back after their first visit.
- **Avg Session** -- How long players typically stay on your server per session.
- **Top Region** -- The most common geographic region your players connect from.

### Charts and Visualizations

The Player Activity tab includes several charts to help you understand player behavior:

- **Player Count Timeline** -- A line chart showing how many players were online over time, so you can spot trends and peak periods.
- **Peak Hours** -- A bar chart showing which hours of the day are busiest, helping you plan restarts or events around your server's most active times.
- **Activity Heatmap** -- A visual grid showing player activity patterns across days and hours, making it easy to see at a glance when your server is most and least active.

### Retention Funnel

The retention funnel tracks how well your server keeps players coming back. It shows the flow from **New Players** to **Day 1** retention, then **Day 7**, and finally **Day 30** retention, with percentages and player counts at each stage. If you notice a big drop-off at a particular stage, that's a signal to investigate what might be driving players away.

### Player Leaderboard and Activity Feed

On the lower half of the tab, you'll find two panels side by side:

- **Player Leaderboard** -- Ranks your most active players by playtime, with a search bar so you can look up specific players.
- **Activity Feed** -- A live feed of player events like joins and leaves, so you can see who's coming and going in real time.

### Time Ranges

You can adjust the time range for player activity data using the dropdown. Available ranges are 1 hour, 6 hours, 24 hours (the default), 3 days, 7 days, and 30 days.

## Crash Reports

When your server does crash, this section keeps a detailed history so you can understand what happened and how often it's occurring.

### Filters

You can narrow down the crash list by type and time range:

- **Type** -- Show all events, crashes only, or clean exits only.
- **Time Range** -- Choose from the last 24 hours, 3 days, 7 days (the default), or 30 days.

### Summary Cards

When crashes exist in the selected range, you'll see four summary cards at the top:

- **Total Crashes** -- The total number of crashes in the time range you selected.
- **Last 24h** -- How many crashes happened just in the past day. If this number is high, something is actively wrong.
- **OOM Kills** -- Out-of-memory kills specifically. These happen when your server runs out of RAM and the system forcibly shuts it down.
- **Avg Uptime** -- The average time between crashes. Short averages mean frequent crashes.

### Crash Details

Each crash entry in the list shows you:

- **Timestamp** with a relative label (like "3 hours ago") so you can quickly gauge how recent it was.
- **Type badge** -- Color-coded so you can tell at a glance what kind of event it was. OOM Kill shows in red, Clean Exit in green, and Error Exit in orange.
- **Status** -- Whether the server was automatically restarted after the crash.
- **Exit code** -- The process exit code, which can help with debugging.
- **Resource usage** at the time of the crash -- uptime, memory, and CPU levels when things went wrong.

### Viewing Crash Logs

Click **View Logs** on any crash entry to see the console output from around the time of the crash. This is often the fastest way to figure out exactly what went wrong.

The log viewer includes:

- Syntax highlighting for timestamps, log levels, and error messages so important lines stand out.
- ANSI color code rendering for properly formatted output.
- Line numbers for easy reference.
- An option to download the full log as a `.txt` file if you want to share it or analyze it elsewhere.

{: .info}
> If your server has no crashes to report, you'll see a confirmation message that everything is running smoothly. That's always nice to see.
