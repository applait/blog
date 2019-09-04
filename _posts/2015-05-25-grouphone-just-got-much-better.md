---
layout: post
title: Grouphone just got (much) better
permalink: grouphone-just-got-much-better
date: 2015-05-25 12:24:16
---

Yesterday we’ve released the Beta 3 of [Grouphone](https://grouphone.me). It’s a brand new public beta launch, which targets some of the most reported & very well known browser/platform compatibility issues and UX enhancements, among other things.

Some of those fixes aren’t very straight forward, as they’re substantially more of moral issues, than technical ones. We’ve tried to explain them in the later part of this post.


## Public Beta

**Grouphone opens up for public Beta!**

Previously, we had opened up limited access beta, where we’ve had given access to a handful set of selected few users within two short time windows. This was to test the early implementations of the service, until we were satisfied with it.

But now we’ve opened up the Public Beta, which allows you to request access to sign-up for the service whenever you want, [from the login page of the application](https://grouphone.me/login). We’re sending out the sign-up invitations in short bursts, so you won’t even have to wait for many days.

We’re still concerned about the infrastructure capacity, and as such, we’re evaluating & scaling the infra as we go. Hence we’re keeping the request-access model for the time being.


## Browser Incompatibilities

Sadly, the web is way too fragmented than we would like it to be.

For example, Firefox has [major changes](https://hacks.mozilla.org/2015/03/webrtc-in-firefox-38-multistream-and-renegotiation/) in WebRTC implementations in version 34, 37 & 38 from developers’ point of view.

That’s just one browser. There are protocol implementation differences for each browser, across releases, each with pros and cons of their own. Overall it’s a massive moving target.

**What we solved:** issues with getting audio-stream; as in – not being able to hear the other participant(s) – should be fixed for 90% of the reported cases. For the rest of the 10%, it is often fixed by reloading the page. *Please note*, sometime it may also be because of low/muted “Media Volume” set by the user on Android handhelds, but that’s rarer.


## Platform Support

**Grouphone doesn’t work on iOS:** and it won’t. Not in foreseeable future.

Not only in Safari, but in Chrome for iOS as well. The reason being, the underlying layer for them aren’t different on iOS & Apple forces browser vendors to use [their version of WebKit](http://stackoverflow.com/a/29164511), which doesn’t support WebRTC. There’s barely anything we can do about it, [save the lulz](https://twitter.com/kaustavdm/status/602150045534822400).

**Grouphone doesn’t work reliably on Firefox OS version less than 2.0:** and again, it wont. The WebRTC implementation on lower versions of Firefox OS (1.4, 1.3, 1.1 etc.) are way too obsolete, and requires a truck load of non-standard implementations & hacks.


## UX enhancements

**We’ve fixed the “Call End” button not ending calls properly** for Google Chrome on Touch screen devices; and in that process, have implemented a better touch vs click event handling mechanism for the entire application.

**Also, we’ve patched Grouphone for better interaction-feedback**, so the call creation, connectivity, user count, browser/platform is incompatibility etc. are much more transparent. Instead of failing silently (which is confusing & frustrating), Grouphone now will throw particular tantrums, while pointing fingers at the right direction.

![yuno](http://blog.applait.com/content/images/2015/05/yuno-300x300.jpg)

[![WebRTC incompatibility in stock Android browser](http://blog.applait.com/content/images/2015/05/Screenshot_2015-05-25-12-27-35-169x300.jpg)](http://blog.applait.com/content/images/2015/05/Screenshot_2015-05-25-12-27-35.jpg)


## Web Standard Compliance

In last few weeks, we had to make some choices. Choices around technical feasibility vs. feature richness vs. user experience. At the end of the day, we ended up taking the red-pill.

Hence, for example, making the Copy URL to Clipboard isn’t difficult to implement using Flash. In fact, it’s way too trivial – compared to the rest of the pieces of technology. But we chose not to use Flash. We know it’s a little less convenient for the user, and we’re aware that we’ll keep on facing the complains “why don’t you implement Copy URL feature?” – and, we’re okay with it, until a proper web-native solution appears. Till then, we have a small workaround for you: the URL gets updated for you to the call join link. So, **you can directly share the URL using your browser’s “Share” option on Android**.

The same goes for many other lower level choices (from unification of SDP negotiation compliance at the protocol layer to flexbox layout at the interface layer), which is beyond the scope of this blog post.

WebRTC in itself is a pretty new technology, and it’s on the bleeding edge. Check this following table to understand how much more work it needs to get stable.

[![webrtc-compat](http://blog.applait.com/content/images/2015/05/webrtc-compat.png)](http://blog.applait.com/content/images/2015/05/webrtc-compat.png)


## But, wait!

While the big enterprise players are pondering, cowering, squinting eyes & reevaluating to take a shot at it, a handful of folks from Applait brings you a fully-functional group audio call service, using WebRTC.

While we could have written shims to cover these gaps and bridge the fragmentation, that was not the promise of the open web. Grouphone is a project to see how much the web has progressed on the “open” front. We intend to keep it that way.

It wasn’t easy, and it definitely wasn’t as simple as it may look like. But we’re hopeful, your Grouphone experience will get better as the spec gets better – in web technology, as it always does.


