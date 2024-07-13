<!-- ---
layout: help/article
title:  "WorldGuard and WorldEdit"
categories: Minecraft
icon: <i class='fa-light fa-puzzle'></i>
permalink: /help/minecraft/plugins/worldguard-and-worldedit/
tags: minecraft edit paint brush structure wand protect guard restrict area region define 

author: Korbs
authorGitHub: korbsstudio
--- -->

In-Progress
{: .label .label-yellow }



<div class="install-plugin">
    <img src="https://enginehub.org/static/worldedit-logo.a212455e.svg">
    <p>WorldEdit</p>
    <a href="https://enginehub.org/worldedit/">Download this Plugin</a>
</div>

<div class="install-plugin">
    <img src="https://enginehub.org/static/worldguard-logo.7ceabec8.svg">
    <p>WorldGuard <span class="label label-green" id="plugin-recommend">Recommended</span></p>
    <a href="https://enginehub.org/worldguard/">Download this Plugin</a>
</div>

# WorldGuard and WorldEdit
## WorldGuard
### What is it?
WorldGuard has a host of functions for any server admin, server map makers, regular surivival servers, and everyone else between. You can set zones where players can't or can build in, set additional rules (and set rules per zone), blacklist items and blocks so they can't be used, Useful commands like "STOP ALL FIRE SPREAD" command, protect against many types of abuses, allow only certain actions like interacting with doors and levels, and so much.

### Requirements and Compatibility
#### Requirements
You'll need, of course, WorldGuard itself and WorldEdit so the built-in wand tool can be used.

Use either Spigot or Paper (Paper is recommended over Spigot).

#### Compatibility
WorldGuard supports all versions of Minecraft, but 1.17 (as of the writing of this article), from v1.0.0 to 1.16.5

### How to Use It
#### Setting and Removing a Region
<!-- Leave the two lines below commented in, for whatever reason, the other chat below won't work without it, yes I know it's weird. -->
<!-- | Preview        | Color Code                                      | -->
<!-- |:---------------|:---------------------|:-------------------------| -->

| Set Region | Remove Region      |
|:---------------|:---------------------|:-------------------------|
| <video style="height: 120px; object-fit: cover; object-position: top;" src="/assets/videos/worldedit-worldguard/wg-define.webm" controls muted> | <video style="height: 120px; object-fit: cover; object-position: top;" src="/assets/videos/worldedit-worldguard/wg-remove.webm" controls muted>

What's a region? A region is a zone you can create in WorldGuard that allows you to protect the area inside of it, also making other changes in the zone like game rules and etc.

To set a region, use the `/region` command with the `define` option and providing a name for it.

{: .note #command }
```
/region define <name of region>
```

To remove a region, use the `/region` command with the `remove` option and providing the name of the region you want to remove.

{: .note #command }
```
/region remove <name of region>
```

#### Flags
<!-- Leave the two lines below commented in, for whatever reason, the other chat below won't work without it, yes I know it's weird. -->
<!-- | Preview        | Color Code                                      | -->
<!-- |:---------------|:---------------------|:-------------------------| -->

| Interacting with Flags menu (Not possible in old versions)
|:---------------|:---------------------|:-------------------------|
| <video src="https://help.falixnodes.net/assets/videos/worldguard/flags-wg.webm" controls muted>

Each region can have it's own set of flags, where you can change the way the game behaves in those area like gamerules, interactions, damage, pvp, etc...

As an example:
<!-- Leave the two lines below commented in, for whatever reason, the other chat below won't work without it, yes I know it's weird. -->
<!-- | Preview        | Color Code                                      | -->
<!-- |:---------------|:---------------------|:-------------------------| -->

| Allowing Interactions with Doors and Levels 
|:---------------|:---------------------|:-------------------------|
| <video style="height: 180px; object-fit: cover; object-position: top;" src="/assets/videos/worldedit-worldguard/wg-allow-passthrough.webm" controls muted>

You can set a flag to allow players(or a certain rank if you're using LuckPerms) to interact with doors and levels. This is done with the `passthrough` flag along with the region name in front of it, which can be set to `allow`, it's `deny` by default.

{: .note #command }
```
/flag <name of region> passthrough allow
```


## WorldEdit
### What is it?

### How to Use It
#### Selection Making
<!-- Leave the two lines below commented in, for whatever reason, the other chat below won't work without it, yes I know it's weird. -->
<!-- | Preview        | Color Code                                      | -->
<!-- |:---------------|:---------------------|:-------------------------| -->

| Command Only | With Wand Tool         |
|:---------------|:---------------------|:-------------------------|
| <video poster="https://i.imgur.com/LV1ErEr.png" src="https://help.falixnodes.net/assets/videos/worldedit/pos-we.webm" controls muted> | <video poster="https://i.imgur.com/WRKUTv7.png" src="#" controls muted>

With the **command method**, go to the position you want to set position 1, then use:

{: .note #command }
```
//pos1
```
Do the same for the second position and use:

{: .note #command }
```
//pos2
```
The position, when using the command, is set where your legs are, not your head.

With the **wand method**, you can use the left and right click of your mouse pointer to choose either position 1 and position 2.

Left click: Positon 1

Right click: Position 2

#### Copy, Paste
<!-- Leave the two lines below commented in, for whatever reason, the other chat below won't work without it, yes I know it's weird. -->
<!-- | Preview        | Color Code                                      | -->
<!-- |:---------------|:---------------------|:-------------------------| -->

| Copying and Pasting a Selection
|:---------------|:---------------------|:-------------------------|
| <video src="https://help.falixnodes.net/assets/videos/worldguard/copy-paste.webm" controls muted>

We're all familiar with how copying and pasting works, WorldEdit includes this feature too where you can copy a selection and then paste else.

Using this feature is simply, make a selection of what you want to **copy**, then use:

{: .note #command }
```
//copy
```

Also please be aware of where you're standing when copying, if you copy the selection while it's below you, then it will paste below you.

To **paste**:

{: .note #command }
```
//paste
```

#### Undoing and Redoing
Lots of mistakes can happen while using World Edit, especially when experimenting, luckily there is the undo option to save the day!

Just use:

{: .note #command }
```
//undo
```

If you ever over undo your progress, you can redo by using:

{: .note #command }
```
//redo
```