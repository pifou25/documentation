Aeotec Minimote
===============

\

-   **The module**

\

![module](../images/aeotec.minimote/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/aeotec.minimote/vuedefaut1.jpg)

\

summary
------

\

This Aeon Labs mini controller is compatible with a wide variety of
Z-Wave modules such as switches, dimmers,
movement, switches for blinds ... So you can order at
distance your lights, appliances or shutters. With this
remote control, you will also be able to include / exclude modules from
your Z-Wave network and associate scenes with the buttons of the
remote control. A sliding flap conceals the buttons allowing
set up the Z-Wave network.

\

functions
---------

\

-   Z-Wave network configuration (inclusion / exclusion of modules)

-   Allows driving up to 4 scenes

-   8 keys: 4 for scenes, 4 for network setting

-   On / off and dimming functions

-   ALL ON / ALL OFF function

-   Internal battery re-chargeable on USB

-   Firmware update via USB

\

Technical characteristics
---------------------------

\

-   Module Type: Z-Wave Controller

-   White colour

-   Power supply: Internal rechargeable battery via USB

-   Display: blue and red LED

-   Frequency: 868.42MHz

-   Range: up to 30 m

-   Dimensions: 0.8cm x 3.3cm x 9.3cm

-   Operating temperature: -35 to +85 ° C

\

Module data
-----------------

\

-   Brand: Aeotec

-   Name: Minimote

-   Manufacturer ID: 134

-   Product type: 1

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
> To put this module in inclusion mode, press the button
> LEARN, in accordance with its paper documentation.

\

![inclusion](../images/aeotec.minimote/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/aeotec.minimote/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/aeotec.minimote/commandes.jpg)

\

Here is the list of orders:

\

-   Buttons: this is the command that will move up the button

1: Button 1 short press

2: Button 1 long press

3: Button 2 short presses

4: Button 2 long presses

5: Button 3 short presses

6: Button 3 long presses

7: Button 4 short presses

8: Button 4 long presses

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

![Config1](../images/aeotec.minimote/config1.jpg)

\

Parameter details:

\

-   241: operating mode of button 1 (leave by default)

-   242: operating mode of button 2 (leave by default)

-   243: operating mode of button 3 (leave by default)

-   244: operating mode of button 4 (leave by default)

-   250: operating mode of the remote control (absolutely leave
    Scene for use in remote control)

\

### Groups

\

This module has four association groups, none are needed
to use it as a remote control in Jeedom.

\

![Groupe](../images/aeotec.minimote/groupe.jpg)

\

Good to know
------------

\

### Specificities

Wakeup
------

\

To wake up this module there is only one way to proceed:

-   stay pressed for 3 seconds on the LEARN button

\

F.A.Q.
------

\

This module wakes up by pressing and holding the LEARN button for 3 seconds.

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
