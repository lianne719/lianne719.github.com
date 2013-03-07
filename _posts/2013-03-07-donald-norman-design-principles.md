---
title: Donald Norman on Design Principles
layout: post
categories: opw
tags: [mozilla, opw]
---
I've recently started paying more attention to the application's design, and Lukas recommended reading up on Donald Norman's views on design. Not just design for web applications, but design for everyday tools - kitchen appliances, vehicles, mobile phones, etc. His speeches reconcile the various types of design techniques out there into one: *user-centered design*. All designers should place themselves in the users' shoes in order to achieve good design. In [one of his presentations](http://www.slideshare.net/gelvan/design-principles), Donald introduces the six design principles that make up good design. Here, I will be describing these six principles in terms of their applications into web design, through my understanding.

#### Visibility
First question to ask: "Can I see it?"
Rules to remember: 
* **Font sizes, layout dimensions, and object positions should be relatively defined (%, em...).** This is to cater for the variation of screen sizes from that of a tiny Blackberry Bold/Curve to a huge 23'' monitor, otherwise your website will be looking like [this](http://www.universalrestaurant.com/home.html). Doubtful that webpages will be seen across 40'' flat screens but one can still plan for that! 
* **Adequate spacing and proper emphasis.** So that users will be able to SEE what they need to WITH EASE. Personally I do not like scrolling too much (unless it involves some attractive Photoshop*ed* background that makes scrolling fun i.e. [Toshiba's hdd site](http://www.canviohdd.com/), anything important should be before my eyes once loaded, so company banners/headers should not take up half the page before showing what NEEDS TO BE SEEN.

#### Feedback
Second question: "What is it doing now?"
Rules:
* **Error notification** is a must, but depending on the target audience and nature of the web application, may or may not be too specific. For example, *Password confirmation is incorrect* would be much more informative than *Invalid input in one of the fields* in a user sign up form, but printing a whole stack trace of an error might lead to exposed source code for hackers!
* **Progress bars** I love them! And would like to figure out how to incorporate them into the dashboard while it is waiting for Flask's server to load data. Otherwise, I'll have to work on the performance (story for a later time) or use JS instead to grab every tab's data separately (very un-MVC-like, but who doesnt love [HArthur's dashboard](http://harthur.github.com/bugzilla-todos/?email=xxx@example.com)?)

#### Affordance
"How do I use it?"
* **WYSIWYG** Although this term was meant for UI editors, I would like to use it here to describe what websites should be to users in terms of features and functionality. [In particular, non-links should NOT have pointers as cursors when hovered over like this.]() In any case, design should never affect what the user thinks the website is capable of doing.
* **Be helpful** to users, provide hints, or lead them in a step-by-step process, but don't overdo it! Again, it still comes down to the target audience.

#### Mapping
"Where am I at using this, and where can I go from here?"
* **Navigation** - Depending on the access priviledges of a user, websites could limit or make abundant the links available to different users. I learnt from my Web Applications course that the admin page should never be a link that can be accessed by a user, rather a separate or entirely different path.
* **Site maps** are nice to have, but I've seen some automated ones that display all available pages without organisation, the site would have been better off without it.

#### Constraint
"Why can't I do that?"
* **Plan** what the user can, or can't do. 
* **Hide/Lighten** buttons/links/menu that cannot be clicked on.
* **Test** if the constraints work, and if the user can perform functions that should be allowed.

#### Consistency
"I think I've seen this before?"
* **Use a layout template** for a consistent header, footer, and menu. 
* **Stick to tradition** Top left for the homepage link, top right for user account summary, etc...

Of course, these are just the foundation towards a good website. As for the looks, style and feel, I'll have to consult others for now ![](http://www.pic4ever.com/images/grouphug.gif)
