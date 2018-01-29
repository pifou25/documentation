D-Link DCH-Z110 - "3 in 1 Opening"
====================================

\

-   **The module**

\

![module](../images/dlink.dchz110/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/dlink.dchz110/vuedefaut1.jpg)

\

summary
------

\

The DCH-Z110 detector offers 3 different functions: detection
opening, temperature sensor and brightness sensor. He is
consists of two parts: a detector and a magnet. They are designed
to be placed on a door or window with the magnet attached to the
part that opens and the detector on the fixed part.

Opening the door or window will move the magnet away from
detector, which will trigger the detector that will send a Z-Wave signal
if the system is armed (this signal can be operated by a
siren or by a home automation box for example). The sensor can also
be used for automatic lighting control, depending on the
brightness level. For example, the sensor will send a signal to
the Z-Wave switch to turn on the light when the door opens
and that the room is dark.

The detector will also go up the brightness and the temperature, either in
case of significant change, and each time the opening / closing
is detected. A Z-Wave controller (remote control, dongle ...?) Is
necessary to integrate this detector into your network if you have
already an existing network.

\

functions
---------

\

-   3-in-1 detector: Opening, temperature, light

-   Optimized antenna range

-   Use for home automation or security applications

-   Button to include / exclude the detector

-   tamper

-   Low battery indication

-   Small, discreet and aesthetic

-   Ease of use and installation

\

Technical characteristics
---------------------------

\

Official site :
<Http://www.dlink.com/-/media/Consumer_Products/DCH/DCH%20Z110/Datasheet/DCH_Z110_Datasheet_FR.pdf>

Other technical link:
<Http://www.kafkas.gr/uploads/Pdf/182732/DCH-Z120_183010381_01_Z02.PDF>

![caracteristiques
techniques](../images/dlink.dchz110/caracteristiques_techniques.jpg)

\

Module data
-----------------

\

-   Brand: D-Link

-   Model: DCH-Z110 Door and Window Opening Detector
    mydlink ™ Home

-   Manufacturer: FIBARO System

-   Manufacturer ID: 264 \ [0x0108 \]

-   Product Type: 2 \ [0x0002 \]

-   Product ID: 14 ​​\ [0x000e \]

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
> Do not install the module on the window / door before having it
> properly configured, and pay attention to the alignment of
> the magnet during tests on a flat surface and during installation.
> (Use shims if necessary) To put this module in mode
> inclusion must be pressed 3 times on the association button in 1.5
> second, according to his documentation. (constant red flashing
> in association mode

\

![config inclusion](../images/dlink.dchz110/config-inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/dlink.dchz110/apres_inclusion.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/dlink.dchz110/commandes.jpg)

\

Here is the list of orders:

\

-   Opening: it is the command that will remount a detection
    opening

-   Temperature: it is the command which allows to go up the
    temperature

-   Brightness: it is the command which makes it possible to raise the luminosity

-   Sabotage: it is the sabotage command (it is triggered in
    case of tearing)

-   Battery: it's the battery control

\

### Module configuration

\

> **Important**
>
> When first included, or a modification, save and then
> always wake up the module by pressing the association button.
> It should blink red and change status.

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

![Config1](../images/dlink.dchz110/config1.jpg)

![Config2](../images/dlink.dchz110/config2.jpg)

\

Parameter details:

\

-   2: Adjusts the signal sent to the modules in the group
    association 2

-   4: Adjusts the brightness level from which the
    signal defined in parameter 2 will be sent to the modules associated with the
    group 2

-   5: operating mode (refer to the
    manufacturer's documentation)

-   6: multi-sensor operating mode (refer to the
    manufacturer's documentation). Recommended value: 7

-   7: Custom operating mode of the multi-sensor (refer to
    on the manufacturer's documentation). Recommended value: 20 (for
    have functional opening)

-   9: Set how long the OFF signal will be
    sent to modules associated with group 2

-   10: Sets the duration between two battery reports (one
    unit = parameter 20)

-   11: Sets the duration between two opening auto reports
    (one unit = parameter 20)

-   12: Sets the duration between two auto reports of
    brightness (one unit = parameter 20). Recommended value: 6

-   13: allows to define the duration between two auto reports of
    temperature (one unit = parameter 20). Recommended value: 2

-   20: duration of an interval for parameters 10 to 13. Value
    recommended: 10

-   21: value of variation in ° F of temperature to trigger a
    report

-   22: value in% of brightness variation to trigger
    a report. Recommended value: 10

\

### Groups

\

This module has two association groups, only the first is
essential.

\

![Groupe](../images/dlink.dchz110/groupe.jpg)

\

Good to know
------------

Association / Notification possible with other modules (example: Siren
DCH-Z510 notification chime on opening door / window)

\

Alternative visual
-----------------

\

![Groupe](../images/dlink.dchz110/autre_visuel_jeedom.jpg)

\

Wakeup
------

\

To wake up this module there is only one way to proceed:

-   Release the association button and press it again

-   Lower the wake-up interval in the configuration / system of the module
    (in seconds)

\

F.A.Q.
------

\

This module wakes up by pressing its association button.

\

This module is a battery module, the new configuration will be
taken into account at the next wakeup. (association button for the
force, hence the interest of not setting up the module before its
good configuration)

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

