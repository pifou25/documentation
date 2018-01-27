-   **The module**

![module](../images/etc4/module.jpg)

-   ** The Jeedom **

![vue default](../images/etc4/vue_default.jpg)

summary
======

The 4-channel mini e-Trendy remote control is simple, robust and stylish
it was created to please. It easily connects to receivers and
can control your lighting on / off and dimmables, engines,
blinds, shutters, gates, garage doors. It has two modes of
programming.

Moreover, the interaction with other protocols is possible, it can
interact with Edisio brand receivers, with Jeedom, but
also by any Z-Wave receiver on your network.

functions
=========

-   Usage mode: On / Off, Open / Stop / Close, Dimmer,
    Motorization, Blinds, Shutters, Gates, Garage doors

-   2 programming modes

-   Small, discreet and aesthetic

-   Ease of use and installation

Technical characteristics
===========================

-   Module type: Edisio transmitter

-   Power supply: 3VDC (CR2430 Lithium Battery)

-   Channels: 4

-   Frequency: 868.3 MHz

-   Operating temperature: -10 ° C + 50 ° C

-   Dimensions: 52x28x12mm

-   Degree of protection: IP40

Module data
=================

-   Brand: Edisio Smart Home

-   Name: ETC4

General configuration
======================

To configure the Edisio plugin and associate a module with Jeedom,
refer to this
[Documentation] (https://www.jeedom.fr/doc/documentation/plugins/edisio/fr_FR/edisio.html).

> ** Important **
>
> So that Jeedom automatically creates your sending modules, do not forget
> do not activate the option in the plugin configuration.

The trends
---------

Control and centralize your on / off lights and dimmers,
opening, motors, on the same key or on 2 separate buttons. The
e-Trendy remote controls have 2 modes of operation, MODE 1 and MODE 2
:

-   MODE 1: One-touch control: On / Off, Open / Close,
    Variation + / Variation-, Impulsive

-   MODE 2: Control on 2 keys:

    -   UP keys: Off, Close, Variation-, Pulse

    -   Bottom Keys: On, Open, Variation +, Pulse

Operating diagram
===========================

Depending on whether your transmitter is set to "1-touch" or "2-way"
"keys", here is the operation of the remote control:

![diagramme](../images/etc4/diagramme.jpg)

Change the mode
===============

-   MODE 1:

    -   Press and hold the "C4" key

    -   Press the "C1" key 1x, always holding the key
        "C4", the LED will flash 1 time

![mode1](../images/etc4/mode1.jpg)

-   MODE 2:

    -   Press and hold the "C4" key

    -   Press the "C1" key twice, always holding the key
        "C4", the LED will flash 2 times

![mode2](../images/etc4/mode2.jpg)

Remote control association in Jeedom
=======================================

The association of an Edisio transmitter is simple and
automatically. Just press each key you
want to have in your Jeedom.

Once your equipment is associated, you should get this:

![asso equip](../images/etc4/asso_equip.jpg)

Orders
---------

Once your equipment is created, you should get the orders
associated with the module:

![Commandes](../images/etc4/commandes.jpg)

Here is the list of orders:

-   bt01: This is the command that allows to interact with the button 1

-   bt02: This is the command that allows you to interact with the 2 button

-   bt03: This is the command to interact with button 3

-   bt04: This is the command that allows to interact with the 4 button

-   Battery: Indicates the status of the battery

information
------------

Once your equipment associated with Jeedom, various information will be
available:

![Commandes](../images/etc4/infos.jpg)

-   Creation: Indicates the date on which the equipment was created

-   Communication: Indicates the last call recorded between
    Jeedom and the micro-module

-   Battery: Indicates battery status for battery modules

-   Status: Returns the status of the module

use
-----------

Once your remote is set up, you can with the
Jeedom's scenario plugin interact with your remote on Jeedom.

> ** Note **
>
> Each key has a binary state return.

F.A.Q.
======

How to erase the association of a key with a receiver?

: Press the "R" on the receiver for 5 seconds, a single beep signals
    the deprogramming mode activated. Press the "C" key to be erased.
    Repeat this operation for all the keys to be erased.

** @ ** Jamsta
