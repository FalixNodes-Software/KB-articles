---
title: Changing the Minecraft Server Version
tags: Setup
description: Choose the right server version for more functionality and optimal performance.
keywords:
    - keyword: java
      matches: ["version"]
permalink: /minecraft/java/setup/server-version
author:
       - Mocab
       - Cakey
       - Deka
---

Using the correct server software and version is essential for stability and compatibility. Falix makes this process simple by providing a server version installer directly in the dashboard, which automatically handles Java requirements and removes the need for manual configuration in most cases.

If you are switching Minecraft versions or changing server software, follow the steps below.

{: .warning }

> Always stop your server before changing its version to avoid data corruption or startup issues.

## Choosing the Server Software

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Ensure your server is turned off by clicking the "**Stop**{: .red }" button above the console.

4. Scroll down on the Console page until you find the **Server Version** section.

5. Click on **Server Version**.

After clicking **Server Version**, a list of available server software types will appear. Some of the most popular ones are:

- **Paper** - Stable and widely used, best for plugin-based servers with optimization and additional configuration options.

- **Purpur** - A fork of Paper with extended optimization and configuration options.

- **Fabric** - Lightweight mod loader.

- **Forge** - Mod loader commonly used for large modpacks and heavily modded servers.

- **Vanilla** - Official Minecraft server software with no optimizations or additional configuration options.

Select your preferred software type and click **Next**.

## Selecting the Minecraft Version

1. Choose a version from the available version list for the selected software.

2. Click **Install Version**.

3. A confirmation prompt will appear. Confirm to begin the installation.

4. Wait for the installation process to complete.

Once finished, the dashboard will notify you that the server version has been successfully installed.

### Starting the Server

1. After installing the new version, click "**Start**{: .green }" in the Console to launch your server.

2. After startup, verify that the correct **software type and version** are shown in the Console.

Your server is now running on the newly selected version.

## Additional Notes & Tips

- Plugins and mods must be compatible with the newly selected server version.

- Downgrading Minecraft versions may cause world corruption and backups are strongly recommended.

- Java version management is handled automatically when using the built-in installer.

- If the server fails to start, check the **Console logs** for compatibility or dependency errors.
