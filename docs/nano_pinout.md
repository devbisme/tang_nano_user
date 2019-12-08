---
layout: page
title: Nano Board Pinout
description: FPGA pin connections on the Tang Nano board.
tags: [Tang Nano, FPGA, Sipeed, GOWIN, home]
---

Before you can go somewhere new, you gotta know where you are.

In the [previous post]({{site.url}}/testing_it_out), I compiled and downloaded
an existing example design to verify that the GOWIN EDA software was working.
But to create new designs of your own, you'll need to know what the pins
of the FPGA are connected to on the Nano board.
(For example, what FPGA pins are connected to the two pushbuttons?)
That information is contained in the [Nano board schematic](http://dl.sipeed.com/TANG/Nano/HDK/Tang-NANO-2704(Schematic).pdf),
but getting it in a useful form requires you to trace the wiring from the FPGA pins to other parts on the board.
Even with a small schematic, that's more painful than it should be.

To make it a bit easier, I created a [spreadsheet](https://github.com/xesscorp/tang_nano_user/blob/master/Sipeed_Tang_Nano/HDK/pinout.xlsx)
that lists where the FPGA pins are connected.
It also includes a [board image]({{site.url}}/images/nano_pinout/pinout.png)
showing where the FPGA pins exit the board through the 0.1"-spaced prototyping headers.

<img src="{{site.url}}/images/nano_pinout/pinout.png" width="600"/>


* **[Prev: Testing It Out]({{site.url}}/testing_it_out)**
* **[Next: LED + Button]({{site.url}}/led_btn)**
