In 90% of cases it is not necessary to force the GSM keys into
GSM only (instead of GSM + CDROM + card reader), the only case
where it's mandatory is if you want to use the key in a
Jeedom on a VM (VMware ESXi). Indeed if you do not pass it in
GSM mode only the key will not appear in the list of
USB devices that you can pass to the VM.

> ** Important **
>
> This tutorial was done on a Windows 10

Installing drivers
========================

Once the key connected to a Windows 10 PC you must have a
new CD-ROM drive. You have to double click on it and install the
software proposed (there is nothing to change do just following the whole
long).

![gsmonly](../images/gsmonly.PNG)

COM port recovery
========================

Then you have to get the number of the communication port. Go to
the "Start" menu and search for "Device Manager", launch
this one and then unfold the part "Ports (COM and LPT)" you should have
an item containing "HUAWEI", then just remember the number of the
COM port:

![gsmonly2](../images/gsmonly2.PNG)

Download Putty
=======================

Then download putty
[here] (https://the.earth.li/~sgtatham/putty/latest/x86/putty.exe) and
launch the downloaded file

Putty configuration and switching to GSM mode only
================================================== =====

Once launched configure putty like this (putting your number correctly
COM port to you, see step above):

![gsmonly3](../images/gsmonly3.PNG)

A black window will appear (from time to time there may be a
"boot ..." message, that's normal, that means you're fine
connected to the GSM key). In this window you must type and press
on the "Enter" key:

    AT ^ u2diag = 0

> ** Important **
>
> Be careful when you go to type the text you will not see anything at
> the screen is normal, the text is still well taken into account.

Normally in return you must have an OK.

That's it. Your key is in GSM mode only and you
can you use it through a VMware now.
