Fibaro Opening detector - FGK-101
======================================

\

-   **The module**

\

![module](../images/fibaro.fgk101-DS18B20/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/fibaro.fgk101-DS18B20/vuedefaut1.jpg)

\

summary
------

\

This Z-Wave powered battery powered detector has a sensor
reed, a magnetically operated proximity switch, which
detect the opening of a door or window when
two elements are far apart.

The device consists of a part with a magnet (the part
movable), fixed on the door or window, as well as the unit
main position on the fixed part of the window / door with
screw or an adhesive. When the two parties are no longer in front, a
Z-Wave radio signal is automatically sent.

In addition, this detector has an analog input allowing
connect a 1-Wire DS18B20 temperature probe. This detector has
also a wired input, so it can be used as a
universal transmitter: leave out its magnetic contact, and
connect its screw inputs to any detector (normally closed) of your
choice such as a smoke, gas or carbon monoxide detector,
etc.

A Z-Wave controller (remote control, dongle ...) is necessary in order
to integrate this detector into your network if you already have a network
existing.

\

functions
---------

\

-   Opening detector

-   Button to include / exclude the detector

-   Low battery detection

-   Tamper protection

-   1 potential-free wired input

-   1 analog input 1-wire (to connect a probe of
    temperature DS18B20)

-   Very small, small dimensions

-   Ease of use and installation

\

Technical characteristics
---------------------------

\

-   Module type: Z-Wave transmitter

-   Color: White (FGK-101/102/103/104/105/106/107 depending on color)

-   Power supply: ER14250 (1 / 2AA) 3.6V battery

-   Frequency: 868.42 Mhz

-   Transmission distance: 50m free field, 30m indoor

-   Dimensions: 76 x 17 x 19 mm

-   Operating temperature: 0-40 ° C

\

Module data
-----------------

\

-   Brand: Fibar Group

-   Name: Fibaro FGK-101 with temperature sensor (DS18B20)

-   Manufacturer ID: 271

-   Product Type: 1792

-   Product ID: 4096

\

Configuration
-------------

\

To configure the OpenZwave plugin and know how to put Jeedom in
inclusion refer to this
[Documentation] (https://jeedom.fr/doc/documentation/plugins/openzwave/fr_FR/openzwave.html).

\

> **Important**
>
> To put this module in inclusion mode you have to press 3 times on the
> inclusion button, according to its paper documentation.

\

![inclusion](../images/fibaro.fgk101-DS18B20/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/fibaro.fgk101-DS18B20/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/fibaro.fgk101-DS18B20/commandes.jpg)

\

Here is the list of orders:

\

-   State: it is the order which will go up the open or closed state of the
    module

-   Battery: it is the command which makes it possible to raise the state of the
    drums

\

You can hide or show these commands as you wish.

\

### Module configuration

\

> **Important**
>
> During a first inclusion always wake up the module just after
> inclusion.

\

Then if you want to configure the module accordingly
of your installation, you have to go through the button
"Configuration" of Jeedom's OpenZwave plugin.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

You will arrive on this page (after clicking on the tab
Settings)

\

![Config1](../images/fibaro.fgk101-DS18B20/config1.jpg)

![Config2](../images/fibaro.fgk101-DS18B20/config2.jpg)

\

Parameter details:

\

-   Wakeup: this is the wakeup interval of the module (value
    recommended 7200)

-   1: Set the alarm cancellation time for the IN input
    (dry contact)

-   2: allows you to choose whether the blue led should blink on opening and
    closing your door for example

-   3: defines the contact type connected to the terminal block (IN)

-   5: Do not change this setting unless you know why
    (defines the type of signal sent to association group 1)

-   7: value sent to association group 1

-   9: Set the sending of the cancel signal between the IN input
    and the association group 1

-   12: Adjusts the sensitivity to the temperature change (if
    a 1-wire probe is connected to the module)

-   13: Set the broadcast mode send of the broadcast signals
    temperature and tamper

-   14: Activate the scene activation feature

\

### Groups

\

This module has three association groups, only the third is
essential.

\

![Groupe](../images/fibaro.fgk101-DS18B20/groupe.jpg)

\

Good to know
------------

\

### Specificities

\

> **Tip**
>
> This module is very capricious on the wakeup and requires a very
> close proximity to the controller when it is included

\

### Alternative visual

\

![vuewidget](../images/fibaro.fgk101-DS18B20/vuewidget.jpg)

\

Wakeup
------

\

To wake up this module there is only one way to proceed:

-   press the inclusion button 3/4 times. It may be necessary
    to do it several times in a row (2 or 3)

\

F.A.Q.
------

\

This module wakes up by pressing 3 times on one of the tamper buttons. But
the other tamper button must be depressed.

\

This module has a very small scope. It is advisable to do
inclusion in the closest to your box.

\

This module is a battery module, the new configuration will be
taken into account at the next wakeup.

\

Important note
---------------

\

> **Important**
>
> You have to wake up the module: after its inclusion, after a change
> of the configuration, after a wakeup change, after a
> change of association groups

\

**@** sarakha63
