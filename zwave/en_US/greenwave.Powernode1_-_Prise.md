Greenwave PowerNode - 1 socket
=============================

\

-   **The module**

\

![module](../images/greenwave.Powernode1/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/greenwave.Powernode1/vuedefaut1.jpg)

\

summary
------

\

The PowerNode plug-in module from GreenWave is a smart device that
connects to one of your household appliances and electronics for
allow you to monitor and control power consumption at
distance via a web browser or smartphone.

Using Z-Wave technology, the PowerNode controlled outlet is
compatible with most domotic market boxes like Fibaro
Home Center 2, eedomus or Zipabox.

PowerNode plug-in module collects consumption data
connected device and transmits them to the home automation box.
This controlled outlet also allows you to enable or disable
the device remotely via a web browser or smartphone or set
a calendar to automatically enable or disable your device
at predefined times.

A small thumbwheel on the side of the socket allows you to choose a color
which will represent the room to which it is assigned. For example "
blue for the room. "This trick will allow you to differentiate your
different PowerNode plugs and sockets. We can also adjust
this wheel on a padlock. This function allows you to lock the
taken in order to avoid turning it off by accident but the control since
home boxing will no longer be possible.

The PowerNode controlled outlet also has a status indicator
bright which gives different information according to its color:
switched on or off, limited radio range, inclusion mode and
exclusion.

The PowerNode plug-in module is equipped with a protection against
overcurrent to protect the connected device. The PowerNode plug will be
deactivated in case of malfunction of a defective device or
short circuit. Additional protection is provided by the fuse
internal located in the socket.

\

functions
---------

\

-   Order a lamp or a device remotely

-   Plug module integrating directly between an electrical outlet and
    the charge to order

-   Allows consumption tracking of the connected device

-   ON / OFF function

-   Ability to assign a number and a color to it in order to
    differentiate the different PowerNode from the same installation

-   On / Off button directly on the socket

-   Overcurrent protection

-   Light status indicator

\

Technical characteristics
---------------------------

\

-   Alimentation : 250V \~ AC, 50Hz

-   Maximum charging current: 10A

-   Maximum load power: 2400W (@ 240V)

-   Standby power consumption: 0.4 W

-   Measurement accuracy: ± 0.1W

-   Overcurrent protection: 10A internal fuse

-   Plug type: DIN49440 / CEE 7/7 (Schuko)

-   Z-Wave Frequency Radio: 868.42MHz

-   Z-Wave maximum range: 30m

-   Operating temperature: 0 ° C to + 25 ° C

-   Storage temperature: -20 ° C to + 60 ° C

-   Maximum humidity: 5% to 90%

-   IP Rating (Humidity Tolerance): IP20

\

Module data
-----------------

\

-   Brand: GreenWave

-   Name: GreenWave \ [1 x taken \]

-   Manufacturer ID: 153

-   Product type: 2

-   Product ID: 2

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
> present inclusion under the catch.

\

![inclusion](../images/greenwave.Powernode1/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/greenwave.Powernode1/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/greenwave.Powernode1/commandes.jpg)

\

Here is the list of orders:

\

-   Status: This is the command that allows to know the status of the
    taking

-   On: This is the command that turns on the plug

-   Off: This is the command that turns off the plug

-   Power: It's the command that goes back the instantaneous power
    consumed

-   Conso: This is the order that goes back the total consumption

\

Note that on the dashboard the ON / OFF / STATUS commands are grouped together
in one button.

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

![Config1](../images/greenwave.Powernode1/config1.jpg)

\

As you can see there is not a lot of configuration
for this module.

\

Parameter details:

\

-   1: Delay before the blinking of the button: number of seconds
    minimum between two calls (if this time is exceeded the button
    the socket will flash)

-   2: Selected color of the wheel (detected automatically)

\

### Groups

\

This module has four association groups, only the 3rd group is
essential.

\

![Groupe](../images/greenwave.Powernode1/groupe.jpg)

\

Good to know
------------

\

Unlike its big sister power strip, this jack does not require
polling to boost consumption.

\

### reset

\

![Config2](../images/greenwave.Powernode1/config2.jpg)

\

You can reset your consumption meter by clicking
on this button available in the System tab. It's necessary to choose
Pressbutton.

\

### Specificities

\

Wakeup
------

\

No notion of wakeup on this module.

\

F.A.Q.
------

\

Did you associate group 3 of the module with Jeedom?

\

No. The module does not allow it. Put on a small piece of ribbon
black adhesive.

\

**@** sarakha63
