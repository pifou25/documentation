Description
===========

There are two ways to save Jeedom and each has some
advantages and disadvantages.

It is possible to make a backup from the interface
Jeedom. This concerns only the Jeedom software and its data.
It has the advantage of being made hot and the file of
backup can be exported to other media.

It is also possible to make a backup by making an image
microSD card disc (mini and mini +). This way has the advantage
to be a complete backup of the system as well as of Jeedom and its
data. However, it must be done by switching off Jeedom and
plugging the microSD card into another computer.

The best way to be quiet is to use both: Make a
save the microSD card from time to time and schedule a
regular backup of Jeedom.

> **Tip**
>
> The microSD recovery procedure can be useful for
> restore a default Jeedom from the image provided by
> the team see
> [here] (https://www.jeedom.fr/doc/documentation/installation/fr_FR/doc-installation.html).

Jeedom Backup / Restore
=================================

Une documentation est déjà présente pour expliquer la page
Administration→Sauvegardes. Vous la trouverez
[ici](https://jeedom.github.io/core/fr_FR/backup).

Backup / Restore the microSD card
===========================================

Preparations
-----------

These backups / restorations are realized from another
computer to make a "clean image" of the SD card. It takes in
first stop the mini +. To do this, switch to Jeedom mode
Expert in the user menu at the top right.

![save restore06](../images/save-restore06.jpg)

And click on Exit

![save restore07](../images/save-restore07.jpg)

Then, take the microSD card out of the mini + and connect it to
your computer via an adapter / card reader / ...

![save restore08](../images/save-restore08.jpg)

Windows
------------

It will start by downloading third-party software for example:
[Win32 Disk Imager] (http://sourceforge.net/projects/win32diskimager/)

1.  **Backup**

    -   Launch the software and check that the letter below
        * Device * matches that of your card / reader
        Map.

    -   In the * Image File * field, specify the name of the image file that
        you want to create as well as where it will be saved.

    -   Finally, click on the * Read * button to create the image.
        Image :: ../ images / save-restore09.jpg \ [align = "center" \]

2.  **Restoration**

    -   Launch the software and check that the letter below
        * Device * matches that of your card / reader
        Map.

    -   In the * Image File * field, go to the image file
        you want to restore.

    -   Finally click on the * Write * button, in order to restore this
        image on the microSD card.

![save restore10](../images/save-restore10.jpg)

Under MacOSX
-----------

For your convenience, you can download the software
[ApplePi Baker] (http://www.tweaking4all.com/hardware/raspberry-pi/macosx-apple-pi-baker/)

![save restore11](../images/save-restore11.jpg)

1.  **Backup**

    -   With ApplePi-Baker: Select the right card from the list
        * Pi-Crust *, and click * Create Backup * to create a
        image file of your microSD card.

    -   In shell command:

        -   In order to find the disc corresponding to the card, open
            a terminal and enter the command: `diskutil list`
            Image :: ../ images / save-restore12.jpg \ [align = "center" \]

        -   Start the creation of the image by entering the command:
            `sudo dd if = / dev / disk1 of = ~ / Desktop / Backup_Jeedom.img bs = 1m`
            * Note: In this example, the disk name of the card
            is `/ dev / disk1`, so you have to enter in the command of
            backup \ `/ dev / disk1 \` *

2.  **Restoration**

    -   With ApplePi-Baker: Select the right card from the list
        * Pi-Crust *, put the path to the image file to restore
        in the * IMG file * field of the * Pi-Ingredients * section, and
        click * Restore Backup * to restore the image to the
        microSD card.

    -   In shell command:

        -   In order to find the disc corresponding to the card, open
            a terminal and enter the same command as for the
            backup: `diskutil list`

        -   Unmount the partitions of the card by typing the command:
            `sudo diskutil unmountDisk / dev / disk1`

        -   Restore the image on the microSD card by typing the command
            :
            `sudo dd bs = 1m if = ~ / Desktop / Backup_Jeedom.img of = / dev / disk1`
            * Note: In this example, the disk name of the card
            is `/ dev / disk1`, so you have to enter in the command of
            backup \ `/ dev / disk1 \` *

On Linux
----------

1.  **Backup**

    -   In order to find the disc corresponding to the card, open a
        terminal and enter the command: `sudo fdisk -l | grep Dis`

        ``` {.bash}
        $ sudo fdisk -l | grep Dis
        Disk /dev/sda: 320.1 GB, 320072933376 bytes
        Disk /dev/sdb: 16.0 GB, 16012804096 bytes
        Disk /dev/sdc: 8.0 GB, 8006402048 bytes
        ```

    -   Start the creation of the image by entering the command:
        `sudo dd if = / dev / sdc of = Backup_Jeedom.img bs = 1m` * Note: In
        this example, the disk name of the card is /dev/sdc.*

2.  **Restoration**

    -   In order to find the disc corresponding to the card, open a
        terminal and enter the command: `sudo fdisk -l | grep Dis`

    -   Unmount the partitions of the card by typing the command (in
        replacing the X by the numbers of the partitions):
        `sudo umount / dev / sdcX`

    -   Restore the image on the microSD card by typing the command:
        `sudo dd if = Backup_Jeedom.img of = / dev / sdc bs = 1m` * Note: In
        this example, the disk name of the card is /dev/sdc.*


