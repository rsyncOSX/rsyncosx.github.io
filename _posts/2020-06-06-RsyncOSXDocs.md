---
layout: post
title:  "How to use RsyncOSX"
permalink: rsyncosxdocs
---
June 2020, the Jekyll Based docs are archived and not updated, please [see the Hugo based docs](https://rsyncosx.netlify.app/).

RsyncOSX is a GUI ontop of the command line utility rsync, no more no less. Rsync is a file-based synchronization and backup tool. RsyncOSX supports both synchronize and snapshot tasks. There is no custom solution for the synchronized archive. And you can quit utilizing RsyncOSX (and rsync) at any time and still have access to all synchronized files.

 - [getting and installing RsyncOSX](/rsyncosx)
 - [there is a changelog](/changelog)
 - [signing and notarizing of RsyncOSX](/notarized)

![](/images/RsyncOSX/master/intro/main.png)

### Intro

- a short [intro to RsyncOSX](/intro)

### Remote servers

Using RsyncOSX for synchronize files to remote servers require some setup.

- [there are two options to setup passwordless logins](/remotelogins)
- the preferred [setup by ssh keys](/ssh)
- and a [rsync daemon setup](/rsyncdaemon)

### Add and execute single tasks

- [add configurations](/addconfigurations)
- [executing single tasks](/singletask)

### Parameters to rsync

- [default parameters](/rsyncparameters)
- [user selected parameters](/userparameters)

### Snapshots, quick backup and scheduling

- utilizing the [snapshot feature](/snapshots)
- utilizing the [quick backup feature](/quickbackup)
- [automatic backups](/automatic)
- [scheduling of tasks](/scheduletasks)

### Restore

- [restore of files](/restore)

### Logging, configuration, config files, verify

- some info about [logging execution of tasks](/logging)
- some info about [user configuration](/userconfiguration)
- where does RsyncOSX [stores the config files](/configfiles)
- [the verify function](/verify)

### Source code and compile

- some info [about the source code and how to compile RsyncOSX](/compile)
