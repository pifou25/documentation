Nodon Smart Socket - Smartplug
====================================

\

-   **The module**

\

![module](../images/nodon.smartplug/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/nodon.smartplug/vuedefaut1.jpg)

\

summary
------

\

The NodOn® remote control socket can be controlled via a home automation system
Z-Wave® or Z-Wave Plus® compatible or directly via other
Z-Wave® or Z-Wave Plus® controllers such as the Soft Remote,
wall switch or Octan Remote NodOn®. German standard
(Schuko) or French (Type E), the plug can be plugged into the 2
sense, head up or upside down. Associated with its fine design, these 2
features allow for easy integration without clogging
neighboring drums on a power strip. Learning to take with his
controller only requires a few seconds. A local button allows
turn on or off the plug directly.

\

functions
---------

\

-   Power loss detection

-   Ergonomic: Ability to connect the head-up / head-in
    low

-   Intelligent management of alarms

-   Improved radio range

-   Maximum Amperage: 16A

\

Technical characteristics
---------------------------

\

-   Power supply: 230V AC +/- 10% - 50Hz

-   Maximum power: 3000W continuous / 3500W cyclic
    (Resistive load) Intrinsic consumption: &lt;1W

-   Operating temperature: 0 ° C to 40 ° C - Altitude: 2000m

-   Z-Wave® Radio Protocol: 868.4MHz - 500 Series - Z-Wave Compatible
    SDK 06.51.01

-   Range: 40m indoor / 80m outdoor

-   Dimensions: 104 \ * 51 \ * 36mm

-   2 years warranty

-   Type EU

\

Module data
-----------------

\

-   Brand: Nodon

-   Name: Smartplug

-   Manufacturer ID: 357

-   Product type: 1

-   Product ID: 1

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
> until the light turns red, according to its documentation
> paper.

\

![inclusion](../images/nodon.smartplug/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/nodon.smartplug/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/nodon.smartplug/commandes.jpg)

\

Here is the list of orders:

\

-   Status: This is the order that allows to know the status of the
    socket (On / Off)

-   On: This is the command that turns on the plug

-   Off: This is the command that turns off the plug

-   Status: Lets you know if the plug is powered or not
    (Detection of power failure / disconnection)

\

Note that on the dashboard, state, ON / OFF information is found on
the same icon.

\

### Module configuration

\

You can configure the module according to your
installation. To do this, go through the "Configuration" button on the
Zwave plugin from Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

You will arrive on this page (after clicking on the tab
settings)

\

![Config1](../images/nodon.smartplug/config1.jpg)

![Config1](../images/nodon.smartplug/config2.jpg)

\

Parameter details:

\

-   1: This parameter sets the status (ON / OFF) of the Smart Plug after a
    power failure or after connection

-   2: This parameter is used to con fi gure the noti fi cation reports of
    shutdown / return of power, as well as the associated groups (Groups
    4, 5, 6, 7, 8). Several combinations are possible (refer to
    the paper documentation or the help bubble in jeedom). It is
    recommended to set this parameter to 1.

-   3: This parameter enables or disables groups 2 and 3.

-   4: The parameter forces the status of Smart Plug to "ON" (Smart
    Plug activated). When the parameter is enabled, it is not
    possible to turn off the Smart Plug (local or radio)

-   Parameters 5 to 20: Through the configuration parameters \ # 5 to
    \ # 20, it is possible to con fi gure up to 8 different alarms.
    In order to properly con fi gure your alarms, the online form:
    www.nodon.fr/support/asp3/alarm will guide you

### Groups

\

This module has 8 association groups.

\

![Groupe](../images/nodon.smartplug/groupe.jpg)

\

-   Group 1 - Lifeline: This group is generally used to
    report information from the Smart Plug to the main controller
    network.

-   Group 2 - Smart Plug Status Monitoring When Smart Plug
    is activated (respectively deactivated) via the local button,
    it sends an activation command
    (respectively deactivation) to the associated devices. Any
    command is sent if the status change of the Smart Plug has
    been caused by a radio command

-   Group 3 - Complementary status monitoring When the Smart Plug
    is activated (respectively deactivated) via the local button,
    it sends a deactivation command
    (respectively activation) to the associated devices. Any
    command is sent if the status change of the Smart Plug has
    been caused by a radio control.

-   Group 4 - Noti fi cation of power failure When the Smart Plug
    detects a power failure or a current feedback, a report
    notification is sent to the associated equipment. The report sent
    is a "Noti fi cation Report: Power Management - AC disconnected
    / Re-connected).

-   Group 5 - Activation on power failure When Smart Plug
    detects a power failure, it activates the associated devices.

-   Group 6 - Disabling Power Failure When Smart
    Plug detects a power failure, disables devices
    Related

-   Group 7 - Activation on current feedback When the Smart Plug
    detects a return of the current, it activates the associated devices.

-   Group 8 - Disabling on current feedback When the Smart Plug
    detects a return of the current, it deactivates the associated devices

\

> **Important**
>
> At least Jeedom should be in groups 1 and 4 \

Good to know
------------

\

### Specificities

\

-   It's useless to have fun plugging / unplugging the plug for
    observe the alarm. This one will only work about 3 times. the
    beyond the socket must stay powered a little while to recharge
    the internal battery.

\

Wakeup
------

\

No notion of wakeup on this module.

\

F.A.Q.
------

\

You do not have to have the option to download auto widgets
of activated. You can grab the mobile widgets and dashboard on the
market: alarm \ _prise.

\

Have you set parameter 2 correctly? Do you have well Jeedom at least
in groups 1 and 4? Do you leave time to the pile to get
to charge?

\

**@** sarakha63
