SmartHome by Everspring In Wall On Off - AN179-0
================================================

\

-   **The module**

\

![module](../images/smarthomebyeverspring.AN179-0/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/smarthomebyeverspring.AN179-0/vuedefaut1.jpg)

\

summary
------

\

The ON / OFF Wall Micromodule from SmartHome Europe by Everspring,
is designed to control the switching on and off of luminaires and
electrical appliances in your home. Two sets of dry contacts
allow the connection of two switches.

For security purposes, the unit can detect overheating and extinguish
directly relay to avoid any damage. At a voltage of 230
V, this module can support up to 11A resistive load, 1200 Watts
incandescent, 700 Watts of motor, or 320 Watts (8 x 40 Watts) of
fluorescent charge.

The ON / OFF Wall Micromodule is a Z-Wave ™ compatible device that is
designed to work with all Z-Wave ™ compatible networks. he
can be controlled by remote control, PC software, or any
which Z-Wave controller on your network.

\

functions
---------

\

-   Control lighting / device remotely

-   Installs behind an existing switch

-   ON / OFF function

-   Low energy consumption

-   Very small, small dimensions

-   Long range antenna

-   Z-Wave Plus Technology

-   Easily installs in a standard flush-mounting box

-   Button to include / exclude / associate module

-   Z-Wave repeater function

\

Technical characteristics
---------------------------

\

-   Module Type: Z-Wave Receiver

-   Power supply: 230 V, 50 Hz

-   Consumption: 0.5W

-   Maximum power: Resistive load: 2500W Incandescent bulb
    : 1200W Compact Fluorescent Light Bulb: 320W

-   Frequency: 868.42 Mhz

-   Range: up to 70 m outdoors, up to 30 m in buildings

-   Display: LED on the button

-   Dimensions: 42mm x 43mm x 16mm

\

Module data
-----------------

\

-   Brand: SmartHome by Everspring

-   Name: In Wall On Off

-   Manufacturer ID: 96

-   Product Type: 4

-   Product ID: 8

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
> To put this module in inclusion mode you have to press 3 times on its
> button, according to its paper documentation. It's important to
> note that this module is directly included when
> does not belong to any network and is powered

\

![inclusion](../images/smarthomebyeverspring.AN179-0/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/smarthomebyeverspring.AN179-0/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/smarthomebyeverspring.AN179-0/commandes.jpg)

\

Here is the list of orders:

\

-   On: This is the command that turns on the light

-   Off: This is the command that turns off the light

-   Status: This is the order that allows to know the status of the
    light

\

Note that on the dashboard, state, ON / OFF information is found on
the same icon.

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

![Config1](../images/smarthomebyeverspring.AN179-0/config1.jpg)

\

Parameter details:

\

-   1: This parameter sets the status value command, it is not
    advised to change this value.

-   2: This parameter sets the delay for sending the state change to
    group 1 (value between 3 and 25 seconds)

-   3: This parameter defines whether the switch will resume its
    status (ON or OFF) after a power recovery.

-   4: This parameter defines the type
    switch (push / bistable)

### Groups

\

This module has 2 association groups.

\

![Groupe](../images/smarthomebyeverspring.AN179-0/groupe.jpg)

\

> **Important**
>
> At least Jeedom should be in group 1 \

Good to know
------------

\

### Specificities

\

-   Status feedback can not be set below 3
    seconds. \

### Alternative visual

\

![vuewidget](../images//smarthomebyeverspring.AN179-0/vuewidget.jpg)

\

Wake up
-------

\

No concept of wake up on this module.

\

F.A.Q.
------

\

Yes it is parameter 2 and it can not be set below 3
seconds.

\

No. this module can be included or excluded by pressing several times
on the switch.

\

**@** sarakha63
