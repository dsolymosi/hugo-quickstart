---
date: 2016-12-07T14:11:49-08:00
title: Creating a Basic Site
weight: 20
---

In this section we will create a basic webpage, which we can then either host locally or deploy on a variety of services. Additional information is available in the [official documentation](https://gohugo.io/overview/quickstart/). Navigate to a location where you want to create the folder holding the site, and execute
```
$ hugo new site my-new-site
```
to create a directory structure for your new site `my-new-site`.

## Choosing a Theme

I suggest choosing a theme from the [Hugo Themes Site](http://themes.gohugo.io/) before adding content to your site. Create a directory called `themes` inside `my-new-site`, and use `git` to clone a theme into that new directory. There will usually be a set of instructions and configuration options on the themes site - some themes even have example content to build upon. For our basic site, we will use the [Aglaus](http://themes.gohugo.io/aglaus/) theme. Within `my-new-site/themes`, execute
```
$ git clone https://github.com/dim0627/hugo_theme_aglaus.git
```

To use the theme without having to specify it each time, open the `config.toml` file in the `my-new-site` directory, and add the line
```
theme = "hugo_theme_aglaus"
```
If you are using a different theme, make sure the name here matches up with the folder your theme resides in.

## General configuration

The `config.toml` file also houses other general configuration settings. In particular, the title of your page and the url it expects to be on are contained in `title` and `baseurl` respectively. Some themes expect further configuration options here.

## Adding content

Although you might already have files in mind for your site, you will want to create most text content through `hugo` commands. Think of content as categorized information entries. To add an entry *New Entry* in the category *Posts*, we navigate to the `my-new-site` directory and execute
```
$ hugo new post/new-entry.md
```
This creates the file `my-new-site/content/post/new-entry.md` with some basic content. Open this file with your favourite text editor to see
```
+++
title = "new entry"
draft = true
date = "2016-12-07T11:36:08-08:00"

+++

```
followed by a few lines of empty space. The information inside the `+++` is called the front matter, and gives some configuration options for your content. For now, let's fix the title to use proper case, and let's set the page not to be a draft.

Content goes at the end of this file. Plain text works fine, and more opting are available using [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Now our `new-entry.md` should look something like this:
```
+++
title = "New Entry"
draft = false
date = "2016-12-07T11:36:08-08:00"

+++

Lorem ipsum dolor sit amet, *consectetur* adipiscing elit, sed do eiusmod ~~tempor~~ incididunt ut labore et dolore magna aliqua.

```

To see how the site looks so far, check [http://hugo-my-new-site.surge.sh/](http://hugo-my-new-site.surge.sh/). To see how we put the site there, check the *Deploying on surge.sh* section!
