Aeotec Keyfob
=============

\

-   **The module**

\

![module](../images/aeotec.keyfob/module.jpg)

\

-   ** The Jeedom **

\

![vuedefaut1](../images/aeotec.keyfob/vuedefaut1.jpg)

\

summary
------

\

Aeon Labs keychain remote control with a modern and pleasant design
has 4 buttons to control any type of devices
Z-Wave such as lamps, blinds, etc ...

With its very small dimensions, you can easily put it
in your pocket. Easy to use and elegant, it is equipped with a
ring to attach to keys, making it available at
time to leave home or when returning to your home.

Each button allows you to control two devices or scenes thanks to
management of short and long supports. This remote control can also be
well used as the main controller that secondary.

\

functions
---------

\

-   Keychain remote control

-   Primary or secondary controller

-   Ultra compact and ultra design

-   4 configurable buttons

-   Manage up to 8 devices / scenes

-   Sliding protective shutter

-   Ease of use and installation

\

Technical characteristics
---------------------------

\

-   Module type: Z-Wave transmitter

-   Power supply: 1 x CR2450 3V Lithium battery

-   Battery life: 1 year

-   Frequency: 868.42 MHz

-   Transmission distance: 100m in free field

-   Operating temperature: -10 ° C to 50 ° C

-   Dimensions: 55 x 30 x 13mm (L x W x H)

\

Module data
-----------------

\

-   Brand: Aeotec

-   Name: Key Fob

-   Manufacturer ID: 134

-   Product type: 1

-   Product ID: 22

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
> To put this module in inclusion mode, press the button
> LEARN, in accordance with its paper documentation.

\

![inclusion](../images/aeotec.keyfob/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/aeotec.keyfob/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the modules will be
available.

\

![Commandes](../images/aeotec.keyfob/commandes.jpg)

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

> ** Important **
>
> During a first inclusion always wake up the module just after
> inclusion.

\

Then if you want to perform the configuration of the module according
of your installation, you have to go through the button
"Configuration" of Jeedom's OpenZwave plugin.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

You will arrive on this page (after clicking on the tab
Settings)

\

![Config1](../images/aeotec.keyfob/config1.jpg)

\

Parameter details:

\

-   250: operating mode of the remote control (absolutely
    Scene for use in remote control)

All other parameters are only useful in case of direct association
between the remote control and modules.

\

### Groups

\

This module has a single and unique association group. It is
essential.

\

![Groupe](../images/aeotec.keyfob/groupe.jpg)

\

Good to know
------------

\

### Specificities

To use this module as a remote control, proceed as follows:

-   1: Include the remote control

-   2: Wake up the remote

-   3: Change the parameter 250 to true (do it even if it is
    already appears to true)

-   4: Wake up the remote control and make sure the change has been
    taken into account

-   5: Change the operating mode of the remote control while remaining
    press the two buttons on the back for 3 seconds.

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

> ** Important **
>
> You have to wake up the module: after its inclusion, after a change
> of the configuration, after a wakeup change, after a
> change of association groups

\

** @ ** sarakha63
