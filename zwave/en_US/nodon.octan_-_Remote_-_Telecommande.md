Nodon Remote Control - Octan
==========================

\

-   **The module**

\

![module](../images/nodon.octan/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/nodon.octan/vuedefaut1.jpg)

\

summary
------

\

The Octan Remote NodOn® can control any receiver
Z-Wave® or Z-Wave Plus® compatible such as remote control jack
NodOn® (Main Controller Mode - Standalone), or trigger
scenes / actions via a compatible home automation system (mode
Gateway)

Its integrated magnet allows it to be fixed everywhere, from the radiator to the door
refrigerator, through its wall bracket. Between remote control
and switch, the Octan Remote revolutionizes the control of objects
household

\

functions
---------

\

-   Control alone or with a home automation system

-   Built-in magnet

-   Led of color

-   Wall Plate

-   2 years of battery

\

Technical characteristics
---------------------------

\

-   Power supply: CR2032 battery - Autonomy 1,5 - 2 years

-   4 buttons

-   Double-sided adhesive wall mount (included) or screws
    (not included)

-   Integrated magnet for fixing on metal surface

-   Operating temperature: 0 ° C to 40 ° C - Altitude: 2000m

-   Z-Wave® Radio Protocol: 868.4MHz - 500 Series - Z-Wave Compatible
    SDK 06.51.01 Range: 40m indoor / 80m outdoor

-   Dimensions: 80 \ * 80 \ * 15mm

-   2 years warranty

\

Module data
-----------------

\

-   Brand: Nodon

-   Name: CRC-3-1-00 Octan Remote

-   Manufacturer ID: 357

-   Product type: 2

-   Product ID: 1

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
> To put this module in inclusion mode you have to press both
> button (1 and 2) until the light turns pink then press
> Button 1, in accordance with its paper documentation.

\

![inclusion](../images/nodon.octan/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/nodon.octan/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/nodon.octan/commandes.jpg)

\

Here is the list of orders:

\

-   Buttons: this is the command that will move up the button

+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| Buttons | Support | Long Support | Relaxation | Double support |
================ ================ + + + =============== = + + ================ ================ +
| **1** | 10 | 12 | 11 | 13 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| **2** | 20 | 22 | 21 | 23 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| **3** | 30 | 32 | 31 | 33 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| **4** | 40 | 42 | 41 | 43 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +

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
settings)

\

![Config1](../images/nodon.octan/config1.jpg)

\

Parameter details:

\

-   1-2: Allows to choose the profiles of the buttons in case of use in
    central (useless for use in Jeedom)

-   3: Important parameter to tell if the switch should work
    in Scene or Central Scene mode (Absolutely Scene)

-   4-7: Select the operating mode of the buttons (in case
    group associations)

-   8: Allows to choose the operating mode of the LED

### Groups

\

This module has 7 association groups.

\

![Groupe](../images/nodon.octan/groupe.jpg)

![Groupe](../images/nodon.octan/groupe2.jpg)

\

-   Group 1 - Lifeline: This group is generally used to
    report information from the Smart Plug to the main controller
    network.

-   Group 2 to 5 - Devices in these groups are controlled by the
    corresponding button according to MONO profile

-   Group 6 to 7 - Devices in these groups are controlled by the
    corresponding button according to DUO profile

\

> **Important**
>
> At least Jeedom should be in group 1 \

Good to know
------------

\

### Specificities

\

-   This module can be capricious on inclusion. Do not hesitate to
    wake up 1 or 2 times after inclusion, and check the
    association group.

\

Wakeup
------

\

To wake up this module just press one of the buttons

\

F.A.Q.
------

\

This module is a module on battery, the new configuration will be
take into account only if you wake up the remote control.

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
