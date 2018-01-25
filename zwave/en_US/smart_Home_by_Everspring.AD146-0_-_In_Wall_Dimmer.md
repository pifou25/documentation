SmartHome by Everspring In Wall Dimmer - AD146-0
================================================

\

-   **The module**

\

![module](../images/smarthomebyeverspring.AD146-0/module.jpg)

\

-   ** The Jeedom **

\

![vuedefaut1](../images/smarthomebyeverspring.AD146-0/vuedefaut1.jpg)

\

summary
------

\

This Wall Dimmer Micromodule of the brand SmartHome Europe by
Everspring is designed to control the switching on and off of
lighting fixtures and electrical equipment in your home. he can
also provide a dimmer function that is only
compatible with the bulbs. At a voltage of 230V, this module can
support up to 300 Watts in resistive or incandescent charge, or 200
Fluorescent charge Watts.

It can be used in 2-wire mode (without neutral), replacing a
existing switch, or three wires with a conventional power supply
module (Phase + Neutral).

The Wall Dimmer Module is a Z-Wave ™ compatible device that is
designed to work with all Z-Wave ™ compatible networks. he
can be controlled by remote control, PC software, or any
which Z-Wave controller on your network.

\

functions
---------

\

-   Control lighting / device remotely

-   Installs behind an existing switch

-   ON / OFF function and dimming

-   Low energy consumption

-   Very small, small dimensions

-   Long range antenna

-   Z-Wave Plus Technology

-   Easily installs in a standard flush-mounting box

-   Use in 2-wire mode (neutral not necessary)

-   Compatible with Led Dimmable bulbs

-   Button to include / exclude / associate module

-   Z-Wave repeater function

\

Technical characteristics
---------------------------

\

-   Module Type: Z-Wave Receiver

-   Power supply: 230 V, 50 Hz

-   Consumption: 0.5W

-   Maximum power:

-   Resistive load: 300W

-   Incandescent bulb: 300W

-   Compact fluorescent bulb: 200W

-   Frequency: 868.42 Mhz

-   Range: up to 70 m outdoors, up to 30 m in buildings

-   Display: LED on the button

-   Dimensions: 42mm x 43mm x 16mm

\

Module data
-----------------

\

-   Brand: SmartHome by Everspring

-   Name: In Wall Dimmer

-   Manufacturer ID: 96

-   Product type: 3

-   Product ID: 2

\

Configuration
-------------

\

To configure the OpenZwave plugin and know how to put Jeedom in
inclusion refer to this
[Documentation] (https://jeedom.fr/doc/documentation/plugins/openzwave/fr_FR/openzwave.html).

\

> ** Important **
>
> To put this module in inclusion mode you have to press 3 times on its
> button, according to its paper documentation. It's important to
> note that this module is directly included when
> does not belong to any network and is powered

\

![inclusion](../images/smarthomebyeverspring.AD146-0/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/smarthomebyeverspring.AD146-0/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/smarthomebyeverspring.AD146-0/commandes.jpg)

\

Here is the list of orders:

\

-   Intensity: This is the command to adjust the intensity of the
    light

-   On: This is the command that turns on the light

-   Off: This is the command that turns off the light

-   Status: This is the command that allows to know the status of the
    light

\

To note that on the dashboard, the infos State, ON / OFF, intensity
find on the same icon.

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

![Config1](../images/smarthomebyeverspring.AD146-0/config1.jpg)

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

-   5: This parameter defines whether the switch will operate in
    variation mode or on / off mode

### Groups

\

This module has 2 association groups.

\

![Groupe](../images/smarthomebyeverspring.AD146-0/groupe.jpg)

\

> ** Important **
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

![vuewidget](../images//smarthomebyeverspring.AD146-0/vuewidget.jpg)

\

Wakeup
------

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

** @ ** sarakha63
