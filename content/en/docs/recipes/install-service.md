---
title: "Install as a service"
description: "AppservR can be installed as a service to run automatically in the background."
lead: "AppservR can be installed as a service to run automatically in the background."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu:
  docs:
    parent: "recipes"
weight: 130
toc: true
---

## Manage service via the CLI

The `appservr service` command allows installing and managing the AppservR service.

{{< alert icon="💡" text="Managing services requires to run a command prompt as admin on Windows." />}}

### Install

`appservr service install` sub-command will install appservr as a service (still running the executable at its current location).

On Windows, we recommand that you modify the service in the services configuration panel afterwards in order to have it ran by a non-admin account. Otherwise, you allow AppservR admin to run arbitrary scripts as admin, which is a security threat (AppservR uses your system installation of R and is not isolated from your system).

### Start

`appservr service start` will start the service.

### Stop

`appservr service stop` will stop the service.

### Uninstall

`appservr service remove` will uninstall the service if it is already stopped, or right after it is stopped.
