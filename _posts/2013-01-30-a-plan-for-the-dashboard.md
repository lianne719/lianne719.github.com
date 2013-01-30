---
title: A Plan for the Release Tracking Dashboard
layout: post
categories: opw
tags: [mozilla, opw]
---
I know, I'm no writer and I need nudges and several reminders just to write a blog post (winks to Marina and Lukas ![>.-](http://www.pic4ever.com/images/2chw5mg.gif)). Anyway, here's what I have been up to.

The past few weeks have been all about moulding the dashboard's requirements and getting started on coding what a user, either the release team or any other contributor, will be able to SEE. 

<img src="/img/countdown.png" width="500" title="Dietrich's live countdown dashboard"/>

The dashboard's main page will adopt Dietrich's [FirefoxOS Status](http://people.mozilla.com/~dietrich/basecamp/counts.html), with extra large indicators as to how far away Firefox is from being able to be released, in terms of open bugs left. This will be where the release team and contributors get an idea of the overall progress of the product, before having the choice of drilling down to a more detailed view of what exactly is driving those numbers.

![Individual view draft](/img/individual_view.png)

The first of two dashboard views is the individual view, where a user will be able to identify assigned and tracked Beta, Aurora, and ESR bugs by default. An option to login will enable the user to view his/her assigned security bugs (easily distinguishable from normal bugs as they will be displayed in a different font/highlighting/colour - blue in this case as shown above). Additional security group bugs that are not tracked will appear after those tracked. Ideally, some visualization of a user's level of activity/progress can be illustrated, which I think would be a great motivation for contributors to work towards resolving as many bugs, ASAP.

<img src="/img/harthur.png" width="500" title="HArthur's to-do list"/>

Besides logging in, another plan for the individual view is to incorporate a menu similar to that of Heather Arthur's [Bugzilla ToDo's](http://harthur.github.com/bugzilla-todos/), but only including bugs that are to be nominated, waiting for approval, or waiting to be uplifted. Although, I might have to steal Heather's design ideas because that one page is so simple, focused, and just plain cute!

While trying to understand the various stages a bug can fall into, I recently learnt that a resolved bug does NOT mean that a case closes! The **shortest** example (thanks a bunch to Lukas for explaining it to me a million times, finally typing it out for me to further spend time to digest): bugs that are *waiting for approval* is defined (in Bugzilla terms) as 
> (1) tracked bugs that are RESOLVED FIXED, (2) at least one of the status-firefox &lt; version> flags for Aurora/Beta are NOT marked fixed, but (3) it does have a patch(es) already nominated for approval-mozilla-(beta,aurora) with a ?

For interested beginners, I suggest looking at bug 819781, or spend several hours staring at the definition, then search bug 819781!

I shall leave the second dashboard view to a later time, when more thought has been given to what needs to be presented. For now, finishing the core functionality of the individual view!

