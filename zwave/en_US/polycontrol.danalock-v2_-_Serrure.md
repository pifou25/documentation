Danalock V2 BTZE
================

\

-   **The module**

\

![module](../images/polycontrol.danalock/module.jpg)

\

-   ** The Jeedom **

\

![vuedefaut1](../images/polycontrol.danalock/vuedefaut1.jpg)

\

summary
------



** Secure your home using the Z-Wave Electronic Lock
Poly-Control! **

More keys, use your smartphone to lock and
unlock your door! Danalock is a new solution that you
will reliably and intelligently secure your home.
Without a key, you can open your lock with your
tablet or smartphone. You will control the access of your guests or
workers and can effectively monitor your home.
Different settings will allow you to control access to your
House. Danalock has an Autolock function allowing a
automatic locking of the entrance door. Ideal when you do not have
not free hands, for example. In addition, 5 keys are provided. You
can be used from the outside. The installation is simple and fast
to perform regardless of the type of door. The corresponding application
is compatible for iPhone 4S, Android 4.4 and Smartphone. Danalock does not
requires no external power source. food
is carried out using batteries with a life of two years. You
will receive an audible signal in case the battery charge level
is too weak

**Easy to put in place**

The Danalock is an intelligent lock that mounts on almost
all the doors in a few minutes.

** Easy to install **

Install the Danalock app on your phone in a few seconds
seconds. A wizard then guides you through the installation and
the calibration of your Danalock.

**Easy to use **

Lock and unlock with the button, the TwistAssist function or
using your smartphone. And with the auto-unlock function,
the Danalock lock automatically unlocks the door when you
approach your house and lock it right after you are
returns.

** Long battery life **

The Danalock has an average battery life of up to one year, and
does not require external power supply. Be informed that the use
a Z-Wave home automation controller or box can reduce the life of
battery. The state of the battery is easily visible in the App.
When the battery reaches 30, 20, 15 and 10 percent, a notification
is sent by SMS and email.

** Limited or permanent access **

No need to hide the keys under the doormat. Give your
family quick and easy access with their smartphones. To your wife
household or your guests, access limited in time or recurring and
receive notifications when your lock is used and by whom.

** Total control of the house **

Develop control of your smart home with a Danalock,
the perfect initiator for all your home orders. Danalock
works seamlessly with other devices in the home
intelligent, and all communication is highly encrypted - nobody
can not hack their way into your house.

** Discreet, durable and Danish **

Danalock combines the elegance and minimalism of Scandinavian design - with
an anodized solid aluminum bezel and advanced technologies
Bluetooth and Z-Wave. A discrete Danish design designed to last.
\

functions
---------

\

-   Control your gateway remotely

-   Connected lock

-   1 cylinder adaptable to different lengths provided

-   5 physical keys are provided to open the door from the outside

-   Connection via Bluetooth Smart and Z-Wave

-   Integration into compatible Z-Wave controllers (eedomus,
    Vera, ...)

-   Activity History

-   Different adjustment possibilities for closing and opening

-   Access Sharing: give access to your housekeeper or friend
    for a limited period

-   Automatic calibration

-   Easy to install

-   Operation with batteries

-   Compatible with iOS (iPhone 4s or later), but
    also Android (from 4.4).

\

Technical characteristics
---------------------------

\

-   Power supply: 4 x CR123 3V batteries

-   Versions: V2

-   Material: Anodized solid aluminum

-   Communication: Bluetooth and Z-Wave

-   Dimensions: 79 mm x 49 mm (diameter x height)

-   Weight: 363g

\

Module data
-----------------

\

-   Brand: Poly-Control

-   Name: Danalock V2 BTZE

-   Manufacturer ID: 010e

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

> ** Important **
>
> You must include this module in secure mode.

\

To put the Z-Wave plugin (openzwave) in Jeedom in inclusion mode
secure: just go to the Z-wave module management page
and click on the "Zwave Network" icon

![inclusion securise jeedom
1](../images/polycontrol.danalock/inclusion-securise-jeedom-1.jpg)

\

Then in the "Actions" tab click on: "ADD MODULE IN MODE
SECURE (INCLUSION) "

![inclusion securise jeedom
2](../images/polycontrol.danalock/inclusion-securise-jeedom-2.jpg)

\

> ** Important **
>
> We assume that you have installed the application on
> your smartphone or iphone and created an account. If it's not already
> done, you can refer to this page.

![inclusion](../images/polycontrol.danalock/inclusion.jpg)

![inclusion1](../images/polycontrol.danalock/inclusion1.jpg)

![inclusion2](../images/polycontrol.danalock/inclusion2.jpg)

In the app click on "Smart home" then on "Z-wave" and finally
on "CONNECT".

Once included you should get this:

\

![Plugin Zwave](../images/polycontrol.danalock/information.jpg)

\

### Orders

\

Once the module is recognized, the commands associated with the module will be
available.

\

![Commandes](../images/polycontrol.danalock/commandes.jpg)

\

Here is the list of orders:

\

-   Status: this is the command that will trace the last action
    executed (open / close)

-   Open: this is the command that opens the lock

-   Close: this is the command that closes the lock

-   Battery: it's the battery control

\

### Module configuration

\

> ** Warning **
>
> Although this module is battery-powered, it uses Flirs technology.
> That means he has no concept of wake up and wake up. he
> will recover all configuration changes in near real time
> as a mains module.

\

If you want to configure the module according to your
installation, it is necessary to go through the "Configuration" button of the
OpenZwave plugin from Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

You will arrive on this page (after clicking on the tab
settings)

\

![Config1](../images/polycontrol.danalock/bouton_configuration.jpg)

\

Parameter details:

\

-   1: Direction 0-1: 0 = The motor goes clockwise
    locked, 1 = The motor goes counter-clockwise when
    Locked

-   2: Speed ​​1 = slowest, 2 = slow, 3 = normal, 4 = fast, 5 = the
    faster

-   3: Mode 1 = Motor drive (energy saving), 2 = mode
    Complete training (Normal)

-   4: Number of turns (1 = 10 degrees, 9 = 90 degrees, etc.)

-   5: Auto lock 0-60 How many seconds from when
    the lock has been unlocked to automatically close
    again. If 0, it is disabled.

-   6: Disable or enable the lock sound signal or
    unlock (0 = Disable, 1 = Enable.)

-   7: Battery Type: Set the type of battery that
    feeds the device.

-   8: Battery alarm: When the battery level is lower
    at this value, the device will inform the user with a signal
    sound after locking or unlocking.

-   9: Turn & Go 0 = Turn & Go Off, 1 = Turn & Go On. Latch & Go
    will turn the handle automatically when
    manually operate it.

-   10: Brake & GoBack 0 = Disabled. 1½ seconds to brake. When
    it is used the lock brakes for x amount of seconds and then
    return to 75 degrees back. Designed for special doors
    without lever. (Only when unlocking).

-   11: Async 0 = Async off, 1 = Async On. When async is enabled
    lock will be automatically calibrated if it is already unlocked and
    Unlock again (used for locks of
    special door).

-   12: operation report

\

### Groups

\

This module has only one association group.

\

![Groupe](../images/polycontrol.danalock/groupe.jpg)

\

Good to know
------------

\

### Specificities

\

> ** Tip **
>
> Although this module is battery-powered, it uses Flirs technology.
> That means he has no concept of wake up and wake up. he
> will recover all configuration changes in near real time
> as a mains module.

\

> ** Tip **
>
> This module returns its status if you operate the lock by hand
> the status will be updated. \

### Alternative visual

\

![vuewidget](../images/polycontrol.danalock/vuewidget.jpg)

\

Wakeup
------

\

There is no concept of wake up for this module.

\

F.A.Q.
------

\

No concept of wake up on this module; read the section Specificities.

\

** @ ** noumea
