---
title: "Customize styling"
description: "Built-in pages (login, etc.) can be customized to match your image."
lead: "Built-in pages (login, etc.) can be customized to match your image."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu:
  docs:
    parent: "recipes"
weight: 120
toc: true
---

## Customize html templates

All buit-in pages, such as signup, login, error pages, are embeded in AppservR executable. However, they can be changed easily if you need to change the text language, add your company's logo, etc.

You just need to create a `templates` directory at the same location as the executable. AppservR will look for existing files in this directory before falling back to the default templates. 

Please check out [this folder](https://github.com/appservR/appservR/tree/main/templates) on Github and copy the templates you want to modify in your `templates` folder (keeping the exact same subdirectories and filenames). The template engine is [Go's default template package](https://pkg.go.dev/text/template). Normally, you would just need to modify the html.

## Add/modify static files

In a similar manner as the `templates` folder described above, you can create an `assets` folder at the same location as AppservR executable. Static files will be looked up in this directory, fall back to default files if they do not exist, and return a `404 not found` error if the file is not present neither in your `assets` directory or in the default [`assets`](https://github.com/appservR/appservR/tree/main/assets) folder.

The content of the `assets` folder is served under the `/assets/` url path.
