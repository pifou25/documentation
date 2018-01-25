Goal
========

You will find here the documentation to install Jeedom on a
raspberry PI 3 ** without microSD card. **

The PI3 offers the possibility to boot directly on a
USB device and thus free yourself from the microSD card sometimes
generating problems (corruption).

** The installation procedure is strictly identical to that on a
microSD card, but it will make sure to own a firmware to
day.**

For this, open an SSH connection. (if you do not know how,
watch the installation on microSD:
[Here] (https://jeedom.github.io/documentation/installation/fr_FR/index.html)
)

    vcgencmd otp_dump | grep 17:

You must get back:

    17: 3020000a

If so, your PI3 is correctly configured to boot on
USB. If he can not find anything, he will normally start on a map
microSD.

If the return is different, you should simply make a change
day.

    sudo apt-get update; sudo apt-get install rpi-update

then

    sudo rpi-update

Then restart the PI3

    sudo reboot

> ** Important **
>
> To avoid power problems, opt for a mSATA SSD drive
> low consumption.

> ** Tip **
>
> You can now install Jeedom by following exactly the same
> procedure with an SD card.
> [Here] (https://jeedom.github.io/documentation/installation/en_US/index.html)

Possible adjustments
=====================

** The following remarks must be taken into account: **

> ** Important **
>
> The following changes are the result of problems encountered by
> users. You must adapt them to your case. The support
> Jeedom does not intervene for problems related to your configuration.

-   ** If you have swap problems, you need to change it. **

    -   ** Increase its size **:

        -   Change the size of the swap by opening this file:

<! - ->

    sudo nano / etc / dphys-swapfile

-   Find the right parameter:

<! - ->

    CONF_SWAPSIZE = 100

-   Change the value of CONF \ _SWAPSIZE to 1024, for example, and then
    restart:

<! - ->

    sudo reboot

-   ** Change the call value to the swap. **

By default, the system calls the swap when there is less than 40% of
Ram.

-   Open the file to change this setting:

<! - ->

    sudo nano /etc/sysctl.conf

-   Add this line, to ask the Pi3 to use the swap only
    when 10% of available memory remains (100 MB of
    Ram available):

<! - ->

    vm.swappiness = 10

-   Then restart:

<! - ->

    sudo reboot

-   ** Disable bluetooth built-in as incompatible with the card
    GPIO zwave.me **

    -   Open the file concerned:

<! - ->

    sudo nano /boot/config.txt

-   add the line:

<! - ->

    dtoverlay = ft3-disable-bt

-   Make a clean stop

<! - ->

    sudo halt

-   Unplug reconnect (no sudo reboot!).


