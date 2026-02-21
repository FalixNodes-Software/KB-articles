---
layout: post
title: "Storage Mode"
tags: Server
permalink: falix/dashboard/server/storage-mode
description: "What storage mode is, why your server was moved there, and how to bring it back."
keywords:
    - keyword: storage
      matches: ["mode", "inactive", "inactivity", "offloaded", "moved"]
    - keyword: inactive
      matches: ["storage", "offloaded", "moved", "server"]
    - keyword: transfer
      matches: ["storage", "node", "moving", "back"]
author: Lily
---

## Introduction
If you haven't logged into the dashboard for a while, you might come back to find your server in storage mode. This means your server has been moved to a dedicated storage node to free up resources for active players. You'll need to bring the server out of storage before you can use it again.

## Why It Happens
Free-plan servers are automatically moved to storage after 6 hours of inactivity. Inactivity is measured by how long it's been since you last logged into the dashboard -- not by player count or server uptime. This keeps free nodes available for people who are actively using them.

{: .info}
> Premium servers are never moved to storage, regardless of how long you've been away.

## What You Can't Do in Storage Mode
While your server is on the storage node, most features are unavailable:

- **File Manager** -- you can't browse, upload, or edit files.
- **Backups** -- you can't create new backups or transfer existing ones to the server.
- **Console** -- you can't send commands or interact with the server.

The dashboard will show a storage mode warning letting you know the server needs to be started before you can access anything.

## Getting Out of Storage Mode
Bringing your server back is straightforward:

1. Navigate to your server's **Console** page.
2. Click **Start**{: .blue }.
3. Your server will be transferred from the storage node to a runtime node. You'll see a transfer alert with a countdown timer while this happens.
4. Once the transfer completes, your server starts up and everything is back to normal.

If the transfer is taking longer than expected, it's likely because the free nodes are overloaded. During busy periods there may not be a runtime node with enough resources available right away. The system will keep trying -- just give it some time, or consider upgrading to premium for faster transfers and no storage mode in the first place.

{: .info}
> The transfer can take a moment depending on how much data your server has. Console interaction is blocked during the transfer -- just wait for it to finish.

## Free vs Premium

| Feature | Free | Premium |
|---------|------|---------|
| Moved to storage after inactivity | After 6 hours | Never |
| Recovery method | Start from console | N/A |
