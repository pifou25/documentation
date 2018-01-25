Aeotec Garage Door Controller
====================================

\

-   **The module**

\

![module](../images/aeotec.garagedoorcontroller/module.jpg)

\

-   ** The Jeedom **

\

![vuedefaut1](../images/aeotec.garagedoorcontroller/vuedefaut1.jpg)

\

summary
------

\

Easily connected to the existing motor of your door, the controller
garage door improves with a suite of security sensors and
safety. The garage door controller does not just allow you to
control your garage door, it also allows you to check
its state. Whether used by the engine or manually, the detector
smart delivered with the garage door controller knows if the door
is open or closed, and can warn you when this is happening
should not.

\

functions
---------

\

-   Control and monitor your garage door remotely.

-   Module that simply installs on your engine
    current door.

-   Door control locally via the integrated button.

-   Send opening / closing alerts to the Z-Wave controller.

-   Audible / audible opening / closing alerts

-   Adjustable alarm sound volume (105 dB max)

-   USB port to charge your own MP3 sounds.

-   Integrated status LED on the button.

-   Part of the Gen5 range of Aeon Labs.

-   Security of radio communication via AES-128 encryption.

-   Integrates the Z-Wave 500 series chip.

-   250% faster communication compared to devices
    Z-Wave standard.

-   Z-Wave message repeater.

-   Optimization of the antenna, range 300 meters.

\

Technical characteristics
---------------------------

\

-   Module Type: Z-Wave + 500 Series Receiver and Transmitter

-   Power supply: Actuator: 5 VDC (adapter supplied) Sensor: Battery
    Lithium 3V 800mA CR2

-   Standby power consumption: 1W

-   Alarm consumption: 2W

-   Maximum volume: 105 dB

-   Supported audio formats: mp3 and WMV at 320Kbps

-   Frequency: 868.42 Mhz

-   Transmission distance: 300m in free field

-   Operating temperature: -20 ° C to 50 ° C

-   Operating humidity: 80%

-   Certifications: FCC, UL, CE, ROHS

\

Module data
-----------------

\

-   Brand: Aeotec

-   Name: Garage Door Controller (ZW062)

-   Manufacturer ID: 134

-   Product type: 3

-   Product ID: 62

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
> Z-Wave, according to its paper documentation.

\

![inclusion](../images/aeotec.garagedoorcontroller/inclusion.jpg)

\

Once included you should get this:

\

![Plugin Zwave](../images/aeotec.garagedoorcontroller/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/aeotec.garagedoorcontroller/commandes.jpg)

\

Here is the list of orders:

\

-   Open / Close: Open, close or stop the garage door.

-   Position: Current position of the garage door.

-   Volume: Current volume of the speaker.

-   Temperature: Zone temperature, no automatic winding.

-   Sabotage: State of sabotage in text.

\

### Module configuration

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

![Config1](../images/aeotec.garagedoorcontroller/config1.jpg)

![Config1](../images/aeotec.garagedoorcontroller/config2.jpg)

\

Parameter details:

\

-   34: Starts the calibration of the opening time of
    the door.

-   41: Resets the tamper status by selecting "Relieve
    the alarm state "

-   80: on Hail

-   255: resets the factory configuration

\

### Groups

\

This module has two association groups. The first "Lifeline" is
essential.

\

![Groupe](../images/aeotec.garagedoorcontroller/groupe.jpg)

\

Good to know
------------

\

### Specificities

Calibration of the opening time of the garage door:

-   1: The garage door must be completely closed.

-   2: Activate parameter 34 on "Do calibration".

-   3: Start opening the door

-   4: Wait until the door is completely open.

-   5: Start closing the door

The calibration is completed

-   Parameter 34 will be updated to "Normal".

-   Parameter 35 will be updated with the calculated opening time.

\

Reset of sabotage:

-   1: The sensor must be properly attached.

-   2: Enable parameter 41 on "Relieve the alarm state".

-   3: Update the settings.

The calibration is completed

-   Parameter 41 will be updated with "Sensor is not removed".

\

F.A.Q.
------

\

\

** @ ** nechry
