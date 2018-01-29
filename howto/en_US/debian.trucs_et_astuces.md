Useful packages
==============

Here are some useful packages to put on a blank installation:

-   **fail2ban**: Bans IPs trying to connect
    to the machine.

-   **vim**: It's a command-line text editor, you can
    also replace it with nano or others.

-   **net-tools**: collection of programs to manage the network

-   **dos2unix**: text conversion tool

<! - ->

    apt-get install -y vim fail2ban net-tools dos2unix

If you are on VMware, you can add additional tools
:

    apt-get install -y open-vm-tools

Colorize the console
====================

If you want your console (bash) to use colors:

    rm -rf /root/.bashrc
    wget https://raw.githubusercontent.com/jeedom/core/stable/install/bashrc -O /root/.bashrc
    dos2unix /root/.bashrc

Allow root login in SSH
==================================

You have to edit the file / etc / ssh / sshd \ _config and change:

    PermitRootLogin without-password

By :

    PermitRootLogin yes

> **Important**
>
> Make sure you use a strong root password! The use of
> fail2ban is also recommended.

Mount a Samba share
=======================

Installing the cifs package

    apt-get install -y cifs-utils

Create the mount point:

    mkdir / mnt / my_share

> **Note**
>
> Il faut adapter mon\_partage en fonction de votre besoin

Addition of editing in / etc / fstab

    // IP_SERVER_SAMBA / my_share / mnt / my_share cifs uid = 0, rw, user = TODO, password = TODO 0 0

> **Note**
>
> You have to change the TODOs by your linux username and your
> password

Passage from Jessie to Stretch
===========================

For testing the upgrade and Stretch installation with restore
backup, I confirm that the installation of Stretch by
crushing will save you time.

-   **Method 1: Installation of Stretch:** 1 to 2 hours max max, and
    especially a clean operating system.

-   **Method 2: Jessie's update to Stretch:** half a day to
    to wipe the bugs.

Method 1: Installing Stretch and Restoring Backup
-------------------------------------------------- ---------------

Before you begin, make a full backup via Jeedom of your
installation under Jessie, then export the backup to another
storage medium.

> **Tip**
>
> Download the backup other than through the web interface (SSH, FTP,
> SAMBA, others of your choice), because if your archive is voluminous
> It can easily be corrupted via an HTTP download.
> However, if it's less than 100MB, it's playable.

-   Install Debian Stretch on your box.

-   Reconfigure your local network, check that your machine is
    operational and up to date.

-   Install Jeedom by following the doc:
    <Https://github.com/jeedom/documentation/blob/master/installation/fr_FR/other.asciidoc>

\ [WARNING \] MariaDB no longer allows access to the 'root' profile, which means
can block the restoration of a database that you would have
changed the name (like me) so we do not restore immediately the
backup. If the user 'jeedom' does not have the correct permissions, the
restore will fail.

Reference:
<Http://jc.etiemble.free.fr/abc/index.php/realisations/trucs-astuces/deb9php7>
(chapter 5a)

In short, 2 lines of commands to allow the user 'root' in
MYSQL, under Stretch:

    $ mysql -u root -p mysql
    Enter password:
    Welcome to the MariaDB monitor. Commands end with; or \ g.
    Your MariaDB connection id is 2
    Server version: 10.1.21-MariaDB-5 Debian 9.0
    Copyright (c) 2000, 2016, Oracle, MariaDB Corporation Ab and others.
    Type 'help;' or '\ h' for help. Type '\ c' to clear the current input statement.

    MariaDB [mysql]>
    MariaDB [mysql]> GRANT ALL PRIVILEGES ON *. * TO root @ 'localhost' IDENTIFIED BY 'mypass';
    Query OK, 0 rows affected (0.00 sec)
    MariaDB [mysql]> exit;
    Bye

> **Tip**
>
> Replace 'monpass' with your MYSQL password used for the
> root account under "Debian 8 - Jessie". I give rights to root
> especially to manage my bases with 'PHPMYADMIN', but to give them to
> the user MYSQL 'jeedom' must suffice.

> **Tip**
>
> You will find the password mode of the user MYSQL Jeedom here:
> Administration → Configuration → OS / DB → Database

It's up to you to adapt this command according to your configuration
former :

    GRANT ALL PRIVILEGES ON *. * TO root @ 'localhost' IDENTIFIED BY 'monpass';

or

    GRANT ALL PRIVILEGES ON *. * TO jeedom @ 'localhost' IDENTIFIED BY 'monpass';

-   Copy your backup to the `/ var / www / html / backup` folder

-   Give rights to www-data:
    `chown -R www-data: / var / www / html / backup / *`

-   Launch the restore via the Jeedom interface (Administration →
    Backups → Local Backups: Choose the right backup
    and click **Restore** just below)

-   Wait during the restoration

-   Give back rights to www-data on any Jeedom:
    `chown -R www-data: / var / www / html /`

-   Restart the box: `reboot`

-   Connect to Jeedom with your old credentials via
    the web interface

-   Pass on each plugin to reinstall the dependencies (especially
    on those where the daemon is "NOK" KO).

Method 1: Upgrade (less chance of success)
-----------------------------------------------

Update of the OS in Jessie version.

    apt-get -y update
    apt-get -y upgrade
    apt-get -y dist-upgrade

You have to edit the file /etc/apt/sources.list and replace all
Jessie by Stretch, with prior file backup, by doing:

    cp /etc/apt/sources.list /etc/apt/sources.list_backup
    sed -i 's / jessie / stretch / g' /etc/apt/sources.list

Update of the OS in Stretch version.

    apt-get -y update
    apt-get -y upgrade
    apt-get -y dist-upgrade

Flip in MariaDB.

    apt-get -y install mariadb-server mariadb-customer mariadb-common

Update of Jeedom

    sh /var/www/html/install/install.sh -s 2
    sh /var/www/html/install/install.sh -s 5
    sh /var/www/html/install/install.sh -s 7
    sh /var/www/html/install/install.sh -s 10

Deleting unnecessary libraries

    apt -y remove `aptitude -F %p search '~ o' | grep -E -v ^ lib`
    apt -y remove `aptitude -F %p search '~ o'` ----
