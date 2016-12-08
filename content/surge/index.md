---
date: 2016-12-07T14:11:49-08:00
title: Deploying on surge.sh
menu: main
weight: 40
---

Deployment on surge.sh is very simple. Make sure that you set `baseurl` in the `config.toml` file to the desired surge.sh url. To publish our `my-new-site` from the previous section at `http://hugo-my-new-site.surge.sh/`, our `config.toml` should include the line
```
baseurl = "http://hugo-my-new-site.surge.sh/"
```
Now, we simply run
```
$ hugo
```
to generate the html for the website, which is placed in the `public` directory. Enter that folder, and run
```
$ surge
```
Walk through the surge wizard, making sure that the domain you specify matches the one from above.

![Publishing my-new-site on surge.sh](/images/2.png)

And that's it!