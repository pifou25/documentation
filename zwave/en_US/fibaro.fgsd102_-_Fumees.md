Fibaro FGSD-002 "Smoke Sensor 2"
================================

\

-   **The module**

\

![module](../images/fibaro.fgsd102/module.jpg)

\

-   **The jeedom**

\

![vuedefaut1](../images/fibaro.fgsd102/vuedefaut1.jpg)

\

summary
------

\

Featuring soft lines, a polished surface and a small size, this
smoke detector will allow you to be alerted of a threat with
Multicolored RGB LEDs and an integrated siren. The large format of the
grid helps detect the smallest amount of smoke so
to get a quick reaction. It will thus very easily find
place in your home to preserve the safety of all the
family.

The Fibaro Smoke Detector FGSD-002 is a Detector Alarm
Autonomous Smoke (DAAF) according to EN 14604: 2005. Good
it is also communicating thanks to Z-Wave technology
More.

Some materials burn without smoking. That is why the engineers of
Fibaro have decided to include additional protection in their
smoke detector in the form of a temperature sensor. If the
amount of smoke is not enough to trigger the alarm,
the device will still be able to detect a threat by detecting
a rapid change in temperature caused by fire. A change
fast temperature or increase up to 54 ° C is enough
so that the smoke sensor detects a threat and signals it to
inhabitants of the house. Only this type of smoke sensor offers a
high efficiency, regardless of what burns.

\

functions
---------

\

-   Z-Wave smoke detector

-   Battery powered

-   Adjustable sensor sensitivity (3 levels)

-   Protection against sabotage

-   Alarm signaled by sound, LED light and Z-Wave signal

-   Fire detection by measuring the air temperature

-   Automatic efficiency test, performed every 5 seconds

-   Built-in Z-Wave network coverage tester

-   Complies with EN 14604: 2005

-   Z-Wave Plus compatible

-   Very simple installation - just install it in one place
    or there is a risk of fire

\

Technical characteristics
---------------------------

\

-   Module type: Z-Wave transmitter

-   Power supply: 3V CR123A Lithium Battery

-   Battery life: 3 years

-   Frequency: 868.42 MHz

-   Transmission distance: 50m free field, 30m indoor

-   Dimensions: 65 x 28 mm (diameter x height)

-   Operating temperature: 0-55 ° C

-   Operating humidity: 0% - 93%

-   Range of temperature measurement: -20 to 100 ° C

-   Smoke sensitivity: 1st level - 1.20 +/- 0.5% obs / m; 2nd
    level - 1.80 +/- 0.5% obs / m; 3rd level - 2.80 +/- 0.5% obs / m

-   Noise level: 85 dB at 3m

-   Measurement accuracy: 0.5 ° C (in a range of 0 to 55 ° C)

-   Standards: EMC 2004/108 / EC and R & TTE 199/5 / WE

-   Certifications: EN 14604: 2005

\

Module data
-----------------

\

-   Brand: Fibar Group

-   Name: Fibaro Smoke Sensor FGSD-002

-   Manufacturer ID: 271

-   Product type: 3074

-   Product ID: 4098

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
> To put this module in inclusion mode you have to press 3 times on the
> central button of inclusion, according to its paper documentation.

\

![inclusion](../images/fibaro.fgsd102/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/fibaro.fgsd102/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/fibaro.fgsd102/commandes.jpg)

\

Here is the list of orders:

\

-   Smoke: this is the alert command of the module (for smoke,
    heat ...)

-   Temperature: this is the temperature control

-   Sabotage: This is the sabotage command. It signals the opening
    of the box

-   Test Alert: this is the command that will go back to the fact that the module
    is in test mode

-   Heat Alert: it's the order that will go up a heat alert
    (not reliable yet)

-   Battery: it's the battery control

\

### Module configuration

\

> **Important**
>
> During a first inclusion always wake up the module just after
> inclusion.

\

Then it is necessary to perform the configuration of the module in
depending on your installation. You have to go through the button
"Configuration" of Jeedom's OpenZwave plugin.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

You will arrive on this page (after clicking on the tab
Settings)

\

![Config1](../images/fibaro.fgsd102/config1.jpg)

![Config2](../images/fibaro.fgsd102/config2.jpg)

\

Parameter details:

\

-   Wakeup: this is the wakeup interval of the module (value
    recommended 21600)

-   1: Adjusts the sensitivity of smoke detection

-   2: allows to choose the notifications that will be sent to Jeedom
    (advice: all)

-   3: lets you choose which notifications will be accompanied by a
    visual indication

-   4: allows you to choose which notifications will be accompanied by a
    sound indication (in all cases the heat and
    fires will sound the module)

-   10: do not change this setting unless you know what you
    make

-   11: same

-   12: same

-   13: allows to notify other modules zwave (to disable unless
    you know why you activate it)

-   20: time between two temperature reports

-   21: temperature difference from which, even if the duration
    from above is not reached, the temperature will be sent to Jeedom

-   30: heat alarm trigger temperature

-   31: interval of signaling of the peaks of temperature

-   32: signal interval if Zwave loss

\

### Groups

\

For optimum operation of your module. Jeedom must be
associated at least with groups 1 4 and 5:

\

![Groupe](../images/fibaro.fgsd102/groupe.jpg)

\

Good to know
------------

\

### Specificities

\

### Alternative visual

\

![widget1](../images/fibaro.fgsd102/widget1.jpg)

\

Wakeup
------

\

To wake up this module, press the central button 3 times

\

F.A.Q.
------

\

This module wakes up by pressing 3 times on its inclusion button.

\

This module is a battery module, the new configuration will be
taken into account at the next wakeup.

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
