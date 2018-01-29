Nodon Switch - Wall Switch
================================

\

-   **The module**

\

![module](../images/nodon.wallswitch/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/nodon.wallswitch/vuedefaut1.jpg)

\

summary
------

\

The NodOn® wall switch can directly control any
Z-Wave® or Z-Wave Plus® compatible device such as
intelligent NodOn® or even trigger scenes via a central
home automation compatible.

The switch has a mounting plate for easy mounting
in the house: using the screws of a recessing pot,
screwing to the wall, or simply sticking it through the adhesives
double-sided present on the back of the turntable.

\

functions
---------

\

-   Control alone or with a home automation system

-   Easy to assemble and disassemble

-   Feeling of pleasant support

-   Wireless

-   2 years of battery

\

Technical characteristics
---------------------------

\

-   Power supply: CR2032 battery - Autonomy 1,5 - 2 years

-   4 buttons

-   Double-sided adhesive wall mounting (included) or screws (not included)

-   Operating temperature: 0 ° C to 40 ° C

-   Altitude: 2000m

-   Z-Wave® Radio Protocol: 868.4MHz - 500 Series - Z-Wave Compatible
    SDK 06.51.06

-   Range: 40m indoor / 70m outdoors

-   Dimensions: 80 \ * 80 \ * 15mm

-   2 years warranty

-   EN 60950-1: 2006 + A11: 2009 + A1: 2010 + A12: 2011 + A2: 2013

-   EN 300 220-2 V2.4.1

-   EN301 489-1 V1.9.2

-   EN301 489-3 V1.6.1

-   EN 62479: 2010

\

Module data
-----------------

\

-   Brand: Nodon

-   Name: CWS-3-1-01 Wall Switch

-   Manufacturer ID: 357

-   Product type: 2

-   Product ID: 3

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

![inclusion](../images/nodon.wallswitch/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/nodon.wallswitch/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the modules will be
available.

\

![Commandes](../images/nodon.wallswitch/commandes.jpg)

\

Here is the list of orders:

\

-   Buttons: this is the command that will move up the button

+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| Buttons | Support | Long Support | Relachement | Double support |
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

![Config1](../images/nodon.wallswitch/config1.jpg)

\

Parameter details:

\

-   1-2: To choose the profile of the buttons in case of use in
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

![Groupe](../images/nodon.wallswitch/groupe.jpg)

![Groupe](../images/nodon.wallswitch/groupe2.jpg)

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
    wake up 1 or 2 times after inclusion. And check the
    association group.

\

Wakeup
------

\

To wake up this module just press one of these buttons

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
