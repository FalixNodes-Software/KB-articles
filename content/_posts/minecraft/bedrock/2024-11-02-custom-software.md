---
title: Add Custom Server Software or Version To Your Minecraft Bedrock Server
tags: Setup
description: Find out how to use a custom or modified software or version not available in the versions list.
keywords:
    - keyword: custom
      matches: ["software", "core", "bedrock", "server"]
    - keyword: pocketmine
    - keyword: nukkit
permalink: /minecraft/bedrock/setup/custom-software
author:
    - DynamicSlayer
    - Mocab
---

Before proceeding with this guide, we recommend reading our [server software guide](/minecraft/bedrock/general/server-software) to better understand the terms used below.

Users may often want to use other software not officially provided by Falix, either for their unique features, plugin support or cross-play capabilities. Fortunately this can be done by adding it as a custom core, as will further be explained in this article.

## Choosing the Server Software:

Before we can continue, you must choose a server core and download it. A list of the most commonly used Bedrock server software and their download websites are as follows:

-   [Official Bedrock Dedicated Server](https://www.minecraft.net/en-us/download/server/bedrock)
-   [PocketMine-MP (PMMP)](https://github.com/pmmp/PocketMine-MP/releases)
-   [NukkitX](https://ci.opencollab.dev/job/NukkitX/job/Nukkit/job/master)

{: .warning }

> **NEVER** download shady or untrusted server software, or software from unofficial websites. Malicious developers can use them to easily gain backdoor access to your server and wreck havoc.

## Installing It on Your Server:

{% tabs customSoftware %}
{% tab customSoftware <i class="bedrock-software bedrock"></i> Official Bedrock Server %}

{: .warning }

> Make sure to make a backup of your server to prevent any data loss.

1. Download the Dedicated Server Software for Ubuntu **(Linux)** from the [Minecraft Bedrock website](https://www.minecraft.net/en-us/download/server/bedrock).

    > If you are looking for a preview version, download Dedicated Server Software for Ubuntu (Linux) Preview instead.
    > If you are looking for an older version, you **must** agree to the [Minecraft End User License Agreement](https://www.minecraft.net/en-us/eula) and [Privacy Policy](https://www.microsoft.com/en-us/privacy/privacystatement), then copy the download link and change the version near the end of the link with the one you are looking for (e.g: `.../bedrock-server-1.20.81.01.zip`). Open the link to begin downloading the `.zip` archive.

2. Login to the [Dashboard](https://client.falixnodes.net/).

3. Choose a server from your server list.

4. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console). Make sure your server is offline by clicking on the "**Stop**{: .red }" button at the top of the console.

5.  In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

6. Select all the files using the tickbox on top left of the file manager ribbon.

    > If you are only updating the server you will only need to select the `bedrock_server` file.

7. A mass actions popup should appear, click on "**Delete**{: .red }" to delete the files.

8. Click the "**Upload Files**{: .blue }" button and select the `.zip` archive.

    > If you are updating your server, extract the archive and only upload the `bedrock_server`.

9. If you uploaded the entire archive, find it and press the three dots to its right and click "Unarchive".

10. After unarchiving, navigate back to the [Console](https://client.falixnodes.net/server/console) and start your server.

{% endtab %}
{% tab customSoftware <i class="bedrock-software nukkit"></i> NukkitX %}

1. Login to the [Dashboard](https://client.falixnodes.net/).

2. You will be redirected to your server's [Console](https://client.falixnodes.net/server/console). Make sure your server is offline by clicking on the "**Stop**{: .red }" button at the top of the console.

3. In the navigation menu, open the "Console & Files" category and navigate to [File Manager](https://client.falixnodes.net/server/filemanager).

4. If you already have a `.jar` file, click on the three dots to its right and press the "**Delete**{: .red }" button.

5. Click the "**Upload Files**{: .blue }" button and select your downloaded `.jar` file.

6. Ensure the uploaded file is named `server.jar`. If it is not, press the 3 dots to its right and select "Rename".

7. In the top navigation bar, hover over "Manage" the navigate to the [Settings](https://client.falixnodes.net/server/settings) page.

8. Locate "Environment" and make sure it is set to the latest Java version available.

9. Navigate back to the [Console](https://client.falixnodes.net/server/console) and start your server.

10. Language codes will appear in the console. Select your preferred language by typing its code. For example, if you want to select English, type `eng`.

{% endtab %}
{% endtabs %}

{% comment %}

// Manual installation for PMMP is broken as of now, but the installing from the Versions page is still available.

{% endcomment %}
