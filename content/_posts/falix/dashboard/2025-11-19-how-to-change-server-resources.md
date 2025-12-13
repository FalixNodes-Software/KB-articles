---
layout: post
title: "How To Change Server Resources"
tags: Server
permalink: falix/dashboard/general/change-resources
description: "Learn how to allocate and change your server's CPU, memory, and disk resources."
keywords:
    - keyword: resources
      matches: ["change", "allocate", "upgrade", "adjust"]
    - keyword: server
      matches: ["cpu", "memory", "ram", "disk", "storage"]
    - keyword: settings
      matches: ["configuration", "allocation"]
author: Lily
---

{: .warning}
> It's not possible to change your resources on the free plan.

## Introduction
After purchasing additional resources for your server, you'll need to allocate them through your server settings. This guide will show you how to change your server's CPU, memory, and disk allocation.

## Before You Start
Please note the following before changing your server resources:

- Changing resources require a server restart to take effect
- Make sure you have purchased the resources you want to allocate
- Your server may experience brief downtime during the restart

## Steps to Change Server Resources

1. Log in to the [Dashboard](https://client.falixnodes.net/).
2. Navigate to your server list and select the server you want to modify.
3. In the left sidebar, click on **Server Settings** -> **Settings**.
4. Click the **Change Resources** button.
5. A modal will appear with the following options:

### CPU Allocation
- Enter the desired CPU allocation
- 1 = 100% of one CPU core
- Minimum value: 0.25 (25% of one core)

### Memory Allocation
- Enter the desired memory in megabytes (MB)
- Minimum value: 128 MB
- Example: For 2GB of RAM, enter 2048

### Disk Allocation
- If you have an unmetered storage plan, this field will show "Unmetered Storage"
- Premium plans include unmetered disk space

6. After entering your desired values, click **Save Changes**.
7. Restart your server for the changes to take effect.

## After Changing Resources

Once you've changed your server resources:

- Your server need to restart for changes to apply
- The new resource allocation will be reflected in your server dashboard
- Monitor your server to ensure it's running properly with the new configuration

{: .warning}
> If your server fails to start after changing resources, make sure you've allocated enough CPU and memory for your server software to run properly.

## Troubleshooting

If you experience issues after changing resources:

- **Server won't start**: Verify you've allocated sufficient CPU and memory
- **Resources not showing**: Try refreshing the page or logging out and back in
- **Changes not applied**: Ensure you restarted your server after making changes

## Need Help?

If you're having trouble changing your server resources or need assistance determining the right allocation for your needs, please contact our [support team](https://client.falixnodes.net/support/).
