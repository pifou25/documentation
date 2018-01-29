Swiid Switch - Swiidinter
===============================

\

-   **The module**

\

![module](../images/swiid.inter/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/swiid.inter/vuedefaut1.jpg)

\

summary
------

\

SwiidInter is the first cord switch in the environment
Z-Wave home automation that is small enough and discreet enough to be
comparable to an ordinary cord switch.

It can be used both manually as any other
switch on ordinary and remote cord via a controller
Z-Wave.

The SwiidInter switch also offers possibilities for association
and this two-way. So, it can be operated automatically by a
other Z-Wave device on the same network, such as the
triggering a presence detector. Conversely with a support
short or with a long press it can control two separate groups of
Z-Wave devices that have been associated with it: for example, all
other lights in the room where your switch is located
SwiidInter.

The SwiidInter switch installs exactly like a switch
on ordinary cord: it is thus a simple and fast installation which
does not require any specialized tools. It must then be configured to
integrate into a Z-Wave "network", this network can be as simple
only one remote control that controls your SwiidInter switch to
distance.

\

functions
---------

\

-   Cord switch that can be used both manually
    (short press) and radio remote (Z-Wave)

-   Use as a replacement for a standard cord switch
    a bedside lamp, table or desk

-   ON / OFF function

-   Enabling a home automation scenario on long support
    (Z-Wave association)

-   Dimensions comparable to an ordinary cord switch

-   Installs as a regular cord switch

-   Suitable for all types of lamp bulbs

\

Technical characteristics
---------------------------

\

-   Module Type: Z-Wave Receiver

-   Black color

-   Power supply: 230V ± 10% - 50Hz

-   Max power: 660W

-   Consumption: &lt; 0,08W

-   Protection class: IP20

-   Radio protocol: Z-Wave® (SDK 4.55)

-   Radio frequency: 868.42 MHz (US)

-   Dist. transmission: Up to 30m indoors (depends on materials)

-   Temp. operating temperature: 0 - 40 ° C

-   On / off display: blue LEDs

-   Dimensions: 84 x 32 x 29 mm

-   EU standards: EN 61058-2-1: 2011 EN 55015

\

Module data
-----------------

\

-   Brand: Swiid

-   Name: Swiidinter

-   Manufacturer ID: 358

-   Product Type: 256

-   Product ID: 256

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
> To put this module in inclusion mode, press the button
> back, in accordance with its paper documentation

\

![inclusion](../images/swiid.inter/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/swiid.inter/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/swiid.inter/commandes.jpg)

\

Here is the list of orders:

\

-   Status: This is the command that allows to know the status of the
    light

-   ON: This is the command that turns on the light

-   OFF: This is the command that turns off the light

\

Note that on the dashboard all the information is found on the same
icon

\

### Module configuration

\

You can configure the module according to your
installation. To do this, go through the "Configuration" button on the
OpenZwave plugin from Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

You will arrive on this page (after clicking on the tab
settings)

\

![Config1](../images/swiid.inter/config1.jpg)

\

Parameter details:

\

This parameter allows you to choose the behavior when you associate the
swiidinter to another module (long press)

\

-   Inactive: will have no effect on other lights

-   Only OFF: will only be effective to turn off the others
    lights

-   Only ON: will only be effective to turn on others
    lights

-   ON and OFF (fully): will be effective to turn on and off
    other lights

\

### Groups

\

This module has two association groups.

\

![Groupe](../images/swiid.inter/groupe.jpg)

\

> **Important**
>
> For optimum operation of your module. It is necessary that Jeedom
> at least be associated with group 2.

\

Associate with another light
----------------------------

\

To associate the swiidinter with another light and to benefit from
the lighting of another light, just add it to the group
Association 1 via the screen above.

\

Good to know
------------

\

### Alternative visual

\

![vuewidget](../images/swiid.inter/vuewidget.jpg)

\

Wake up
-------

\

No concept of wake up on this module.

\

F.A.Q.
------

\

Did you associate the two modules and did you configure the part
specific.

\

No. The module does not allow it.

\

**@** sarakha63
