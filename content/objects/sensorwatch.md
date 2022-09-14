---
title: Sensor Watch
date: 2022-01-10
---
Sensor Watch is a bridge between eras. It takes an iconic 30-year-old design from a golden age of digital watches, and pairs it with a modern, powerful microcontroller and state-of-the-art sensing capabilities. This small circuit board, less than an inch in diameter, replaces the original quartz movement in a Casio F-91W or A158W watch to put the capabilities of an ultra-low-power ARM Cortex M0+ microcontroller on your wrist.

<!--more-->

{{< image src="/images/objects-sensorwatch-angle-01.png" alt="Photo: the Sensor Watch circuit board next to a Casio F-91W" position="left" >}}

Sensor Watch is both an open source hardware project and a product available for purchase, as well as an attempt to launch a hardware platform from scratch:

* I designed the Sensor Watch circuit board in January 2021.
* In the months following, I built a [low-level library](https://joeycastillo.github.io/Sensor-Watch/) for interacting with the hardware.
* By October I designed [Movement](https://www.sensorwatch.net/docs/movement/), a firmware framework that allowed for community contributions.
* The first community contributions happened in November: a [stopwatch complication](https://github.com/joeycastillo/Sensor-Watch/pull/21) and a [TOTP code generator](https://github.com/joeycastillo/Sensor-Watch/pull/23), both from [Wesley Ellis](https://twitter.com/tahnok).
* That same month, I flew to Augusta, Georgia to [supervise the assembly of 100 boards](https://www.youtube.com/watch?v=6T1hul6tOjA)
* In January 2022 I launched the project [on Crowd Supply](https://www.crowdsupply.com/oddly-specific-objects/sensor-watch), where it garnered over 750 backers and more than 250 preorders.
* I personally [packed and shipped the first 90 backer boards](https://www.crowdsupply.com/oddly-specific-objects/sensor-watch/updates/blue-boards-shipping-check-your-address-green-boards-delayed-and-other-news-of-the-watch) in April 2022.

Along the way I generated copious amounts of documentation, including a [Watch Interface Guidelines](https://www.sensorwatch.net/docs/wig/) document (like Apple's HIG) talking through the unique UX considerations associated with the simple display, limited inputs and low power requirements. I also did marketing, copywriting and [web design](https://www.sensorwatch.net) for the project, as well as the logistics involved in manufacturing and shipping more than 2,000 individually packaged boards during a year of historic parts shortage.

As of September, I am on track to ship the remaining boards by the end of 2022.

## Acknowledgments

Sensor Watch borrowed its board outline from [Pluto, an F-91W board swap from carrotIndustries](https://github.com/carrotIndustries/pluto). It was also deeply inspired by [Travis Goodspeed's Goodwatch](https://github.com/travisgoodspeed/goodwatch/). Finally: I learned of the SAM L22 microcontroller, which makes this whole thing possible, from [Greg Davill's arm-watch](https://twitter.com/GregDavill/status/1335771887750680576); his Advent Calendar of Making in December of 2020 directly inspired me to design Sensor Watch in January of 2021.

Sensor Watch would not exist but for these open hardware projects. Thank you all!