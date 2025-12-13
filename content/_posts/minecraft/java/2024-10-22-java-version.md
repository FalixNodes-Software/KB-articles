---
title: Changing the Minecraft Server Java Version
tags: General
description: Choose the right server Java version for functionality and optimal performance.
keywords:
    - keyword: java
      matches: ["version", "environment"]
permalink: /minecraft/java/general/java-version
author:
       - Mocab
       - Cakey

toc: false
---

Minecraft: Java Edition runs on Java, and using the correct server software and version is essential for stability and compatibility. FalixNodes makes this process simple by providing a built-in server version installer directly in the dashboard. This method automatically handles Java requirements and removes the need for manual configuration in most cases.

If you are switching Minecraft versions, changing server software, or setting up plugins or mods, follow the steps below.

{: .warning }

> Important: Always stop your server before changing its version to avoid data corruption or startup issues.

## Step-by-Step Instructions

1. Log in to the FalixNodes [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). Ensure your server is turned off by clicking the "**Stop**{: .red }" button above the console.

4. Scroll down on the Console page until you find the Server Version section.

5. Click on Server Version.

## Choose Server Software

After clicking **Server Version**, a list of available server software types will appear. Select the option that best fits your needs:

- **Vanilla** – Recommended if you do not plan to use plugins or mods.

- **Purpur / Paper** – Best for plugin-based servers with improved performance and configuration options.

- **Fabric** – Lightweight mod loader, commonly used for performance or client-side mods.

- **Forge** – Required for many large modpacks and heavily modded servers.

Select your preferred software type and click **Next**.

---

## Select Minecraft Version

1. Choose a version from the **available version list** for the selected software.

2. Click **Install Version**.

3. A confirmation prompt will appear. Confirm to begin the installation.

4. Wait for the installation process to complete.

Once finished, the dashboard will notify you that the server version has been successfully installed.

## Start the Server

1. Click **Start**  to launch your server.

2. After startup, verify that the correct **software type and version** are shown in the Console.

Your server is now running on the newly selected version.

---

## Additional Notes & Tips

- Plugins and mods must be compatible with the selected server version.

- Downgrading Minecraft versions may cause world corruption so backups are strongly recommended.

- Java version management is handled automatically when using the built-in installer.

- If the server fails to start, check the **Console logs** for compatibility or dependency errors.
