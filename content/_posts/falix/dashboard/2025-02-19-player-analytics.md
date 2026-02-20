---
layout: post
title: "Player Analytics"
tags: Server
permalink: falix/dashboard/general/player-analytics
description: "Track player activity, retention, peak hours, and session data for your Minecraft server."
keywords:
    - keyword: player analytics
      matches: ["activity", "stats", "track", "monitor"]
    - keyword: player count
      matches: ["online", "peak", "average", "track"]
    - keyword: retention
      matches: ["player", "returning", "funnel", "rate"]
    - keyword: peak hours
      matches: ["player", "activity", "busy", "time"]
    - keyword: leaderboard
      matches: ["player", "top", "playtime", "sessions"]
author: Lily
---

## Introduction
Running a Minecraft server is about more than just keeping it online -- it's about building a community. The Player Activity tab on the Monitor page gives you the data you need to truly understand your players: who's showing up, when they're most active, whether they stick around, and how your server is growing over time.

Why does any of that matter? Because good analytics help you make better decisions. You can figure out the best times to host events by looking at peak hours, spot retention problems early if new players aren't coming back, and track your growth week over week to see if your community-building efforts are paying off.

{: .info}
> Player analytics is only available for **Minecraft** servers. The tab does not appear for other server types.

## Overview

At the top of the page, you'll see a live summary that gives you a quick snapshot of how your server is doing right now and over your selected time range:

- **Current Online** -- The number of players connected to your server at this very moment.
- **Peak Players** -- The highest player count recorded during the selected time range. Great for knowing your all-time busy moments.
- **Average Players** -- The average number of players online over the period, which gives you a more realistic sense of typical activity than the peak alone.
- **Unique Players** -- The total number of distinct players who joined. This tells you how many different people are checking out your server.
- **New Players** -- Players who joined for the very first time. Keep an eye on this one -- it's your growth indicator.

### Insight Cards

Just below the overview, four compact cards give you deeper context at a glance:

- **Growth Rate** -- Your week-over-week player growth as a percentage, complete with a trend indicator so you can see whether things are heading up or down.
- **Retention Rate** -- The percentage of players who come back after their first visit. This is one of the most important numbers on the page -- if people aren't returning, something about the first experience might need work.
- **Avg Session** -- How long players spend on your server per session on average. Longer sessions generally mean players are engaged and having fun.
- **Top Region** -- The most common player region, inferred from activity times. Handy for figuring out which time zones your community lives in.

## Time Ranges

You can adjust the time range to control what all the charts and data on the page reflect. Just pick the one that fits what you're looking for:

| Range | Available |
|-------|-----------|
| 1 hour | Yes |
| 6 hours | Yes |
| 24 hours (default) | Yes |
| 3 days | Yes |
| 7 days | Yes |
| 30 days | Yes |

## Player Count Timeline

This area chart shows how your player count fluctuates over the selected time range. Hover over any point on the chart to see the exact count at that moment. It's a great way to visually spot trends -- maybe your server is busier on weekends, or maybe there's a dip during certain hours.

## Peak Hours

The peak hours bar chart breaks down the average number of players for each hour of the day (0 through 23). This is one of the most actionable charts on the page because it tells you exactly when your server is busiest.

{: .info}
> Use your peak hours data to schedule server events when the most players are on. Hosting a build competition or PvP tournament during off-peak hours means fewer people will show up.

## Activity Heatmap

The activity heatmap takes things a step further by showing activity intensity across both the day of the week and the hour of the day in a 2D grid. Brighter colors mean more players. This is perfect for spotting weekly patterns -- for example, you might notice that weekend evenings light up while weekday mornings are quiet. Use this to plan your week around when your community is actually playing.

## Retention Funnel

The retention funnel is a horizontal flow that shows how well you hold onto new players over time. This is where you find out if people are sticking around or bouncing after their first visit:

| Stage | Description |
|-------|-------------|
| **New Players** | Total new players in the period |
| **D1 Retention** | Percentage who returned within 1 day |
| **D7 Retention** | Percentage who returned within 7 days |
| **D30 Retention** | Percentage who returned within 30 days |

Each stage displays both the percentage and the actual count (for example, "45% (52/115)"), so you get the full picture.

{: .warning}
> If your D1 retention is low, that's a sign new players aren't having a great first experience. Consider improving your spawn area, adding a tutorial or welcome system, or making sure new players aren't immediately overwhelmed. First impressions matter a lot.

## Player Leaderboard

The player leaderboard is a ranked list of your top players sorted by total playtime. For each player, you'll see:

- **Rank** -- Their position on the leaderboard.
- **Player Name** -- Their Minecraft username, which you can click to see more details.
- **Play Time** -- The total time they've spent on your server.
- **Join Count** -- How many separate sessions they've logged.
- **Last Seen** -- When they were last online, shown as relative time (like "2 hours ago").

Use the **search bar** at the top of the leaderboard to quickly look up a specific player by name. This is a great way to check on regulars or investigate a specific player's activity.

## Live Activity Feed

At the bottom of the page, you'll find a real-time feed of player events marked with a blinking **Live** indicator. Events that show up here include:

- Player joins
- Player leaves
- Achievements
- Deaths

Each event shows the player's name and a timestamp. The feed displays the 100 most recent events and auto-scrolls to keep the latest activity in view, so you can keep an eye on what's happening without refreshing.
