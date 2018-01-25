We will see here how to migrate an installation with Jeedom mode
slave to a Jeedom with the plugin "Jeedom Link". Slave mode
Jeedom being dropped from Jeedom to version 3.0, he is
necessary to proceed before migration to the new mode of
operation.

Preparation before migration
===========================

> ** Warning **
>
> It is important to read all of this documentation before
> get started in the migration. Important information regarding
> the prerequisites for updating, backup and recovery
> information is essential for the proper understanding of
> the operation to be carried out. Refraining from reading this documentation may
> cause destructive operations on your installation. If you
> do not understand a point, do not hesitate to ask questions about the
> forum before starting the procedure!

> ** Important **
>
> Be careful not to loop equipment in
> configuring the "Jeedom Link" plugin. For example, do not do a
> Equipment-X in a Jeedom1 that goes back in a Jeedom2 then goes back
> again in the Jeedom1. This could bring down your Jeedoms!

> ** Note **
>
> For a better reading and understanding of this tutorial, here are the
> terms used: \
> \
> - ** Jeedom Target **: Server (your old Jeedom Master) who
> centralizes the equipment of ** Jeedom (s) Source (s) ** \
> The screenshots on a black background correspond to the ** Jeedom Target **.
> \
> - ** Jeedom Source **: Server (your old Jeedom Slave (s))
> which puts your equipment back on the ** Jeedom Target **.
> \
> - The notions of ** Jeedom Master ** and ** Jeedom Esclave ** are no longer
> news. The new synchronization mode of operation
> Equipment between several Jeedoms can be bidirectional. A
> Jeedom server can now be ** Source ** and ** Target ** while
> the old fashion allowed only the reassembly of the equipment of
> ** the Slave ** to ** the Master **. With the new mode it is also
> possible to have several ** Jeedom Targets ** for the same ** Jeedom
> Source **. Communication between Jeedoms can now also
> be done remotely via internet (DNS Jeedom or other). \
> \

![jeelink.migration9](../images/jeelink.migration9.png)

Updates and Configuration Check
------------------------------------------------

-   Update ** Jeedom Master ** to the latest version (even if
    no update is offered).

-   Update the ** Jeedom Maître ** plugins to the latest
    versions available.

-   Check in the Health page that the internal network configuration of the
    ** Jeedom Master ** is OK (and external if your ** Jeedoms Sources **
    will be distant).

Gathering useful information
-------------------------------------

Depending on the plugins installed on your ** Jeedom Esclave **, it is
necessary to retrieve the following information:

### Zwave Plugin

-   In the health page of the Zwave plugin on the ** Jeedom Master **, choose
    your ** Slave ** in the drop-down menu and make a screenshot,
    this in order to have a list of the equipment that comes
    of it.

-   Note for each equipment coming from ** Slave **: the object
    parent, the name, the ID (Node), the template.

-   Recover the Zwcfg file: * Plugins ⇒ Plugins management ⇒
    Z-Wave *. Click on the red button * Zwcfg * and copy the content
    in a text file on your computer.

### RFXcom plugin

-   Note for each equipment coming from ** Slave **: the object
    parent, name, ID (Logic), Type, Model.

> ** Note **
>
> A non-exhaustive sheet of information to note for the migration
> is available [here] (../ images / MemoMigration.xls)

Preventive backups
-----------------------

-   Make a [backup
    Jeedom] (https://jeedom.github.io/documentation/core/fr_FR/doc-core-backup.html)
    of your ** Jeedom Master ** and your ** Jeedom Slave (s) **
    and recover the one (s) on your PC / NAS ....

-   Make a [backup
    SD / Disk] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-sauvegarde.comment_faire.html#_sauvegarde_restauration_de_la_carte_microsd)
    of your ** Jeedom Master ** and your ** Jeedom Slave (s) **
    and recover them on your PC / NAS ....

Migration
=========

> ** Note **
>
> Do not remove the old equipment for the moment
> ** Slave ** on ** the Master **.

Install and activate the "Jeedom Link" plugin on the ** Jeedom Target ** (old Master).
-------------------------------------------------- -----------------------------------

On your ** Jeedom Target **, * Plugins ⇒ Plugins Management *:

![jeelink.migration1](../images/jeelink.migration1.png)

Installation of ** Jeedom Source **:
-----------------------------------

> ** Note **
>
> if you have an extra Raspberry Pi and another card
> SD, you can migrate one protocol after the other in
> installing a new ** Jeedom Source ** in parallel without having to
> touch your existing ** Jeedom Slave **. By obviously moving
> as and when possible controllers from one to the other.

> ** Warning **
>
> If you use your existing RaspberryPi, please be certain
> to have followed the chapter of this documentation.

> ** Note **
>
> if you are using the existing Raspberry Pi which is currently a
> ** Jeedom Slave **, we advise you to use a card
> SD / microSD new. This will allow you to backtrack
> easily if needed.

-   Install a new Jeedom on a new SD card (whatever it is
    to put in your existing ** Jeedom Slave ** or for a
    new Raspberry Pi) by following the [documentation
    Installation] (https://jeedom.github.io/documentation/installation/fr_FR/doc-installation.html).

-   Update the ** Jeedom Source ** to the latest version (even if
    no update is offered).

-   Check in the Health page that the internal network configuration (and
    external if needed) ** Jeedom Source ** is OK.

Jeedom Source Configuration
------------------------------

-   Change the password of the admin user or / and configure a
    New user.

-   Set Up Your Jeedom Market Account (* Configuration ⇒ Updates
    and files ⇒ "Market" tab *). Click on test after having
    saved, to validate the entry of your identifiers
    Jeedom Market).

-   Installation and activation of the "Jeedom Link" plugin on the new
    ** Jeedom Source **.

![jeelink.migration2](../images/jeelink.migration2.png)

-   Install and activate the plugins you want to use.
    (It is advisable to do them one by one, checking each
    once dependencies and possible daemons are OK).

-   Recreate the tree of objects (just the ones that will get you
    to be useful) of the ** Jeedom Target ** (Old Master) on your new
    ** Jeedom Source ** (Old Slave).

Equipment configuration on ** Jeedom Source **
-------------------------------------------------- ----

To proceed with the sending of equipment present on ** Jeedom Source **
to the ** Jeedom Target ** via the "Jeedom Link" plugin, it is necessary
that the latter is already operational on your new ** Jeedom
Source**.

> ** Note **
>
> Thinking as you go to disable the logging of commands
> info of each equipment on ** Jeedom Source ** so
> to save the SD card of it (The historization will be done on the
> ** Jeedom Target **).

> ** Note **
>
> You can also, as and when assigning equipment to
> objects recreated on the ** Jeedom Source ** so that they are later
> automatically put in the right object on the ** Jeedom Target ** when
> the declaration in the "Jeedom Link" plugin. In case of duplicate name
> with equipment already present in the ** Jeedom Cible ** items,
> the plugin will add "remote XXXX" to the name of the device.

### Zwave plugin:

-   Click on the "Synchronize" button to retrieve the modules
    associated with your controller. (They are kept in the memory
    of it)

-   Replace the * Zwcfg * file: * Plugins ⇒ Plugin Management ⇒
    Z-Wave *. Click on the red button * Zwcfg * and paste the contents of the
    text file previously created on your computer. *Save
    changes*.

-   Rename your modules and place them in the desired objects in you
    helping with your migration memo.

### Rfxcom plugin:

#### Probes, sensors, detectors, ...:

-   Pass the plugin in inclusion mode.

-   Repeat the inclusion until you have all your equipment
    this type.

-   Rename your equipment and place it in the desired objects in
    helping you with your migration memo.

#### Actuators, plugs, .... :

-   Add new equipment.

-   Define name, ID, parent object, equipment type, and
    model by helping you from your migration memo.

-   Repeat for all your equipment of this type.

Configuration of the "Jeedom Link" plugin
-------------------------------------

The "Jeedom Link" plugin installed on the ** Jeedom Source ** will allow the
Climb equipment on the ** Jeedom Target ** (Your old Master).

> ** Note **
>
> Reminder, for a better reading and understanding of this tutorial: \
> \
> The screenshots on a black background correspond to the ** Jeedom Target **.
> \
> The screenshots on a white background correspond to ** Jeedom Source **. \

On the ** Jeedom Source **,
[Set] (https://jeedom.github.io/documentation/plugins/jeelink/fr_FR/jeelink)
the "Jeedom Link" plugin by specifying:

-   The name of ** Jeedom Target **.

-   The IP address or DNS name of the ** Jeedom Target **.

-   The ** Jeedom Target ** API Key.

And save the configuration.

![jeelink.migration3](../images/jeelink.migration3.png)

In the tab * Assignment *, add the equipment you want
go back to the ** Jeedom Target **.

![jeelink.migration4](../images/jeelink.migration4.png)

Click on * Add equipment * Select object and equipment
to add :

![jeelink.migration5](../images/jeelink.migration5.png)

Après avoir rafraîchit la page *Mes JeeLinks* du **Jeedom Cible**, vous
devez constater la création automatique de l’équipement :

![jeelink.migration6](../images/jeelink.migration6.png)

Like all Jeedom equipment, you can enable / disable and display
or not the equipment, its controls, ... or change the category:

![jeelink.migration7](../images/jeelink.migration7.png)

In the * Orders * tab, you access all the parameters of the
equipment orders:

![jeelink.migration8](../images/jeelink.migration8.png)

Historical recovery
----------------------------

> ** Note **
>
> To do on the ** Jeedom Target ** (Old Master) for each order
> info of the equipment of the old ** Slave ** which we want to recover
> the history.

-   Go to the configuration of the order (* Notched wheel to
    right*).

-   Go to the * Advanced Configuration * tab.

-   Click on the button * Copy the history of this command on a
    other order *.

-   Look for the corresponding command of the new JeeLink equipment
    corresponding and validate.

Replacing old slave devices in Scenarios / Virtual / ...
-------------------------------------------------- --------------------------

> ** Note **
>
> To do on the ** Jeedom Target ** (Old Master) for each order
> info / action of the equipment of the old ** Slave ** which one wants
> replace occurrences in scenarios / virtual / ....

-   Go to the configuration of the order (* Notched wheel to
    right*).

-   Go to the * Information * tab.

-   Click on the button * Replace this command with the command *.

-   Look for the corresponding command of the new JeeLink equipment
    corresponding and validate.

Retrieving advanced command display configurations
-------------------------------------------------- ----------------

> ** Note **
>
> To do on the ** Jeedom Target ** (Old Master) for each order
> info / action of the equipment of the old ** Slave ** which one wants
> recover advanced display settings.

-   Go to the configuration of the order (* Notched wheel to
    right*).

-   Click on the * apply to * button.

-   Search and select the corresponding order of the new
    corresponding JeeLink equipment and validate.

Copy of advanced command configurations
-------------------------------------------------

> ** Note **
>
> To do on the ** Jeedom Target ** (Old Master) for each order
> info / action of the equipment of the old ** Slave ** which one wants
> recover the advanced configuration.

-   No easy solution at this level, it will take two
    tabs / windows open on your browser.

-   Open orders for the equipment of the former ** Slave ** in a
    tab (Jeedom Target).

-   Open jeeLink equipment commands in the other tab
    (Target Jeedom).

-   And manually copy the desired parameters.

> ** Note **
>
> In order to avoid returning to the same order several times,
> operations 2.6 → 2.9 can be performed as a result on the same
> order before moving on to the next ones.

> ** Warning **
>
> Interactions on ** Jeedom Target ** can not be launched
> through equipment of a ** Jeedom Source ** transferred via the
> Jeedom Link plugin.

Household on the ** Jeedom Target **
==============================

> ** Note **
>
> After validating with certainty that your
> equipment / scenarios / interactions / virtual / .... function
> correctly with the new jeelink system, you can proceed to
> household.

-   Remove residual equipment from the old ** Jeedom Slave **.

-   Disable and remove plugins that are no longer useful
    (The ones you only had equipment on the Slave).

-   In the "Jeedom Link" plugin, rename the equipment that
    could have a name ending with "remote XXXX".

-   On the Jeedom Network page, delete the old ** Jeedom Slave **.


