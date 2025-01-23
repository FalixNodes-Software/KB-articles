---
title: How To Change Your Server Icon
tags: General
permalink: /minecraft/java/general/server-icon
description: Set a custom and unique icon to make your server stand out in multiplayer servers list.
keywords:
    - keyword: icon
    - keyword: server
      matches: &server_matches ["image", "logo", "picture", "thumbnail"]
    - keyword: custom
      matches: *server_matches
author:
    - Naoki
    - Deka
    - Mocab
---

The server icon is a great way to customize your server with a unique icon visible in the multiplayer server list. Not only will it help grab players' attention, but it will also make your server stand out.

## Preparing a Server Icon

Due to limitations, icons must be in the `.png` format and to avoid stretching or compressing the image, an image of size 64 by 64 pixels must be used. You may use any tool or software to achieve this, however in this article we will be using [Casper's Server Icon Maker](https://casperslab.me/falix/server-icon-maker/).

> Since the image is in the `.png` format, transparency is supported.

1. Go to [Casper's Server Icon Maker](https://casperslab.me/falix/server-icon-maker/).

2. To upload your server icon, click on "Upload", then select your icon.

3. Once your icon has been uploaded, ensure it looks as wanted on the preview provided.

4. Click on "Download" to download your server icon.

5. Ensure the image has `server-icon.png` as it's name.

## Applying It to the Server

1. Log in to the [Dashboard](https://client.falixnodes.net/).

2. Choose a server within your server list.

3. You will be redirected to your server's [Console page](https://client.falixnodes.net/server/console). In the top navigation bar, hover over "Manage" then navigate to the [File Manager](https://client.falixnodes.net/server/filemanager).

4. Click on the "**Upload Files**{: .blue }" button and select the previously generated icon.

5. Navigate back to the [Console page](https://client.falixnodes.net/server/console) and (re)start your server to apply your icon.
