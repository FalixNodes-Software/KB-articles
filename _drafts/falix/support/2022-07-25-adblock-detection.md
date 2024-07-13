---
layout: help/article
title:  "AdBlock Detected - Falix"
icon: <i class='fa-light fa-question'></i>
permalink: /help/falix/support/adblock-detected.*
gitURL: _posts/falix/support/2022-07-25-adblock-detected.md
description: "Find out on how to disable adblock for Falix"

author: Korbs
authorGitHub: korbsstudio
---
<style>
#desktop > section:nth-child(5) {
    display: none;
}
pre:before {
    content: "Command Line";
    width: 120px;
}
</style>

## Disabling Your AdBlock for <u>FalixNodes.net</u>
With most, probably all adblockers, you can whitelist individual domains to allow ads to be displayed on. Go to the whitelist setting of your adblock and add falixnodes.net.

Articles for common adblockers on whitelisting domains:

**AdBlock** - [How to disable AdBlock on specific sites](https://help.getadblock.com/support/solutions/articles/6000055743-how-to-disable-adblock-on-specific-sites)

**AdGuard** - [Unblocking everything on a website](https://kb.adguard.com/en/general/how-to-create-your-own-ad-filters#unblocking-everything-on-a-website)

**uBlock** - [How to mark a web site as trusted](https://github.com/gorhill/uBlock/wiki/How-to-mark-a-web-site-as-trusted)

Articles for common web browsers that have built-in adblocker:

**Brave** - [Shields State](https://support.brave.com/hc/en-us/articles/360022806212-How-do-I-use-Shields-while-browsing-)

**Opera** - [Allow ads for individual pages](https://www.opera.com/features/ad-blocker#more-benefits)

## My AdBlock is disabled or I don't have one
If your browser does not have an adblocker or you are certain that the adblocker is off and the AdBlock Detected message still appears, it is possible that something else is causing the problem, which might be system-wide. 

### Host File
Every now and then, we noticed that our customers have modified their host file which commonly was to block Spotify ads on their desktop. While that might work for Spotify, mostly, it does affect everything else system-wide. If your host file contains a lot of URLs like Google Ads or snigel.com, you need to remove them, all of them. 

Editing the host file will require admin permission, as it's a system file.
Some anti-virus software tend to modify the hosts file, double-check your anti-virus software.

Here's how to access and edit the host file:
**Windows**
1. Search **Powershell** > Open as Admin
2. Type in the following command line and press enter:

{: .note #command }
```
notepad.exe C:\Windows\System32\drivers\etc\hosts
```

**macOS**
1. Open Finder
2. Select the **Go** drop-down menu located at the top of the screen
3. Select **Go to Folder...** > Go to "/private/etc/hosts" 
4. Edit "hosts" file, not "host".

**Linux**
1. Open terminal
2. Type in the following command line and press enter:

{: .note #command }
```
sudo nano /etc/hosts
```