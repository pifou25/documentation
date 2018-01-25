Everspring Miniplug Dimmer - AD147-6
====================================

\

-   **The module**

\

![module](../images/everspring.AD147-6/module.jpg)

\

-   ** The Jeedom **

\

![vuedefaut1](../images/everspring.AD147-6/vuedefaut1.jpg)

\

summary
------

\

The Mini Inverter Socket is designed to control the ignition and
extinguishing the luminaires and electrical equipment of your
House. It also allows a dimmer function that is compatible
only with the bulbs. With a voltage of 220 - 240 V, this
Dimmer socket can support a load of 6 W at 250 W.

The Mini Dimmer Socket is a Z-Wave ™ compatible device that is
designed to work with all Z-Wave ™ compatible networks. She
can be controlled by remote control, PC software, or any
which Z-Wave controller on your network.

\

functions
---------

\

-   Order a lamp remotely

-   Plug module integrating directly between an electrical outlet and
    the charge to order

-   ON / OFF function and Dimmer to control lamps

-   Local load control via integrated button

-   Z-Wave Plus Technology

-   Reduced dimensions to go almost unnoticed

-   Status LED on integrated button

-   Z-Wave repeater function

\

Technical characteristics
---------------------------

\

-   Module Type: Z-Wave Receiver

-   Power supply: 230 V, 50 Hz

-   Consumption: 0.6W

-   Maximum power: Resistive load: 250W, Incandescent bulb
    : 250W, Led bulb (not dimmable): 6W

-   Frequency: 868.42 Mhz

-   Range: up to 70 m outdoors, up to 30 m in buildings

-   Display: LED on the button

-   Dimensions: Length (socket included): 74mm Diameter: 52mm

\

Module data
-----------------

\

-   Brand: Everspring

-   Name: Miniplug Dimmer

-   Manufacturer ID: 96

-   Product type: 3

-   Product ID: 3

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

![inclusion](../images/everspring.AD147-6/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/everspring.AD147-6/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/everspring.AD147-6/commandes.jpg)

\

Here is the list of orders:

\

-   Intensity: This is the command to adjust the intensity of the
    taking

-   On: This is the command that turns on the plug

-   Off: This is the command that turns off the plug

-   Status: This is the order that allows to know the status of the
    taking

\

Note that on the dashboard, the information State, ON / OFF, Intensity
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
Settings)

\

![Config1](../images/everspring.AD147-6/config1.jpg)

\

Parameter details:

\

-   1: This parameter sets the status value command, it is not
    advised to change this value.

-   2: This parameter sets the delay time of the state change to
    group 1 (value between 3 and 25 seconds)

-   3: This parameter defines whether the socket will resume its status
    (ON or OFF) after a power recovery.

-   4: This parameter defines whether the plug will operate in
    variation or in on / off mode

### Groups

\

This module has 2 association groups.

\

![Groupe](../images/everspring.AD147-6/groupe.jpg)

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

Wakeup
------

\

No notion of wakeup on this module.

\

F.A.Q.
------

\

Yes it is parameter 2 and it can not be set below 3
seconds.

\

** @ ** sarakha63
