Description
===========

The procedure will allow to connect in SFTP to your box so
to go get daily backups made by it.

> **Tip**
>
> Attention, so that this procedure works, it is necessary that
> the SSH server of the box is always functional.

Installing Filezilla
=========================

Filezilla is free software and available on all
platforms. It allows to transfer files via different
protocols (FTP, FTPS, SFTP ...) It is downloadable via this link:
<Https://filezilla-project.org/download.php?type=client>

Connection to the box
==================

To connect to your box, just fill in the fields
information at the top of the Filezilla window:

![restore filezilla01](../images/restore-filezilla01.jpg)

-   Host: IP address of Jeedom (sftp: // is added automatically)

-   Id: jeedom

-   Password: Mjeedom96

-   Port: 22

Then click on "Quick connection"

Navigation to the backup directory
===========================================

Once the connection is established, it is necessary to go to the
Jeedom backup directory.

2 cases of figures:

-   Apache server (Jeedom Smart Box): / var / www / html / backup

-   Nginx server (Box Jeedom Mini +):
    / Usr / share / nginx / www / jeedom / backup

The path is filled in the remote site part.

![restore filezilla02](../images/restore-filezilla02.jpg)

Downloading the backup
===============================

On the list of backups, by right-clicking, it is possible
to launch its download.

![restore filezilla03](../images/restore-filezilla03.jpg)
