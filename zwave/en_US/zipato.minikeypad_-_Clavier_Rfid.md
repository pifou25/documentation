Zipato miniKeypad RFID
======================

\

-   **The module**

\

![module](../images/zipato.minikeypad/module.jpg)

\

-   **The Jeedom**

\

![vuedefaut1](../images/zipato.minikeypad/vuedefaut1.jpg)

\

summary
------

\

Control your security system with this mini Zipato wall keyboard
!

With this Z-Wave compatible RFID keyboard, you will be able to activate or
easily disable your alarm system. The keys "Home" and
"Away" allows you to arm / disarm the security system and / or
run domotic scenarios quickly. In addition to using the
digital keyboard, you can also pass an RFID badge in front of the
keyboard to arm / disarm the system. The keyboard transmits to your
home automation controller the identifier of the badge that has been recognized. You
can easily create scenarios based on the person
who used his badge.

\

functions
---------

\

-   Keyboard with code and RFID

-   Supports Z-Wave technology

-   Arm / Disarm your security system

-   Access control by reading RFID badges

-   Code keypad access control

-   Tamper protection

-   LED indicator to confirm each action

-   Built-in buzzer for audible indication of the arming / disarming of
    the alarm for example

\

Technical characteristics
---------------------------

\

-   Type: Z-Wave Slave

-   Power supply: 2x AA 1.5V batteries

-   Frequency: 868.42 MHz

-   Radio range: 30m in free field

-   RFID protocol: ISO15693, ISO18000-3, Tag-it ™, RFID

-   Buzzer: 60dBa at 10 cm distance

-   Storage temperature: -5 ° C to + 65 ° C

-   Storage humidity: 10% to 70%

-   Operating temperature: 10 ° C to 40 ° C

-   Operating humidity: 30% to 80%

-   Dimensions: 62 x 62 x 20 mm

-   Certifications: Safety: UL EMC: FCC, CE RoHS

\

Module data
-----------------

\

-   Brand: Zipato

-   Name: Zipato Mini Keypad RFID

-   Manufacturer ID: 151

-   Product type: 24881

-   Product ID: 17665

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
> To put this module in inclusion mode just press two
> seconds on the metal tab (the red LED on the front panel
> must flash twice) and release the tab so that
> the inclusion takes place.

\

![inclusion](../images/zipato.minikeypad//inclusion.jpg)

\

Once included you should get this:

\

![information](../images/zipato.minikeypad/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![commandes](../images/zipato.minikeypad/commandes.jpg)

\

Here is the list of orders:

\

-   Action: it's the command that will move up the home / away (5 for away 6
    for home)

-   Sabotage: it is the sabotage command (it is triggered in
    case of tearing)

-   Code: displays the code of the badge or keypad when the code entered
    is not in one of the memories

-   Battery: it's the battery control

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

![bouton configuration](../images/plugin/bouton_configuration.jpg)

\

You will arrive on this page (after clicking on the tab
Settings)

\

![config1](../images/zipato.minikeypad/config1.jpg)

\

Parameter details:

\

-   1: allows to reset the config by default (not recommended)

-   2: cancellation duration (not to be modified)

-   3: return by beep: allows to activate or not a series of 8 beeps
    after recognition of a badge / code

-   4: number of beeps per second (do not change has no effect)

-   5: operating mode: normal or always awake mode
    (not recommended because very very consumer of batteries)

\

### Groups

\

This module has two association groups.

\

![groupe](../images/zipato.minikeypad/groupe.jpg)

\

> **Important**
>
> For optimum operation of your module. It is necessary that Jeedom
> at least be associated with group 1.

### Badges / codes

\

In the equipment page there is a Wizard tab.

\

![bouton assistant](../images/plugin/bouton_assistant.jpg)

\

This one allows to add codes. You will see a painting.

\

![config2](../images/zipato.minikeypad/config2.jpg)

\

-   This table allows you to view the memories occupied on your
    keyboard

-   To save a new code click on the green button on the
    desired memory and follow the steps

-   To delete a code just click on the red button.

-   It is impossible to register the same code / badge on two memories
    different

-   It is impossible (for security reasons) to read the value of a
    registered code

\

> **Important**
>
> Remember to wake the module after adding a code or badge.

\

Examples of use
----------------------

\

![exemple](../images/zipato.minikeypad/exemple.jpg)

\

The trigger element is the event command, indeed this one is
updated only when a valid code / badge has been submitted. If the
value is 6 (home) disable the alarm (for example), or turn on the
power strip, turn on the light according to the brightness, send
a notification to indicate that someone has returned, we launch a
voice syntenesis for a weather report for example. Otherwise (necessarily
5) activate the alarm, cut the power strip, send a
notification to indicate that the house is empty.

\

Good to know
------------

\

### Specificities

\

The keypad reads the codes / badges in two ways:

\

-   when you press home / away during the first 1 to 2
    seconds if you start typing a code, it will read this code

-   if nothing is done in the first 1 to 2 seconds, it goes into
    RFID badge reading mode (red light on). At this moment
    he can read a badge, not before.

\

Wakeup
------

\

To wake up this module there are two ways to proceed:

\

-   press the tamper button and release after 1 to 2 seconds

-   press Home, a random number and Enter

\

F.A.Q.
------

\

This module wakes up by pressing the tamper button and
releasing. He can also wake up by pressing Home then 1 and then
Enter.

\

This module is a battery module, the new configuration will be
taken into account at the next wake up.

\

Important note
---------------

\

> **Important**
>
> You have to wake up the module: after its inclusion, after a change
> of the configuration, after a change of wake up, after a
> change of association groups

\

**@** sarakha63
