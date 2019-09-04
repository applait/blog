---
layout: post
title: Security, Reliability, Thank You-s & Next Beta Wave
permalink: security-reliability-thank-you-s-next-beta-wave
date: 2015-04-27 22:42:21
---

First thing first – we’re having our business meetings with our contacts & partners on Grouphone now… and it’s blowing their minds (in a good way)!

But that apart, we have been working hard at getting to the stable release and, as we had said earlier, we are going there in stages. Let us take this opportunity to extend warm hugs to all our beta users. You guys have given us superb constructive criticism, and it has helped us reach this far! Keep it comin’!

Today, we announce the second Beta wave, aka, Beta 2. And this is what it has in store for you.


## Security

The first beta release did not have much focus on security. That was a prioritization we had to do to get the initial release out. But once that was out of the way, we had started working on making Grouphone more and more secure. We are happy to say that our friends all over the internet have helped us identify where we need to tighten up, and another huge thanks go out to them!

### SSL on all layers

Grouphone servers now run on full SSL. Every communication between you and the Grouphone servers are encrypted to the last mile.

This means, even if our ISPs network gets compromised, your data is still encrypted.

Say hi to [https://grouphone.me](https://grouphone.me)!

### Enhanced password protection

Previously, we had ensured that your password passes through two layers of dynamic hashing till it gets stored in our database. But, we were still sending passwords as cleartext to our servers. That was scary, but, once again, that was a priority we had set to get an audio call experience available. This is what we have done to make up for that.

Now your password does not remain in cleartext at any point between your browser and the database. At each layer it gets rehashed again, and, each of the rehashing is done with a different encryption salt at each stage. Even if someone gets through all these layers, they will still need these encryption salts to use the information they have. Plus, all these hashing is a one way street. Even if you have the hashed password and the salt, you can never get the original text out of it, at any stage.

This also means, even *we* don’t have any access to your cleartext password.

#### Need new passwords

As a side-effect of this upgrade, your existing passwords will not work any more. We have to sent out reactivation emails for existing accounts, and this is going to be a one time thing! If you already have a Grouphone account, you will need to reactivate it following the link in that email, or you can always request a new activation link through “Forgot Password” at **grouphone.me**.


## Improved platform support

We have tested Grouphone to now work on latest Firefox and Chrome on Linux, OSX and Windows. We have ironed out some of the UI glitches as well, making the group call experience more reliable.

It currently works on Firefox for Android and Chrome on Android as well, and we are trying to improve the experience on mobile platforms.

*There were issues with call disconnection, and now that has been cleared. Just to clarify here, if the call creator ends the call, it is actually supposed to end for all the participants currently connected to that call.*


## Smoother and better feedback

Some of you were not happy with sending feedback over email (but still you did, and we love you for that!). So, now, we have embedded a live chat widget. If you have feedback, you can directly give it from the app, or you can head over to [Grouphone’s Scrollback channel](https://scrollback.io/grouphone). We’re listening!


## Big thanks!

We have received a wide range of feedback over the past couple of weeks. Among all of them, we would especially like to thank [Jaipradeesh](https://mozillians.org/u/dolftax/) for helping with the frontend development & [Sumantro Mukherjee](https://mozillians.org/u/SumantroMukherjee/) for running full on security suite to generate report for us. You dudes rock! And you’ve forced us to start designing some swags that we can gift you as a token of appreciation!

![Grouphone Tshirt](http://blog.applait.com/content/images/2015/04/grouphone-tshirt.png)


## Next wave

We have already sent out invitations to the next wave of Beta users. If you don’t have a Grouphone account either ping us, or wait, we are opening up invitation requests on grouphone.me soon!

Till then, enjoy!


