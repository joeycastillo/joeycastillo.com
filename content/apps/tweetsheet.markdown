---
title: TweetSheet
date: 2010-04-01
---

TweetSheet was an app for downloading your Twitter history to your iPhone, iPad or iPod Touch, and letting you search your past. It existed in both a paid "Pro" version and a free "Lite" version.

<!--more-->

{{< figure src="/images/apps-tweetsheet-icon.png" alt="Icon: a magnifying glass over horizontal lines, with a wood trim on top." position="left" caption="The TweetSheet icon" captionPosition="left" >}}

## History

The Twitter service and many of the apps built around it seemed focused on determining what's happening now. TweetSheet built on a different insight: by answering again and again the question, "What are you doing?" Twitter users assemble a rich set of information about their past. This information can speak not just to who we are and what we are doing, but also to who we were and what we have done.

At the time, Twitter's native search feature was limited to searching a user's most recent 3,000 tweets. Rather than lose their history behind that horizon, TweetSheet let users download it all to their phone.

TweetSheet was launched in the spring of 2010, and received updates to add functionality (retweets and adjustable font sizes), and to support Twitter's OAuth switchover. It was discontinued in June of 2012, as Twitter began offering improved tools for account backup and archive.


## Art Direction

{{< image src="/images/apps-tweetsheet-screenshot-phone-1.jpg" alt="Screehshot: TweetSheet for iPhone, main interface. A list of tweets." position="center" style="width: 33%; float: left;" >}}
{{< image src="/images/apps-tweetsheet-screenshot-phone-2.jpg" alt="Screehshot: TweetSheet for iPhone, search interface showing tweets related to the search term, Thanksgiving." position="center" style="width: 33%; float: left;" >}}
{{< image src="/images/apps-tweetsheet-screenshot-phone-3.jpg" alt="Screehshot: TweetSheet for iPhone, detail interface showing a single tweet and the timeline before and after." position="center" style="width: 33%; float: left;" >}}

---

TweetSheet's design intentionally stepped outside of the usual colors and textures employed by iPhone and iPad apps. The design evoked a finely-crafted notebook, with wood-grain texture for the toolbars and a canvas cover. The intent was to create not a sterile table of entries, but rather something that evoked a real object; the goal was to create something that let you touch your history.

{{< image src="/images/apps-tweetsheet-screenshot-pad-1.jpg" alt="Screehshot: TweetSheet for iPad, conversation view, showing a tweet and the replies associated with it." position="center" style="width: 50%; float: left;" >}}
{{< image src="/images/apps-tweetsheet-screenshot-pad-2.jpg" alt="Screehshot: TweetSheet for iPad, map view, showing the location where a tweet was sent." position="center" style="width: 50%; float: left;" >}}

---

TweetSheet was also in the unique position of being in development when the iPad was announced. In order to be a part of the iPad launch, a universal interface was created and tested in the iPad Simulator, and submitted to the App Store before iPads became available to developers. As a result, TweetSheet was available for the iPad on the first day iPads were sold.

## Technologies used

TweetSheet used a custom Python backend, hosted on the [Google App Engine](http://code.google.com/appengine/), to download users' histories. Tests showed that the process of downloading a user's entire history was too network- and processor-intensive to be done on the iPhone itself. Thus, on first run, TweetSheet offloaded the actual download to the server.

For TweetSheet Pro users, the TweetSheet backend sent a push notification when the download process was complete.
