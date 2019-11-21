---
layout: page
title: Where is Everything?
description: Getting Started with the Tang Nano FPGA Board.
tags: [Tang Nano, FPGA, Sipeed, GOWIN, home]
---

I ordered my Tang Nano board from [Seeed](https://www.seeedstudio.com/Sipeed-Tang-Nano-FPGA-board-powered-by-GW1N-1-FPGA-p-4304.html)
and this is what I got:

![](/images/getting_started/seeed_pckg.png)

Yep, that's it: a board and two headers.
No documentation. Not even a link.
Not exactly the friendly introduction to FPGAs you'd hoped for.
So what now?

Well, everything is available on the internet if you look hard enough.
In order to save you the trouble, here's a list of stuff you'll want:

* **[Sipeed Tang Nano Introduction](http://tangnano.sipeed.com/en/)** is Sipeed's intro to their board, complete with broken links and everything!
  It does list the major components of the board.
* **[Tang Nano Schematic](http://dl.sipeed.com/TANG/Nano/HDK/Tang-NANO-2704(Schematic).pdf)** shows how the board's parts are connected.
  This is important for finding out what's connected to the FPGA's pins.
  You can also get a [drawing](http://dl.sipeed.com/TANG/Nano/HDK/Tang-NANO-2704(Assembly%20drawing).pdf) that shows where the parts are
  located on the board if that interests you.
* **[GW1N FPGA Datasheet](http://dl.sipeed.com/TANG/Nano/HDK/GW1N-Datasheet(English)/GW1N%20series%20of%20FPGA%20Products%20Data%20Sheet.pdf)**
  is Sipeed's copy of GOWIN's FPGA datasheet.
  (You can get the same thing [here](https://www.gowinsemi.com/en/document/chkLogin/?a=upload%2Fdatabase_doc%2F178%2Fdocument%2F5da91c1e26c4e.pdf),
  but you'll need to register and then sign in to get it. You even have to pass a CAPTCHA. *Sigh.*) 
* **[GW1N Pinout Spreadsheet](http://dl.sipeed.com/TANG/Nano/HDK/GW1N-Datasheet(English)/GW1N-1%20pinout.xlsx)** lists the pins
  and their functions for all the GW1N-1 FPGA packages.
  The **QN48** column has the pin numbers for the particular FPGA package used on the Nano board. 
* **[GOWIN EDA software](https://www.gowinsemi.com/en/support/download_eda/)** compiles VHDL/Verilog code into bitstreams for the FPGA.
  You need this and you'll *have* to register and sign in to get it.
  There's no way around it (so far).
  While you're there, you might as well get the
  [user manual](https://www.gowinsemi.com/en/document/chkLogin/?a=upload%2Fdatabase_doc%2F379%2Fdocument%2F5dca6a3577b17.pdf).
* **[Licenses](https://www.gowinsemi.com/en/support/license/)** from GOWIN are needed to enable the software.
  Fulfilling your license request may take a while depending upon how many hundreds or thousands of people buy this board.
  As an alternative, you can use Sipeed's [license](http://dl.sipeed.com/TANG/Nano/IDE/gowin.lic),
  their [Synplify license](http://dl.sipeed.com/TANG/Nano/IDE/gowin_Synplifypro.lic),
  and these [instructions](http://dl.sipeed.com/TANG/Nano/IDE/license_readme.txt).
  I'll go over this in more detail below.
* **[Design examples](https://github.com/sipeed/Tang-Nano-examples)** for the Nano board are helpful for getting
  started and verifying that your EDA software is working.

The next step is to install the EDA software and set up the license.
I'm using Windows 10, so I just double-clicked the `Gowin_V1.9.2Beta_win.zip` file and then double-clicked
the `Gowin_V1.9.2Beta_win.exe` installer that was inside:

![](/images/getting_started/EDA_install.png)

I agreed to the license terms and installed in the default location.
After the installation completed, I double-clicked the `Gowin_V1.9.2Beta` icon and the following screen appeared:

![](/images/getting_started/initial_EDA_screen.png)

Next it's time to install the license:

![](/images/getting_started/manage_lic.png)

I received licenses from GOWIN for their software and for Synplify Pro, both of which
I placed in a top-level directory called `.Gowin` (but you can use whatever you like).
I selected the option `Use Local License File` and entered the location of the GOWIN license file.
(I'll ignore the Synplify Pro license for now.)
Then click `Save` and the software is ready to go.

![](/images/getting_started/local_lic.png)

If you haven't got any licenses from GOWIN, Sipeed lets you "borrow" one from their license server.
Just select `Use Floating License Server` and type in the server's IP address
(read Sipeed's [license instructions](http://dl.sipeed.com/TANG/Nano/IDE/license_readme.txt)
to get the most up-to-date IP address).
Then click the `Test Connection` button to see if a valid license has been checked out:

![](/images/getting_started/float_lic.png)

You'll get a `Successed` (sic) message if a valid license was obtained.
Then click `Save` and the software is enabled *for the current session*.
Each time you start the software, it will automatically reach out to the Sipeed
server to get another license.
If you're not connected to the internet or the license server is not available, then
your software won't run.
(That's one reason you might want to get your own local license.)

![](/images/getting_started/float_lic_test.png)

At this point you should have working software that will create bitstreams for the FPGA.
Let's try it out!

**[Next: Testing It Out](/testing_it_out)**
