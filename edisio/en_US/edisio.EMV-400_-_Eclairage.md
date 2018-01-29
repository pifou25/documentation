-   **The module**

![module](../images/emv.400/module.jpg)

-   **The Jeedom**

![vue default eclairage](../images/emv.400/vue_default_eclairage.jpg)

summary
======

The micromodule EMV-400 will allow you to manage an engine
bidirectional or electrical equipment. It allows control
2 On / Off outputs or Roller shutter Open / Stop / Close.

Moreover, the interaction with other protocols is possible, it is
controllable by switches and / or remotes of the brand
Edisio, directly from Jeedom, but also by any
Z-Wave transmitter on your network.

Each module Edisio on electrical network, with the possibility of
function as a wireless repeater with the other modules, so
to ensure total coverage of your home.

Finally, each module can be used in remote mode, it is very
convenient because it allows to associate a transmitter without having to access the
receiver.

> **Important**
>
> The neutral is only necessary for the "Shutter" mode

functions
=========

-   2 relay outputs powered

-   Can be installed in a 55mm embedding box or directly in
    the caissons of the openings

-   Usage mode: On / Off, Open / Stop / Close

-   Compatible with electronic end-stroke motors and
    mechanical

-   Deported mode

-   Timer function: On / Off mode: 30min or 60min

-   Replica signal (repeater)

-   Bidirectional micromodule

-   Low battery level of the transmitter

-   Small, discreet and aesthetic

-   Ease of use and installation

Technical characteristics
===========================

-   Module type: Edisio receiver

-   Power supply: 230VAC, 50Hz

-   Wiring: 4 wires, 2 for controls and 2 for power

-   Frequency: 868.3 MHz

-   Powered outputs: 2 relays

-   Maximum power: 2A per output

-   Resistive load: 460W

-   Other charges: 100W

-   Operating temperature: -10 ° C + 45 ° C

-   Dimensions: 48x46x26mm

-   Degree of protection: IP20

Module data
=================

-   Brand: Edisio Smart Home

-   Name: EMV-400

General configuration
======================

To configure the Edisio plugin and associate a module with Jeedom,
refer to this
[Documentation] (https://www.jeedom.fr/doc/documentation/plugins/edisio/fr_FR/edisio.html).

> **Important**
>
> So that Jeedom automatically creates your sending modules, do not forget
> do not activate the option in the plugin configuration.

> **Important**
>
> Conversely, Edisio receivers are manually created in
> Jeedom.

DIP Switch and "R" button:
--------------------------

![bouton association](../images/emv.400/bouton_association.jpg)

-   The DIP Switch will allow you to adjust the parameters
    (Repeater / Shutter Mode / Lighting / Timer) of the module:

![dip switch](../images/emv.400/dip_switch.jpg)

> **Note**
>
> To avoid unnecessary redundancies, never activate the mode
> "Repeater" on all receivers, up to 5 receivers per
> installation.

-   The button "R", will allow to associate a transmitter to the receiver,
    activate or deactivate the timer function and activate the
    deported:

![bouton r](../images/emv.400/bouton_r.jpg)

> **Note**
>
> Pressing R 3x activates the remote mode.

Operating diagram
---------------------------

Next if your transmitter is set to "1 touch" or "2" mode
"keys", here is the operation of the module:

> **Note**
>
> Refer to the manufacturer's documentation, so that you can
> configure your transmitter.

![diagramme](../images/emv.400/diagramme.jpg)

Timer function
------------------

The timer function automatically switches off the relays after
30 or 60 minutes.

-   Activate: Press 4x "R" of the receiver, confirmation by a simple
    continuous beep

-   Disable: Press 5x "R" of the receiver, confirmation by 3 simple
    beep sound.

-   30 minute timer: DIP Switch 3 at the top

-   60 minute timer: DIP Switch 3 at the bottom

"Lighting" mode
===================

The "Lighting" mode allows you to control 2 electrical devices at
distance.

> **Important**
>
> Neutral is not necessary

Configuration and electrical connections:
--------------------------------------------

![mode eclairage](../images/emv.400/mode_eclairage.jpg)

> **Important**
>
> In order for the module to be in "Lighting" mode, the DIP Switch 2 must be
> at the top

> **Important**
>
> NEVER CONNECT TO POWER

Module creation in Jeedom
------------------------------

To associate an Edisio receiver module with Jeedom, you have to create
manually a piece of equipment.

![ajout equip](../images/emv.400/ajout_equip.jpg)

Once your equipment is created, you should get this:

![crea equip](../images/emv.400/crea_equip.jpg)

> **Note**
>
> Remember to activate your new equipment.

In the equipment list, on the right, select "Micro-module
light ":

![infos equip eclairage](../images/emv.400/infos_equip_eclairage.jpg)

Orders
---------

Once your equipment is backed up, you should get the orders
associated with the module:

![Commandes](../images/emv.400/commande_eclairage.jpg)

Here is the list of orders:

-   On: This is the command that activates the relay 1

-   Off: This is the command to disable relay 1

-   On 2: This is the command that activates relay 2

-   Off 2: This is the command to disable relay 2

-   E: This is the command that allows you to use the remote mode

> **Important**
>
> The return of state is simulated by Jeedom. Therefore, if you
> use another transmitter, Jeedom will not be able to update the status
> the receiver.

information
------------

Once your equipment associated with Jeedom, various information will be
available:

![Commandes](../images/emv.400/infos_eclairage.jpg)

-   Creation: Indicates the date on which the equipment was created

-   Communication: Indicates the last call recorded between
    Jeedom and the micro-module

-   Battery: Indicates battery status for battery modules

-   Status: Returns the status of the module

Association of the micromodule in Jeedom
===================================

So that you can interact with Jeedom, as if it were a
Edisio transmitter.

> **Note**
>
> One of the big advantages of Edisio is that a receiver can have
> several associated issuers

Standard method
----------------

Each output is to be associated with a Jeedom command:

-   Associate Output 1:

    -   Press 1x on the receiver "R", single beep sound (short
        in repetition) signals the programming of output 1 activated.

    -   Within 10 sec, press "Test" on the "Open" command
        in Jeedom, a continuous beep signals the association of
        exit 1 to Jeedom.

    -   Within 10 sec, press "R" on the receiver again, for
        confirm the association, the beep stops.

-   Associate Output 2:

    -   Press 2x on the "R" receiver, double beep sound (short
        in repetition) indicates the programming of output 2 activated.

    -   Within 10 seconds, press "Test" on the "Close" command
        in Jeedom, a continuous beep signals the association of
        Exit 2 to Jeedom.

    -   Within 10 sec, press "R" on the receiver again, for
        confirm the association, the beep stops.

Deported method
----------------

We talked about it at the beginning of this documentation. In the case of
already built-in modules, in false ceilings or attics.
This method allows the addition of a new transmitter without accessing the "R" of the
receiver.

-   Associate the "R" button:

    -   Press 3x on "R" receiver, triple beep sound (short
        in repetition) indicates the activated programming mode.

    -   Within 10 sec, press "Test" command "E" in
        Jeedom, a continuous beep signals the association to Jeedom.

    -   Within 10 sec, press "E" on the receiver again, for
        confirm the association, the beep stops.

It's done, your Jeedom is now associated and his command "E"
now replaces the "R" button on the receiver.

-   Associate a new transmitter to a receiver with Jeedom already associated
    :

    -   Exit 1:

        -   Press 1x "Test" the "E" command in Jeedom, simple
            beep (short in repetition) indicates the programming of
            output 1 activated.

        -   Within 10 sec, press one of the "C" keys on the new
            transmitter to associate, a continuous beep signals
            the association of exit 1.

        -   Within 10 sec, press again "Test" of the
            command "E" in Jeedom, to validate the association, the beep
            sound stops.

    -   Exit 2:

        -   Press 2x "Test" of the "E" command in Jeedom,
            double beep (short in repetition) signals the
            programming of output 2 activated.

        -   Within 10 sec, press one of the "C" keys on the new
            transmitter to associate, a continuous beep signals
            the association of the exit 2.

        -   Within 10 sec, press again "Test" of the
            command "E" in Jeedom, to validate the association, the beep
            sound stops.

> **Note**
>
> You can start again as many times as you want to associate
> from transmitters to receiver

Alternative visual
=================

![Commandes](../images/emv.400/vue_alt_eclairage.jpg)

F.A.Q.
======

How to clear the memory of the receiver?

: Press and hold for 10 seconds on the "R" until you hear a continuous beep.

How to control the receiver via a Z-Wave transmitter?

: With the Jeedom script plugin.

How can I have the same visual?

: With the Jeedom Widgets plugin.

**@** Jamsta
