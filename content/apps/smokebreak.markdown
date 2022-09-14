---
title: SmokeBreak
date: 2012-06-24
---

SmokeBreak was an iPhone, iPod Touch and Android app for helping smokers track and control their smoking habit or help them quit. It was designed to be non-judgmental and fun.

<!--more-->

{{< figure src="/images/apps-smokebreak-icon.png" alt="Icon: six cigarettes lined up vertically against a gray background" position="left" caption="The SmokeBreak icon" captionPosition="left" >}}

## History

SmokeBreak was conceived in the summer of 2010. It launched in October 2010 and quickly gained traction; within a month it was featured in Apple's **What's Hot in Healthcare and Fitness** in the U.S. and Czech App Stores; and after a localization to Spanish, quickly climbed to be one of the **top 10 healthcare and fitness apps in Spain**.

SmokeBreak was discontinued in June of 2012. It ended its life with 75,000 downloads across all platforms, a four-star average rating in the Android app store, and a five-star average rating in the iPhone App Store.

## Art Direction

After researching existing smoking-related apps in the App Store, a disheartening lack of design sense was evident. Several apps featured poorly lit photographs of ashtrays or cigarettes; others had confusing, poorly designed UI elements. It was clear that a beautiful, usable design would separate SmokeBreak from the pack.

{{< image src="/images/apps-smokebreak-screenshot-1.jpg" alt="The SmokeBreak app's goal interface. It asks if you want to limit your smoking, smoke less, quit smoking or stay quit." position="center" style="width: 33.333%; float: left;" >}}
{{< image src="/images/apps-smokebreak-screenshot-2.jpg" alt="The SmokeBreak app's main interface. It shows that the user has smoked seven cigarettes instead of their goal of six. It also shows a seven-day view, with stars for days that the user achieved their goals." position="center" style="width: 33.333%; float: left;" >}}
{{< image src="/images/apps-smokebreak-screenshot-3.jpg" alt="A certificate of achievement in the SmokeBreak app, awarded for going three days without a cigarette." position="center" style="width: 33.333%; float: left;" >}}

---

The design was crisp and clean, eschewing gaudy colors and aiming for a more subdued, cool monochrome tone overall, with color reserved for the buttons and awards.

The title was set in Gotham Rounded, a Hoefler & Frere-Jones typeface chosen for its friendly affect.

### Information Design

How should we visualize information about the user's smoking habit in a way that encourages them? One way is by using **sparklines** to show the last seven days at a glance.

For a more fun presentation of data, the motif of an elementary-school style "report card" allowed for clear feedback in the form of stars. It also offered encouragement; stars are awarded based on the user's goals: bronze for meeting the goal, silver for being under, and gold for having no cigarettes in a given day.

The app also gave awards for streaks and certain combinations of stars; three stars in a row, for example, earned the "Trifecta Award."

### Resolution Independence

All the artwork was Retina Display ready, and there certainly was a lot of it! Indeed, the 'streak' awards required six groupings of stars, presented in three colors and at three resolutions — a whopping 54 images! Yet by utilizing intelligent workflow in [Opacity Express](http://likethought.com/opacity/), all these images were generated from a single file; tweaking the color of the stars required editing just one variable.

## Technologies Used

### Facebook Integration

SmokeBreak integrated with **Facebook Connect** to allow users to post awards to their walls and share them with friends. The Awards backend was a lightweight Python webapp that stored awards using a REST API. It ran on the **Google App Engine**.

### Localization

SmokeBreak was designed from the ground up for localization, and boasted **full localization** in both English and Spanish. Both the mobile app and the awards backend were localization-aware, so Spanish-speaking users were able to share Spanish-language awards on Facebook without ever setting a preference.

### Local Notifications

One downside of an app that relied on daily user input was that the user may forget to open the app one day. SmokeBreak took care of this by allowing users to set reminders at times they often smoke cigarettes; this was accomplished using the local notifications. The notification also played a **custom notification sound** which was developed in-house.
