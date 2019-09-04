---
layout: post
title: Porting an app is more than just the manifest
permalink: porting-an-app-is-more-than-just-the-manifest
date: 2014-07-16 12:00:09
---

Last month while [introducing ourselves](http://blog.applait.com/10 "The name is Applait") to the world, we had talked about porting existing web applications to Firefox OS for just USD 100. Since then, we have been asked whether we will just a manifest file for those web applications and charge $100 for it. The short answer is: No, there is more to porting an app than writing a manifest.

The manifest for a Firefox OS app is a JSON file containing metadata and permission information for that app. We don’t charge $100 for writing just a manifest. We are tech guys at heart and we are hardcore believers of automation. Instead of writing manifest files by hand and charging $100 for it, it will take us lesser effort to build a system which generates manifest files and hosts them for everyone for free. And we have done just that.


## Generate manifest and host it. For free.

We have opened up our [app testing platform](http://explore.applait.com), which currently supports hosting your own web app. When you create the web app, you can download the manifest for it as well. You can then use the app URL you install it as a fully functioning app on your Firefox OS devices/Firefox browser/Firefox OS simulators. But not everyone will be satisfied that way.


## So, what are we charging for?

What we meant when we talked about USD 100 are the things that you need to do *apart* from writing the manifest. They are:

- Create a launch page tuned to display as a mobile app.
- Use proper app-cache to reduce bandwidth consumption.
- Create multiple dimensions of existing logos for the app.
- Take care of basic Content Security Policy issues.
- Ensure your app goes into the marketplace.
- Do all of the above in a couple of hours.
- Bonus: Tell you stories about how great the Firefox OS platform in between the coffee breaks.

So, if you have a web app to port to Firefox OS, you have very less time in your hands and you have $100 in your pocket, we are the people you are looking for.


