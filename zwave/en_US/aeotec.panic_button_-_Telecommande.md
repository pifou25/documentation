Aeotec Panic Button
===================

\

-   **The module**

\

![module](../images/aeotec.panicbutton/module.jpg)

\

-   ** The Jeedom **

\

![vuedefaut1](../images/aeotec.panicbutton/vuedefaut1.jpg)

\

summary
------

\

This keychain remote control with a modern and pleasant design has a
button to control any type of Z-Wave devices such as
lamps, blinds, etc.

With its very small dimensions, you can easily put it
in your pocket. Easy to use and elegant, it is equipped with a
ring to attach to keys, making it available at
time to leave home or when returning to your home.

The button allows you to control two devices or scenes thanks to the
management of short and long supports. This remote control can also be
well used as the main controller that secondary.

This remote control can also be used as a button
emergency or panic. In case of distress or when its holder
faced with another emergency, simply press
the button and a Z-Wave signal will be emitted. In this case, this device
can also be used as a medallion around the neck.

\

functions
---------

\

-   Keychain remote control

-   Primary or secondary controller

-   Ultra compact and ultra design

-   1 configurable button

-   Manage up to 2 devices / scenes

-   Can be used as an emergency / panic button

-   Use around the neck as an emergency medallion

\

Technical characteristics
---------------------------

\

-   Module type: Z-Wave transmitter

-   Power supply: 1 x CR2450 3V Lithium battery

-   Battery life: 2 to 3 months for 10 to 20 uses
    per day

-   Frequency: 868.42 MHz

-   Transmission distance: 30m indoors

-   Dimensions: 55 x 30 x 11mm (L x W x H)

\

Module data
-----------------

\

-   Brand: Aeotec

-   Name: Panic Button

-   Manufacturer ID: 134

-   Product type: 1

-   Product ID: 38

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

![inclusion](../images/aeotec.panicbutton/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/aeotec.panicbutton/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/aeotec.panicbutton/commandes.jpg)

\

Here is the list of orders:

\

-   Buttons: this is the command that will move up the button

1: Short press button

2: Long press button

\

### Module configuration

\

> ** Important **
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

![Config1](../images/aeotec.panicbutton/config1.jpg)

\

Parameter details:

\

-   250: operating mode of the remote control (absolutely
    Scene for use in remote control)

-   255: Resets the Keyfob from the factory

\

### Groups

\

This module has a single and unique association group. It is
essential.

\

![Groupe](../images/aeotec.panicbutton/groupe.jpg)

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
