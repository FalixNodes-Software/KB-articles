<img style="border-radius: 20px;" src="https://i.imgur.com/nyoM6z6.png">

# 📖 FalixNodes Knowledge Base

What's all this? You're currently viewing the articles that make up the [Knowledge Base](https://kb.falixnodes.net/). It's all built on Jekyll, a static website generator we use.

## Table of content

-   [Publishing a New Article](https://github.com/FalixNodes-Software/KB-articles#publishing-a-new-article)
    -   [🛡️ Requirements](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-requirements)
    -   [✍️ Creating an Article](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-creating-an-article)
    -   [📃️ Frontmatter](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-frontmatter)
        -   [Default Options](https://github.com/FalixNodes-Software/KB-articles#default-options)
        -   [Modifications / Addon Options](https://github.com/FalixNodes-Software/KB-articles#modifications--addon-options)
        -   [Getting Started Options](https://github.com/FalixNodes-Software/KB-articles#getting-started-options)
    -   [✒️ Markdown](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-markdown)
        -   [Headers](https://github.com/FalixNodes-Software/KB-articles#headers)
        -   [Emojis / Icons](https://github.com/FalixNodes-Software/KB-articles#emojis--icons)
        -   [Images](https://github.com/FalixNodes-Software/KB-articles#images)
        -   [Lists](https://github.com/FalixNodes-Software/KB-articles#lists)
        -   [Colored Text](https://github.com/FalixNodes-Software/KB-articles#colored-text)
        -   [Tabs](https://github.com/FalixNodes-Software/KB-articles#tabs)
        -   [Blockquote](https://github.com/FalixNodes-Software/KB-articles#blockquote)
        -   [Video](https://github.com/FalixNodes-Software/KB-articles#video)
    -   [📢️ Publishing](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-publishing)

---

# Publishing a New Article

Want to help contribute to the Knowledge base? Write or update an article!

## 🛡️ Requirements

-   The guides must be clear and well explained for the user to understand.
-   Fact check and make sure the information you're providing is accurate.
-   Proofread for any grammatical and spelling mistakes.
-   Validate markdown and html syntax.
-   Provide proper frontmatter.
-   Use valid links and images.
-   Make sure guides are up-to-date.

## ✍️ Creating an Article

All articles are stored within the `content/_posts/` sub-directory. When creating an article, create a `.md` file under the correct section, category and sub-category folders. As an example, if you were to create an article that explains how to install and use a plugin in Minecraft Java, the file would be created as such: `content/_posts/minecraft/modification/plugins/yyyy-mm-dd-plugin-name.md`. You're required to add the date at the beginning of the file name in the `YYYY-MM-DD` format. These dates are used to show when the article was last updated, so that users are aware if an article is up-to-date.

Articles are written in [Markdown](https://www.markdownguide.org/getting-started/). Writing in Markdown is very easy to do. If you need help understanding how to do certain tasks, like creating a link, inserting an image or creating a list, look [here](https://guides.github.com/features/mastering-markdown/).

If you wish to add an alternate version of a guide for a different Minecraft edition (Java or Bedrock). Use a replica of the other title and permalink with the corresponding category (Java or Bedrock) switched.

## 📃️ Frontmatter

<details>

<br>

The frontmatter is the block at the top of every article surrounded by a pair of triple dashes `---`. As the frontmatter is based on YAML, ensure that the correct syntax is followed:

### Default Options

```Markdown
---
layout: post
title: "Title of Article"
category: Java
tags: General
description: "Here is the description of your guide"
keywords: (Main keyword), keyword1, keyword2
permalink: /minecraft/java/general/name-of-article
image: "link"
author: Name
icon: book-bookmark
---
```

| Metadata       | Description                                                                                                                                                                                                                                                 |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `layout:`      | Must **always** remain as `post`                                                                                                                                                                                                                            |
| `title:`       | The title of your guide, make sure it contains the necessary keywords to make it stand out                                                                                                                                                                  |
| `category:`    | Any of the categories in the `content/_categories/` folder _(Case sensitive)_                                                                                                                                                                               |
| `tags:`        | Any sub-category; they are each listed in their corresponding category file in the `content/_categories/` folder. _(Case sensitive)_                                                                                                                        |
| `description:` | A description for your guide, keep it concise, informative and interesting                                                                                                                                                                                  |
| `keywords:`    | Keywords relevant to the topic, with each consecutive keyword being separated by a comma `,`. Main keywords are enclosed by brackets `()`, it functions as a primary identifier and will be combined with normal keywords to improve search result accuracy |
| `permalink:`   | /`section`/`category`/`sub-category`/`short-title` _(Lowercase)_                                                                                                                                                                                            |
| `image:`       | A direct link to an image to be used as a thumbnail _(Optional)_                                                                                                                                                                                            |
| `author:`      | Name of the current author and maintainer. For multiple authors (maximum of 3), use the the array format.                                                                                                                                                   |
| `icon:`        | Direct link to an icon. _(Optional)_                                                                                                                                                                                                                        |
| `toc:`         | Whether to enable table of contents or not. _(Optional, default value is `true`)_                                                                                                                                                                           |

> Encompass your values in quotation marks if it contains symbols other than slashes `/` or hyphens `-`.
> New authors must request for their github account to be manually added to display correct profile pictures.

### Modifications / Addon Options

The below frontmatter options are extra options for **Minecraft modifications and addons (plugins, mods and data-packs)** in addition to the default options:

```Markdown
---
icon: "link"
mod-name: "Name of mod"
mod-software: "Spigot, Paper, Purpur"
mod-url: "link"
---
```

| Metadata        | Description                                                                                                                           |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| `icon:`         | Direct link to the mod's icon                                                                                                         |
| `mod-name:`     | Official mod name                                                                                                                     |
| `mod-software:` | The supported server software relative to the article; if it is in the plugins subcategory, only include plugin server software, etc. |
| `mod-url:`      | A link to the mod's official page or website                                                                                          |

### Getting Started Options

If you wish to include a post from an existing category in the `Getting started` category, use these extra frontmatter options:

```Markdown
---
getting-started-tag: General
post_order: 1
---
```

| Metadata              | Description                                                                        |
| --------------------- | ---------------------------------------------------------------------------------- |
| `getting-started-tag` | Functionally the same as `tags:` but specific to the getting started category only |
| `post_order`          | Order of the post within the Getting-started category                              |

</details>

## ✒️ Markdown

<details>

<br>

[Markdown cheatsheet](https://markdownguide.offshoot.io/cheat-sheet/).

### Headers

Using "# Title of Article" isn't needed; the layout will automatically add the title of the article to the top of the guide. That being said, always use "## Subtitle" instead.
It is recommended to a related Github flavored emoji at the beginning of main subtitles (## or h2) to improve user friendliness (such as: `## :earth_asia: Dynmap`). Emojis/icons will be explained further in the next section.

### Emojis / Icons

Github emojis and a few server software icons are supported to improve user friendliness and add vibrance to your articles:

To use a Github emoji, copy its name including the colons (e.g: `:smile:`) and paste it in the article, we only recommend using them in main subtitles (## or h2) and tabs to avoid over-saturation, a list of all Github emojis can be found in this [cheatsheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).

We have a built in recommended icon and a few server software icons you can use anywhere in your article, with the latter especially so in tabs. We currently support `recommended` for recommended icons and `spigot`,`paper`, `purpur`, `forge`, `neoforge`, `fabric` and `quilt` for server software icons. To add the icon to your article follow the format below, make sure to replace `icon` with one of the options listed beforehand.

```html
<i class="icon"></i>
```

### Images

If you're adding an image to the files, follow the structure below:

```
![Alt text](content/assets/images/posts/...)
```

Replace `Alt text` with an alternate text incase the image is not loaded properly or for accessability purposes. `...` must also be replaced with the actual path of your image including the file name and extension.

### Lists

When typing out steps using lists, make sure to separate each step with a **blank line**. Otherwise, a `<p>` tag will not be generated.

### Colored Text

When navigating around the Dashboard, four colors (Orange, Green, Red, Blue) can often be seen on different buttons such as Restart, Save File, Delete, Connect, etc. It is a good idea to color these words with the same color as can be seen in the Dashboard to make the guides more user friendly and vibrant. Fortunately this can be done by making the word **bold** (`** **`) and immediately following it with an inline attribute with the color as a style name like so:

```
**Connect**{: .blue } **Delete**{: .red } **Restart**{: .orange } **Save File**{: .green }
```

### Tabs

In certain articles, you may want to use tabs to group separate alternate procedures in one place, such as procedures on configuring a software with a plugin and mod version:

```
{% tabs software %}

{% tab software plugin %}

Steps for the plugin go here

{% endtab %}

{% tab software mod %}

Steps for the mod go here

{% endtab %}

{% endtabs %}

```

The first word after the tab keyword is used to group the tabs together, while the words after will be displayed as the tab label.

### Blockquote

There are 4 custom blockquote, which are each used in different context:

**Note:**

Used to add additional information that does not fit in its own paragraph.

```Markdown
> hi this is blockquote
```

**Success:**

Used to signify success messages or completion.

```Markdown
{: .success}

> hi this is blockquote
```

**Warning:**

Used as a warning to avoid something.

```Markdown
{: .warning}

> hi this is blockquote
```

**Error:**

Used as a way to display common errors or issues.

```Markdown
{: .error}

> hi this is blockquote
```

### Video

[Learn how to embed a YouTube video](https://support.google.com/youtube/answer/171780?hl=en)

```html
<video controls preload="auto"><source src="https://example.com/video.webm" type="video/webm" src="https://example.com/video.mp4" type="video/mp4" /></video>
```

> If you're adding a video to the files, use a path like `content/assets/videos/posts/...`.

Make sure to provide both webm and mp4. Webm are much smaller and load faster, although an MP4 file is required as not all browsers support webm format. So the MP4 is more of a fallback option if the user's browser doesn't like the webm format.

</details>

## 📢️ Publishing

Create a pull request in this repo and title it using the following format: "New: `Name of Article`" or if you're editing an article, title it like "Edit: `Name of Existing Article`".

Your edit will be reviewed by our support team along with your code to check for any syntax errors.

---

> All PRs are closed if inactive for a long period of time, usually about 3 weeks to a month.
