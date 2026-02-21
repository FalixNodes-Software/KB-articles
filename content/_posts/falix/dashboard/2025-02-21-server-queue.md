---
layout: post
title: "Server Queue"
tags: Server
permalink: falix/dashboard/server/queue
description: "What the startup queue is and how to get your server started when the node is at capacity."
keywords:
    - keyword: queue
      matches: ["startup", "waiting", "line", "capacity", "skip"]
    - keyword: waiting
      matches: ["queue", "start", "line", "node"]
author: Lily
---

## Introduction
Sometimes when you click **Start**, your server doesn't boot up right away. Instead, you'll see a queue alert letting you know the node is at capacity and your server is waiting in line. This is completely normal during busy periods -- it just means the node needs to free up some resources before your server can start.

## How the Queue Works
Once your server enters the queue, the system automatically retries starting it every 60 seconds. It'll keep trying for up to 30 attempts, so you don't need to sit there clicking Start over and over. Just leave the page open and let it do its thing.

{: .info}
> You don't need to keep clicking Start. The system handles retries automatically -- just wait for your turn.

## Skipping the Queue
If you'd rather not wait, there are two ways to jump ahead:

- **Premium plan** -- premium servers skip the queue entirely. Every time you click Start, your server boots immediately regardless of how busy the node is.
- **Watch an ad** -- on the free plan, a **Watch Ad**{: .blue } button appears during the queue. Watch a short ad and your server will start right away.

## Free vs Premium

| Feature | Free | Premium |
|---------|------|---------|
| Subject to startup queue | Yes | No |
| Skip by watching an ad | Yes | N/A |
| Automatic retries | Every 60 seconds, up to 30 attempts | Instant start |
