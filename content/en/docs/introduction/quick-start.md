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

When you run AppservR for the first time, it will create in the the same directory as the executable:

* a `config.yml` configuration file,
* an `apps` folder containing a sample Shiny app,
* a SQLite database file holding apps and users settings.

Settings which require restarting the server to take effect are defined in the `config.yml` file. Other settings can be changed via the web interface.

### Configuration file

`config.yml` configuration file is created in the same directory as the executable, and allows setting the port and host to listen on, the location of the Rscript executable, etc. It is populated with default settings which should work for most users.

In particular, AppservR will look for the *Rscript* executable at the default install location for your platform. If it is installed elsewhere, you will not see the sample app when navigating to [http://localhost:8080](http://localhost:8080), and you should set the appropriate location in the `config.yml` file.

### Web interface

Go to [http://localhost:8080/admin](http://localhost:8080/admin) to access the admin interface. 

You will first need to register as a user via the signup form. The first user to register is automatically given administrative privileges (which is obviously not the case for the subsequent signed up users).

After you have created your admin account and successfully logged in, you can configure existing or new Shiny apps at [http://localhost:8080/admin/apps](http://localhost:8080/admin/apps). Several apps can live on the same server and are accessed using the path you define.
