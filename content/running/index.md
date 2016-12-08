---
date: 2016-12-07T14:11:49-08:00
title: Running & Deploying the Website
menu: main
weight: 30
---

## Local deployment

It is very easy to run your website locally using Hugo. Navigate to the directory of your site and simply execute
```
$ hugo server
```
Hugo will then generate your site and tell you where it is being served, usually `http://localhost:1313/`. Enter this address in your browser to see a preview, and edit any files you need to. If some content is not showing up, check if they are set to be drafts, or add the `--buildDrafts` flag to your command.
