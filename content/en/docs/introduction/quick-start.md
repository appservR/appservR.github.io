---
title: "Quick Start"
description: "A one page tutorial to use AppservR."
lead: "A one page tutorial to use AppservR."
date: 2020-11-16T13:59:39+01:00
lastmod: 2020-11-16T13:59:39+01:00
draft: false
images: []
menu:
  docs:
    parent: "introduction"
weight: 110
toc: true
---

## Requirements

AppservR runs your Shiny apps using your system install of R. You need to have R installed on your system to use it. You will also need the ```shiny``` package and all other R package your app needs. [Learn more about Shiny →](https://shiny.rstudio.com/)

{{< alert icon="💡" text="Make sure first that you are able to run your Shiny app properly using R/Rstudio." />}}

## Download & Install

Get the latest AppservR executable for your platform on our [Github releases page](https://github.com/appservR/appservR/releases). You will need to chose your download option from the "Assets" section of a specific release.

To install, just uncompress the archive at a location of your choice.  

## Run

AppservR is a command-line program with a web graphical user interface. Most settings can be configured using only the web interface, which means that you do not need to have access to the server to configure a new Shiny app, for instance.

Start a terminal window in the directory where AppservR executable lives and then type:

``` bash
./appservR serve 
```

Go to [http://localhost:8080](http://localhost:8080). You should see a running sample app (the classic Shiny's *Old Faithful Geyser Data*, with a twist). If not, see below.

## Configure

When you run AppservR for the first time, it will create in the the same directory as the executable file:

* A `config.yml` configuration file,
* A folder with a sample Shiny app,
* A SQLite database file containing apps and users settings.


AppservR will look for *Rscript* executable at the default install location for your platform. If it is installed 

## Other commands

Doks comes with commands for common tasks. [Commands →]({{< relref "commands" >}})
