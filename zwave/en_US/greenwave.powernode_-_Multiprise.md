Greenwave PowerNode - 6 outlets
==============================

\

-   **The module**

\

![module](../images/greenwave.powernode/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/greenwave.powernode/vuedefaut1.jpg)

\

summary
------

\

The PowerNode Power Strip from GreenWave is a smart device that
connect to your appliances and electronics for you
allow you to monitor and control the power consumption of your
devices remotely via a web browser or smartphone. using
Z-Wave technology, the PowerNode power strip is compatible with the
most home automation boxes on the market like Fibaro Home Center 2, eedomus
or Zipabox. Equipped with 6 ports, it can control independently 6
different electrical appliances with a total power of 10A.

PowerNode Power Strip Collects Consumer Data
connected devices and transmits them to the home automation box.
You can then control the power consumption of each device
logged. This power strip also allows you to enable or disable
devices remotely via a web browser or smartphone or
set a calendar to automatically enable or disable your
devices at predefined times. A small wheel on the side of the
power strip allows to choose a color that will represent the piece to
which is assigned the power strip. For example "blue for the room
This tip will allow you to differentiate your different
PowerNode power strips. It can also be set on a wheel
padlock. This function allows you to lock the power strip
to avoid extinguishing by accident, but control from the box
home automation will no longer be possible.

The PowerNode Power Strip also has a light status indicator
which gives different information according to its color: taken
on or off, limited radio range, include and exclude mode.

The PowerNode power strip is equipped with a protection against
overcurrent to protect connected devices. The PowerNode
disable ports in the event of a device malfunction
defective or short circuit. Additional protection is
ensured by the internal fuse located in the power strip.

This power strip is ideal for controlling multimedia devices in
a TV stand or to control computer equipment located
in an office and avoid having to use 6 Z-Wave sockets
individual. \

functions
---------

\

-   6-port Z-Wave power strip

-   Tracks the consumption of connected devices

-   ON / OFF function

-   Ability to assign a number and a color to it in order to
    differentiate the different PowerNode from the same installation.

-   On / Off button directly on the power strip

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

-   Name: GreenWave \ [6 x catches \]

-   Manufacturer ID: 153

-   Product type: 3

-   Product ID: 4

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
> inclusion present on the catch.

\

![inclusion](../images/greenwave.powernode/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/greenwave.powernode/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/greenwave.powernode/commandes.jpg)

![Commandes](../images/greenwave.powernode/commandes2.jpg)

![Commandes](../images/greenwave.powernode/commandes3.jpg)

![Commandes](../images/greenwave.powernode/commandes4.jpg)

![Commandes](../images/greenwave.powernode/commandes5.jpg)

\

Here is the list of orders:

\

-   State-1: This is the command that allows to know the status of the
    socket 1

-   On-1: This is the command that turns on the plug 1

-   Off-1: This is the command that turns off the plug 1

-   Power-1: This is the command that raises the instantaneous power
    consumed from the socket 1

-   Conso-1: This is the order that goes back the total consumption of the
    socket 1

-   State-2: This is the command that allows to know the status of the
    taken 2

-   On-2: This is the command that turns on the socket 2

-   Off-2: This is the command that turns off the plug 2

-   Power-2: This is the command that raises the instantaneous power
    consumed from the socket 2

-   Conso-2: This is the order that goes back the total consumption of the
    taken 2

-   State-3: This is the command that allows to know the status of the
    socket 3

-   On-3: This is the command that turns on the plug 3

-   Off-3: This is the command that turns off the plug 3

-   Power-3: This is the command that raises the power instatanée
    consumed from the socket 3

-   Conso-3: This is the order that goes back the total consumption of the
    socket 3

-   State-4: This is the command that allows to know the status of the
    socket 4

-   On-4: This is the command that turns on the 4

-   Off-4: This is the command that turns off the jack 4

-   Power-4: This is the command that raises the power instatanée
    consumed from the socket 4

-   Conso-4: This is the order that goes back the total consumption of the
    socket 4

-   State-5: This is the command that allows to know the status of the
    socket 5

-   On-5: This is the command that turns on the plug 5

-   Off-5: This is the command that turns off the plug 5

-   Power-5: This is the command that raises the instantaneous power
    consumed from the socket 5

-   Conso-5: This is the order that goes back the total consumption of the
    socket 5

-   State-6: This is the command that allows to know the status of the
    socket 6

-   On-6: This is the command that turns on the jack 6

-   Off-6: This is the command that turns off the plug 6

-   Power-6: This is the command that raises the instantaneous power
    consumed from the socket 6

-   Conso-6: This is the command that goes back the total consumption of the
    socket 6

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

![Config1](../images/greenwave.powernode/config1.jpg)

\

As you can see there is not a lot of configuration
for this module.

\

Parameter details:

\

-   1: Delays before the blinking of the button: number of seconds
    minimum between two calls (if this time is exceeded the button
    the socket will flash)

-   2: Selected color of the wheel (detected automatically)

\

### Groups

\

This module has four association groups, only the 1st group is
essential.

\

![Groupe](../images/greenwave.powernode/groupe.jpg)

\

Good to know
------------

\

### Specificities / Polling

\

Unlike her little sister "A catch", this power strip requires
polling to boost consumption.

\

![Config2](../images/greenwave.powernode/config2.jpg)

\

It is just necessary to activate it for the Power command of each
outlet. This will have the effect of raising both (conso and power)

\

### Global Consumption

\

![consocumul](../images/greenwave.powernode/consocumul.jpg)

\

You can using a virtual you create a cumulative consumption
6 shots.

\

![consocumul2](../images/greenwave.powernode/consocumul2.jpg)

\

### reset

\

![Config3](../images/greenwave.powernode/config3.jpg)

\

You can reset your consumption meter by clicking
on this button available in the System tab. (There is a reset by
socket). You have to choose PressButton.

\

Wakeup
------

\

No notion of wakeup on this module.

\

F.A.Q.
------

\

Have you paid a CRON.

\

No. The module does not allow it. Put a piece of black tape
above.

\
**@** sarakha63
