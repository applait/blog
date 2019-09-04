---
layout: post
title: Finder is here
permalink: finder-is-here
date: 2014-10-03 22:40:14
---

One of the projects we were working on last week was a solution to search for files on Firefox OS devices. We launched [Finder](https://marketplace.firefox.com/app/finder) today. Finder lets you search and pick files from your device’s storage through a simple interface. It also exposes a web activity through which you can use Finder to pick attachments for email, search multimedia files on your device to attach on Facebook and so on. This is the first preview release. We have big plans going ahead. We are looking for an early feedback for the idea. You can [download the app](https://marketplace.firefox.com/app/finder) from the Firefox Marketplace.

[![Download from Firefox Marketplace](http://blog.applait.com/content/images/2014/10/firefox-marketplace_badge-orange_172_60.png)](https://marketplace.firefox.com/app/finder/)

Update: [Finder 1.1 is released](http://blog.applait.com/41 "Finder 1.1 released: What’s new?").


## Why did we build Finder?

We noticed that there is no application which can search any kind of file on the device storage. Specially, applications needing a custom file type, that is not handled by the Gallery or Camera, need to implement their own file search mechanism. Take for example the PDF Viewer or the Ringtone Picker app.

Also, scrolling through a long list of images or audio files becomes painful if you have lots of them on your sdcard.

Finder solves this problem by giving you a search driven interface. It is not a file browser or file manager. It is a file picker. That means, the interface is geared to show results file by file, instead of a folder based layout. You search for a file name and you get a list of all the files that match the name. You can then tap on the desired result and open it.

If you used Finder to search for file from another app, tapping on the result will send the file back to the app you had opened it from. It will not open the file itself there.


## How does it look like?

Here is how version 1.0.0 of Finder looks like:

[![Initial screen of Finder](http://blog.applait.com/content/images/2014/10/2014-10-03-18-59-06-176x300.png)](http://blog.applait.com/19/2014-10-03-18-59-06#main)Initial screen of Finder

[![Search results of Finder](http://blog.applait.com/content/images/2014/10/2014-10-03-18-59-26-176x300.png)](http://blog.applait.com/19/2014-10-03-18-59-26#main)Search results of Finder

[![No results screen](http://blog.applait.com/content/images/2014/10/2014-10-03-18-59-46-176x300.png)](http://blog.applait.com/19/2014-10-03-18-59-46#main)No results screen of Finder

[![Finder showing up in web activities](http://blog.applait.com/content/images/2014/10/2014-10-03-19-00-13-168x300.png)](http://blog.applait.com/19/2014-10-03-19-00-13#main)Finder showing up in web activities


## Introducing FinderJS

As we had talked about last month, we have been abstracting some of our works as independent libraries. Today we present to you this nifty little library that we call [FinderJS](https://github.com/applait/finderjs). It provides an event driven API to access device storages. Developers can plug this library in their app and get simplify access to device storage.

FinderJS is the backbone that runs the file search behind Finder. To avoid confusion, FinderJS is the JavaScript library and Finder the app we have built using that library.

For more details, check the [FinderJS Github repository](https://github.com/applait/finderjs). You’ll love it.


## Finder is open-source

We have released Finder out in the open. So, if you want to learn how to use the FinderJS library or how to interact with web activities or if you are interested in contributing a patch to Finder, please take a look at the [Finder project page on Github](https://github.com/applait/finder).

Most importantly, if you find issues with Finder or if you have suggestions for its improvements, please file an issue in the [Finder issue tracker](https://github.com/applait/finder/issues).


## Road ahead

The current release is a basic barebone file search. It does not have many of the useful features you may need at the moment. We are working on it. Here is what we plan for the next couple of months:

- Preview a file before selecting it through Web Activity.
- Search through specific file types, e.g. search only through images or videos.
- Group search results into folders.
- Restrict search by date.
- Restrict search by folder.

If you have any feature in mind that you would like to see in future versions of finder, let us know in the comments below or, even better, [file a bug](https://github.com/applait/finder/issues)!

P.S. If you are wondering how long it took us to develop Finder, it took us 1 full day to build the FinderJS library and 1 full day to build Finder itself. That is why we say we can deliver a solution at less than half the time it would take an organisation to build their own stuff.


## Update

**Update as of October 10, 2014**: Finder is [ranking 5 star](https://marketplace.firefox.com/app/finder/ratings) on the Firefox Marketplace with 11 reviews! It got featured in [Mobile Squash](http://mobilesquash.com/finder-app-for-firefox-os-released/), [Firefox OS Central Blog](http://trreeinctech.blogspot.com.es/2014/10/app-of-day-finder.html), [Firefox OS Und Ich](http://firefoxosundich.wordpress.com/2014/10/06/monday-sparks-matchstick-flame-updates-open-web-board/) and got some tweet love:

> [http://t.co/5EiZAkfFZG](http://t.co/5EiZAkfFZG) – Finder, a Firefox OS app to find files on the device storage.
> 
> — Christian Heilmann (@codepo8) [October 6, 2014](https://twitter.com/codepo8/status/519101417425235968)

> App pour trouver un fichier dans votre [#FirefoxOS](https://twitter.com/hashtag/FirefoxOS?src=hash) à tester [https://t.co/tx0g3wB5KL](https://t.co/tx0g3wB5KL) Retours attendus [http://t.co/Gdvnij18Pq](http://t.co/Gdvnij18Pq) [#Finder](https://twitter.com/hashtag/Finder?src=hash) [@applait](https://twitter.com/applait)
> 
> — Monique Brunel (@webatou) [October 4, 2014](https://twitter.com/webatou/status/518349140640931841)


