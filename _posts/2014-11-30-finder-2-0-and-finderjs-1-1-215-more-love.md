---
layout: post
title: Finder 2.0 and FinderJS 1.1 -  215% more love
permalink: finder-2-0-and-finderjs-1-1-215-more-love
date: 2014-11-30 18:54:56
---

After one and a half month since [Finder 1.1](http://blog.applait.com/41 "Finder 1.1 released: What’s new?"), we launched [Finder 2.0](https://marketplace.firefox.com/app/finder) today. All these days we were cooking our secret sauce that would make Finder more usable and will pack in more of Applait love. Finder 2.0 is a complete rewrite of Finder, making the code more modular, the UI more appealing and the search more accessible. The new version of Finder takes **215% less memory** than its predecessor. We also plugged in the latest release of FinderJS, making searches **230% faster**. Go give it a spin now!


[![Download from Firefox Marketplace](http://blog.applait.com/content/images/2014/10/firefox-marketplace_badge-orange_172_60.png)](https://marketplace.firefox.com/app/finder/)

## What we did in FinderJS 1.1

Last week, we launched version 1.1 of [FinderJS](https://github.com/applait/finderjs), the library for searching files in the DeviceStorages of Firefox OS. Finder depends on FinderJS to provide easy access to DeviceStorages. To have the best out of Finder, we started optimizing it at the very core. The new version solves three major concerns that we had with the previous version:

- we added a reliable way to predict when a search was completed,
- we cut down the complexity in the `search` method, resulting in faster enumeration over the file system, and,
- we added a reliable file count found in a search.

FinderJS is built from the ground up to be an asynchronous library. It communicates through events and does not block the UI at all. To put it in simple words, FinderJS does not keep the client application waiting when it searches files. The moment it finds a matching file, it flings the file at the client application, which can then decide whatever it wants to do with the file. If there is something important happening in FinderJS, there is an event for that.

We did a benchmark on a Flame, running latest release build of Firefox OS 2.0.0-pre-release. We used a 4 GB sdcard on the device, filled with files, to search for files matching the name “jpg”. FinderJS 1.0 took 8.5 seconds (± 0.5 seconds) and FinderJS 1.1 took 3.5 seconds (± 0.2 seconds) to complete the search. That is a **242% speed boost in FinderJS 1.1**!


## What’s new and improved in Finder 2.0

The UI of Finder 2.0 is the first step to create a unified feel across apps made by Applait. The unified top navigation is one of the things we have worked on. It heavily draws influence from Firefox’s mobile browser. It will be the place for the main action on an app, and will also serve as the heading and access to settings.

Apart from that, Finder 2.0 includes:

- A new “share” option, where you can share a file that you have searched in Finder, over bluetooth, messages or email. This is only available in normal mode, i.e. if you open Finder directly, instead of opening it to pick file from another app.
- Smooth transitions between screens, making the UX more meaningful.
- A detailed file view page where you can see more information about the file.
- Support for showing file type in the search results through icons. Only a limited set of file type detection is available at the moment.
- Huge performance improvements!

### Performance improvement in Finder 2.0

This version of Finder is based on FinderJS 1.1. So, it has inherited the speedier search that FinderJS 1.1 has introduced. On the UI front, Finder 2.0 takes about 800KB to start up. A search with around 75 results takes the app memory up to 1.3 MB. Compared to that, Finder 1.1 took about 1.8 MB to start, and a search with 75 results took about 2.8 MB of memory. That is a flat **215% improvement in memory optimization in Finder 2.0**!

If those stats look impressive, read on to find [how we got to this level of speed and optimization](http://blog.applait.com/93 "Building a new UI for Finder 2.0")! Try out Finder 2.0 and let us know how we can improve!


