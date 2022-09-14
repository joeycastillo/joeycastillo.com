---
title: LCD FeatherWing
date: 2022-06-28
---
The LCD FeatherWing is a low power display module compatible with Adafruit’s Feather line of development boards. After three years of learning product design and electrical engineering, I believe this little gadget represents my most mature design to date. It's a simple, streamlined design with a custom LCD, optimized for low BOM cost and easy manufacturability. By plugging in to the Feather ecosystem, I also felt confident that it would find market fit relatively quickly.

<!--more-->

Visit oddlyspecificobjects.com for [more information about the LCD FeatherWing](https://www.oddlyspecificobjects.com/products/lcdwing/), or [buy one at Adafruit](https://www.adafruit.com/product/5581)!

{{< image src="/images/objects-lcdwing-angle-01.jpg" alt="Photo: a grid of LCD FeatherWings displaying different kinds of information" position="left" >}}

I'm fond of saying that this is an object that exists because of Adafruit's ecosystem. What I know about electrical engineering, I learned from reading Adafruit's guides and hacking on Adafruit's products. The BU9796 I²C LCD driver at the heart of the LCD FeatherWing was featured in a Sunday night Desk of Ladyada video. Moreover, just watching the way they designed gadgets and getting into their schematics taught me how to design for manufacturability and testing — and I put all those lessons to work when designing the wing.

The part count on this device is deliberately low: five surface mount components, plus the LCD and two rows of through-hole pin header. This keeps the BOM cost low, allowing me to hit an affordable price point while maintaining ample margin to make it make sense financially. The low part count also means I can give the surface mount parts ample courtyard, instead of jamming them together as I did with [Sensor Watch](/objects/sensorwatch). This design choice leads to higher manufacturing yields: out of more than 200 boards tested so far, I have only experienced one QA failure — a yield of over 99%.

{{< image src="/images/objects-lcdwing-display.svg" alt="Diagram of the LCD design" position="center" style="width: 66%; background-color: white" >}}

Finally, after years of experience having my own PCBs fabricated, I felt confident enough to take the plunge and have my own custom LCD fabricated. This was a big step, and something I wouldn't have dreamed possible when I began this Oddly Specific journey. This custom LCD allows for very versatile use cases, as demonstrated above, while maintaining the excellent low power characteristics of a simple, low-duty segment LCD.

All told, when the I²C bus is inactive, you can expect the LCD FeatherWing to add no more than a dozen microamperes to your project while maintaining an always-on display. This makes it ideal for a clock, countdown timer or passive information display. It also makes it a great fit for battery-powered or solar applications that require a control panel or settings interface, but don't want to add a power-hungry OLED or TFT to the power budget.
