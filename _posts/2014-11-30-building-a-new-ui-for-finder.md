---
layout: post
title: Building a new UI for Finder 2.0
permalink: building-a-new-ui-for-finder
date: 2014-11-30 18:50:11
---

For the last one month we have been trying every available HTML5 UI frameworks on the planet to see what would eventually fit our bill for [Finder 2.0](http://blog.applait.com/77 "Finder 2.0 and FinderJS 1.1 –  215% more love").


## How we decided our approach

Our requirements were multifold:

- We wanted something open source. Could be commercial, but we needed the source.
- We wanted something that will not hog up memory with unnecessary bloat.
- We wanted something that does not pollute the DOM, resulting in clean and beautiful code.
- We wanted something that we could easily extend and customize without much overhead.
- We wanted something that will help us main zero technical debt for our apps.
- **We wanted something that did not take too much decisions on our behalf.**

Apart from the top five requirements, the last one was especially important for us. None of us at Applait like being told around, especially by frameworks about how we should code.

The list of frameworks and libraries we tried out include Ionic, Angular, Chocolatechip UI, Onsen, Sencha and DevExtreme. We built five simple apps, one with each of these frameworks/libraries, adding the type of DOM elements and interactions we will need for the final app, and stress tested for performance. But we quickly found out that none of these were going to match all our requirements.

We decided that we need to build our own UI (:grin:). We needed to write a basic MVC/MVP engine that would handle just the routing, rendering and an event driven API. And then we had Riot.


## Why we chose RiotJS

The choice was really simple, once we found it. [RiotJS](https://muut.com/riotjs) matched all our requirements. It respected the last requirement more than any of the others. It gave us three simple things to work with: an event interface, a routing system and a simple template rendering method.

The documentation is not really the best one out there. In fact, it is somewhat misleading, unless you look straight at the API. But the demos are very helpful. The library itself is just around 4KB, so it is fairly simple to read through the code and understand what it does. It took some time, but then, we ended up with a highly extensible system.

The entire UI has been [made modular](https://github.com/applait/finder/blob/master/js/extend.js) using Riot’s observable interface. [Individual modules](https://github.com/applait/finder/tree/master/js/ui) can plug in any functionality they need, and they have access to the [app’s internal API](https://github.com/applait/finder/blob/master/js/findermodel.js) at all times. The templating engine in Riot (`riot.render()`) is really just a semi-sophisticated string replace method. That worked really well for us, because it gave us the control of fetching the template codes. The routing engine handles a `location.hash` based pattern, where [we can decide](https://github.com/applait/finder/blob/master/js/route.js) how a view is called.

To a programmer looking to prototype quickly with frameworks like Ionic, this doesn’t make much sense. They would need these decisions taken on their behalf; the magic done behind the scenes. But, we wanted to build the science ourself. We wanted that power of customization. Riot gave that to us.


## Using flexbox all through

Kids in near future won’t remember the pain of vertically centering an element on a page. That’s because they will have flexbox.

Our target platform, Firefox OS, has been one of the early adopters of flexbox, and Firefox OS 1.3+ has a very strong support of the flexbox specification. The last version of Finder made partial use of flexbox, but this time we have the whole interface based on it. This has [resulted in a semantic markup](https://github.com/applait/finder/blob/master/index.html) that users of Bootstrap would be jealous of. It has also reduced the amount of CSS drastically. The entire UI is drawn in about [370 lines of CSS](https://github.com/applait/finder/blob/master/css/app.css) code (including comments).


## The bottom line

We put a lot of effort in making sure Finder has a very clean user experience. We re-thought Finder from ground up. We put in each requirement piece by piece. And as we always say, you probably don’t need that library that everyone uses in their app. We hope you enjoy the experience and let us know how we can improve it!

And, for the developers out there, if your app takes less than 1/3rd of the memory that other apps need, it is a feature.


