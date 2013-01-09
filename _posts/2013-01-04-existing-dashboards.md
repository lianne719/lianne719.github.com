---
title: Mozilla's Existing Dashboards
layout: post
categories: opw
tags: [mozilla, opw]
---
Before coming up with a relman/releng dashboard, I had to examine various dashboards created by fellow Mozillians that helped in bug searching in one way or another. There may be some that I missed, but I'll try my best to evaluate more in the coming week in order to be sure of what we need for our dashboard. 

###[Bugs Ahoy!](http://www.joshmatthews.net/bugsahoy/) by Josh Matthews
For new Mozilla contributors, this is a great place to search for bugs according to aggregated components. Using pure Javascript to communicate with the Bugzilla API and HTML/CSS to render the contents, Bugs Ahoy! is a single page application which allows for searches of open bugs by components and skills, with the additional option of displaying only unassigned bugs. Besides bugs related to the search components, there is also a link to each team's wiki if the user wishes to get more involved. The dashboard adopts the three column layout, with search filters and extra information on both right and left columns, and the list of bugs located in the middle column. Content is cut down to a minimum for the bugs list (in descending order of time reported), including only the bug's ID and a short summary. On hover, information about the bug's last update and asignee are displayed. I personally feel that Bug's Ahoy! is certainly a much better experience than searching using bugzilla's search engine.

###[bzhome](http://harthur.github.com/bzhome/) by Heather Arthur
For all who have contributed, bzhome is a good way to keep track of recently updated bugs related to a user. The single page application was written in Javascript, HTML and CSS. The site prompts for the user's email address on entering, and displays the user's bugs list. The list can be filtered by component or bugs that were CC'd/assigned to the user. Visually simple and straight forward, each section has a heading to avoid confusion. However, the reviews and feedback sections do not seem to display any information.

###[Bugzilla-Dashboard](http://hg.toolness.com/bugzilla-dashboard/raw-file/tip/index.html?username=<bugzilla_username>) by Atul Varma
Bugzilla Dashboard is a more organized dashboard for experienced contributors, also written in Javascript. After specifying a Bugzilla user email address, the user's bugs to review, assigned, reported, cc'd and recently fixed bugs can be viewed on one page, in time descending order. Besides the different lists of bugs that can be related to a user, I especially liked Atul's menu to authenticate an existing user, change a user, refresh/repair the existing bugs lists, find a user, and file a bug. Overall, the page looks simple and neat, but requires scrolling horizontally to view all five bugs lists.

###[Firefox OS Status](http://people.mozilla.com/~dietrich/basecamp/) by Dietrich, along with Basecamp Blockers 
This easy dashboard shows Firefox OS Basecamp contributors the number of bugs they are assigned with. To avoid scrolling, contributors can search their names to see if they are assigned any bugs. Like the previous dashboards, this page was written in Javascript, HTML and CSS. Dietrich's target audience can benefit by briefly checking their Bugzilla username on the site, and if present, clicking the link that leads straight to their assigned bugs. 

###[L10n-Triage](http://pike.github.com/late-l10n-triage/), [beta dash](http://pike.github.com/beta-dash/), [l10n dash in wiki](https://l10n.mozilla.org/bugs/) by Axel
Axel's contribution to Mozilla's localization community proves beneficial, in terms of tracking localization bugs and their activities. The three dashboards, implemented using Javascript, present different information related to localization bugs, so users can choose to use each one depending on their purposes. 

#### [L10n-Triage](http://pike.github.com/late-l10n-triage/)
L10n-Triage retrieves bugs for Boot2Gecko with the keywords 'late-l10n' and visualizes the daily total number of bugs. Besides that, all bugs amounting up to the total are listed with the functionality to order by ID, summary, resolution, last fixed date, filed date, late-l10n date, and basecamp status. For Boot2Gecko contributors, this application is certainly a minimal yet sufficient replacement for bug searching and analysis. 

#### [Beta Dash](http://pike.github.com/beta-dash/)
A day-to-day visualized localization bug activity, with the options to filter by locale and/or modifier/commenter. The page is designed in a very simple manner, where the main focus is the visualization, and filtering options are located at the sidebar. For ease of characterization, Axel even made the effort of assigning different coloured text to each locale. 

#### [L10n Dash in Wiki](https://l10n.mozilla.org/bugs/)
Displays the number of open bugs for each locale in Mozilla's wiki. Each link 

###[Socorro Releases](https://wiki.mozilla.org/Socorro:Releases) by Chris Lonnen
As the name suggests, this is a page for tracking Socorro Releases. The page provides necessary information for each release, ie. scheduled release date, freeze date and current status; while listing useful links for more detailed information (bugs list, build link, crash statistics). I would say this page is mainly used internally among the Socorro team, where all the useful links can be found. Hosted in Mozilla's wiki, the design adopts Mozilla's standard wiki page, with information neatly arranged in tables. I have yet to ask Chris about the automation process of this dashboard.

If there's one thing I learnt from my honour's thesis, it is the importance of a thorough survey of related works done by others. I have kept a comparison table to summarize the differences and any requirements/design that can be adopted from these dashboards, and will continue updating it with others that I can find. Hope my next post will be about starting the dashboard!
