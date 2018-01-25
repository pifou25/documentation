We will see here how to manually update on
Jeedom, via the SSH console.

Prerequisites
=========

-   to know how to connect in SSH to Jeedom

-   know the SSH identifiers (see installation documentation)

-   have Internet access from the Jeedom box

> ** Important **
>
> Remember to make and export a backup before any update
> manual.

Download and decompression
===============================

In SSH, do:

    sudo su -
    cd / root
    wget https://github.com/jeedom/core/archive/stable.zip
    unzip stable.zip
    cp -R core-stable / * / var / www / html

Update
===========

Always in SSH:

    sudo su -
    php /var/www/html/install/update.php mode = force
    chmod 775 -R / var / www / html
    chown www-data: www-data-R / var / www / html

> ** Important **
>
> If your installation of Jeedom is old, you have to replace
> all / var / www / html by / usr / share / nginx / www / jeedom
