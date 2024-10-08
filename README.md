<img style="border-radius: 20px;" src="https://i.imgur.com/nyoM6z6.png">

# 📖 FalixNodes Knowledge Base

What's all this? You're currently viewing the source code that makes up the [Knowledge Base](https://kb.falixnodes.net/). It's all built on Jekyll, a static website generator we use.

## Table of content

-   [TODO](https://github.com/FalixNodes-Software/KB-articles#todo)
-   [Publishing a New Article](https://github.com/FalixNodes-Software/KB-articles#publishing-a-new-article)
    -   [🛡️ Requirements](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-requirements)
    -   [✍️ Creating an Article](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-creating-an-article)
    -   [📃️ Frontmatter](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-frontmatter)
        -   [Default Options](https://github.com/FalixNodes-Software/KB-articles#default-options)
        -   [Plugin Options](https://github.com/FalixNodes-Software/KB-articles#plugins)
    -   [✒️ Markdown](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-markdown)
        -   [Headers](https://github.com/FalixNodes-Software/KB-articles#headers)
        -   [Images](https://github.com/FalixNodes-Software/KB-articles#images)
        -   [Blockquote](https://github.com/FalixNodes-Software/KB-articles#blockquote)
        -   [Video](https://github.com/FalixNodes-Software/KB-articles#video)
    -   [📢️ Publishing](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-publishing)
    -   [🏗️ Building and Testing Locally](https://github.com/FalixNodes-Software/KB-articles#%EF%B8%8F-building-and-testing-locally)
        -   [Running Natively](https://github.com/FalixNodes-Software/KB-articles#method-1-running-natively)
        -   [Running with Docker](https://github.com/FalixNodes-Software/KB-articles#method-2-running-with-docker)

---

## TODO

<details>

-   [ ] Improve embeds with author & date updated, etc
-   [ ] Add video thumbnails
-   [ ] Auto toggle subcategories filter based on url
-   [ ] Add hero image to home and category pages (maybe?)
-   [ ] Revisit lighthouse
-   [ ] Multilingual support (maybe?)
-   [ ] Use shadows
-   [ ] Add color contrast between boxes and background
-   [ ] Add a box around aside elements
-   [ ] Redo search result layout
-   [ ] Make toc a tree view
-   [ ] Make java-bed switcher buttons more clear
-   [ ] Add more links to header and change footer layout
-   [ ] Redo post fooder css
-   [ ] Add keywords frontmatter

</details>

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

By following the folder and file structure, create a `.md` file under the correct section, category and sub-category. As an example, if you were to create an article that explains how to install and use a plugin in Minecraft Java, the file would be created as such: `_posts/minecraft/plugin/general/yyyy-mm-dd-plugin-name.md`. You're required to add the date at the beginning of the file name in the `YYYY-MM-DD` format. These dates are used to show when the article was last updated, so that users are aware if an article is up-to-date.

If you wish to add an alternate version of a guide for a different Minecraft edition. ensure that both titles and permalinks are exact replica of each other.

Then start writing the article in [Markdown](https://www.markdownguide.org/getting-started/). Writing in Markdown is very easy to do. If you need help understanding how to do certain tasks, like creating a link, inserting an image or creating a list, look [here](https://guides.github.com/features/mastering-markdown/).

## 📃️ Frontmatter

<details>

<br>

Make sure the frontmatter is setup properly; this is usually at the top of every article.

### Default Options

```Markdown
---
layout: post
title: "Title of Article"
category: Java
tags: General
description: "Here is the description of your guide"
permalink: /minecraft/java/general/name-of-article
image: "link"
author: Name
icon: book-bookmark
---
```

| Metadata       | Description                                                                                                                  |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| `layout:`      | Must **always** remain as `post`                                                                                             |
| `title:`       | The title of your guide, make sure it contains the necessary keywords to make it stand out                                   |
| `category:`    | Any of the categories in the `_categories` folder _(Case sensitive)_                                                         |
| `tags:`        | Any sub-category; they are each listed in their corresponding category file in the `_categories_` folder. _(Case sensitive)_ |
| `description:` | A description for your guide, keep it concise, informative and interesting                                                   |
| `permalink:`   | /`section`/`category`/`sub-category`/`short-title` _(Lowercase)_                                                             |
| `image:`       | A direct link to an image to be used as a thumbnail _(Optional)_                                                             |
| `author:`      | Name of the current author and maintainer. For multiple use the array format. Maximum limit of 3                             |
| `icon:`        | Direct link to an icon. _(Optional)_                                                                                         |
| `toc:`         | Whether to enable table of contents or not. _(Optional, default value is `true`)_                                            |

> Encompass your values in quotation marks if it contains symbols other than slashes `/` or hyphens `-`.
> New authors must request for their github account to be manually added to display profile pictures.

### Modifications / Addon Options

The below frontmatter options are extra options for **Minecraft modifications and addons (plugins, mods and data-packs)** in addition to the default options:

```Markdown
---
layout: post
title: "Title of Article"
category: Modifications
tags: General
description: "Here is the description of your guide"
permalink: /minecraft/modifications/general/name-of-mod
image: "link"
author: Name

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
It is recommended to a related Github flavored emoji at the beginning of main subtitles (## or h2) to improve user friendliness (such as: `## :earth_asia: Dynmap`). A list of all Github emojis can be found in a [cheatsheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).

### Ordered Lists (Steps)

When typing out steps using ordered lists, make sure to separate each step with a **blank line**. Otherwise, Karamdown will not generate a `<p>` tag.

### Images

If you're adding an image to the files, use a path like `content/assets/images/posts/...`.

### Colored Text

When navigating around the Dashboard, four colors (Orange, Green, Red, Blue) can often be seen on different buttons such as Restart, Save File, Delete, Connect, etc. It is a good idea to color these words with the same color as can be seen in the Dashboard to make the guides more user friendly and vibrant. Fortunately this can be done by making the word **bold** (`** **`) and immediately following it with an inline attribute with the color as a style name like so:

```
**Connect**{: .blue } **Delete**{: .red } **Restart**{: .orange } **Save File**{: .green }
```

### Recommended

If you want to add a recommended symbol beside a server software or such, use:

```html
<i class="recommended"></i>
```

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

> If you're adding a video to the files, use a path like `/assets/videos/posts/...`.

Make sure to provide both webm and mp4. Webm are much smaller and load faster, although an MP4 file is required as not all browsers support webm format. So the MP4 is more of a fallback option if the user's browser doesn't like the webm format.

</details>

## 📢️ Publishing

Create a pull request in this repo and title it using the following format: "New Post: `Name of Article`" or if you're editing an article, title it like "Edit: `Name of Existing Article`".

Your edit will be reviewed by our support team along with your code to check for any syntax errors.

## 🏗️ Building and Testing Locally

If you're interested in learning how to build the Knowledge Base locally, maybe to ensure that your article does show up properly, just follow either methods below.

### Method 1: Running Natively

<details>

<br>

Since the Knowledge Base is powered by Jekyll, you'll need to install it [here](https://jekyllrb.com/docs/installation/).
While it's installing, download a copy of this repository.

Once Jekyll is fully installed, open command prompt and change directory (`cd`) to the downloaded repository. Then type and run the following command:

```ShellSession

bundle exec jekyll serve --livereload --watch

```

Once you see a done message, go to <http://localhost:4000/> in your preferred web browser.

</details>

### Method 2: Running With Docker

<details>

<br>

Since we will be using Docker, you'll need to install it [here](https://docs.docker.com/get-docker/).
While it's installing, download a copy of this repository, and create a `docker-compose.yml` file in it's root with the following content:

```YAML
services:
jekyll:
volumes: - "./:/srv/jekyll" - "./vendor/bundle:/usr/local/bundle"
ports: - "4000:4000" - "35729:35729"
image: jekyll/jekyll
command: jekyll serve --livereload --watch --force_polling
```

> If this is the first time running the Knowledge Base, use `bundle install` instead of `jekyll serve --livereload --watch --force_polling`. Once everything is installed you may continue using `jekyll serve --livereload --watch --force_polling`.

Once Docker is fully installed, run it. Then open command prompt and change directory (`cd`) to the downloaded repository, and type and run the following command:

```ShellSession
docker-compose up
```

Once you see a done message, go to <http://localhost:4000/> in your preferred web browser.

</details>

<br>

---

> All PRs are closed if inactive for a long period of time, usually about 3 weeks to a month.
> Theme by [gustavoquinalha](https://github.com/gustavoquinalha/jekyll-help-center-theme). The license can be found [here](https://github.com/gustavoquinalha/jekyll-help-center-theme/blob/master/LICENSE.txt).
