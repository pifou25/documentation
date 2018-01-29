Why ?
==========

-   Apache will gradually become the norm with Jeedom

-   Allows you to have the latest security updates at
    access to files (thanks to .htaccess) during updates of
    Jeedom

-   Corrects some issues of access and stability (especially for those
    who have a lot of cameras)

-   Improves the overall performance of Jeedom.

Prerequisites
=========

-   Know how to connect in SSH on the box (you will find the
    identifiers on the installation documentation)

-   Being connected to the internet.

> **Important**
>
> In case of concern the Jeedom team can not be held responsible and
> may refuse any request for support. Handling is yours
> risks and perils.

> **Important**
>
> Warning some unofficial plugins are not compatible
> Apache, find out well before.

How to do
=============

Disabling Jeedom and nginx services
------------------------------------------

In Jeedom, you have to go to each plugin with a daemon, then
disable the automatic management of the daemon and cut it. It is necessary
Then, in the task engine, disable all tasks (there is a
general deactivation button) and in the scenarios, disable all
the scenarios (there is a general deactivation button).

    systemctl stop cron
    systemctl stop nginx
    systemctl stop mysql

Apache installation and configuration
--------------------------------------

    mkdir -p / var / www / html / log
    apt-get -y install ntp ca-certificates unzip curl sudo
    apt-get -y install apache2 php5 mysql-client mysql-server libapache2-mod-php5
    apt-get -y php5-php5-php5-php5-php5-php5-php5-php5
    wget https://raw.githubusercontent.com/jeedom/core/stable/install/apache_security -O /etc/apache2/conf-available/security.conf
    rm /etc/apache2/conf-enabled/security.conf
    ln -s /etc/apache2/conf-available/security.conf / etc / apache2 / conf-enabled /
    rm /etc/apache2/conf-available/other-vhosts-access-log.conf
    rm /etc/apache2/conf-enabled/other-vhosts-access-log.conf
    systemctl restart apache2
    rm /var/www/html/index.html

> **Note**
>
> If during the installation the system asks you if you want or
> do not keep a modified version of a file, do: "Keep the local
> currently installed version ".

Copy of Jeedom
---------------

    cp -R / usr / share / nginx / www / jeedom / * / var / www / html /
    rm /var/www/html/log/nginx.error
    chmod 775 -R / var / www / html
    chown www-data: www-data-R / var / www / html

Access test
------------

    systemctl start mysql

You should now be able to access Jeedom from the same URL
before. If it's good you can continue ELSE IT NEEDS ESPECIALLY
NOT DO MORE.

Update of the crontab
-------------------------

Make :

    crontab -e

Then update the path to Jeedom, replace:

    * * * * * su --shell = / bin / bash - www -data -c '/ usr / bin / php /usr/share/nginx/www/jeedom/core/php/jeeCron.php' >> / dev / null 2> & 1

By :

    * * * * * su --shell = / bin / bash - www -data -c '/ usr / bin / php /var/www/html/core/php/jeeCron.php' >> / dev / null 2> & 1

Cleaning and removal of nginx
---------------------------------

    apt-get remove nginx *
    rm -rf cp -r / usr / share / nginx
    apt-get autoremove
    systemctl disable nginx

Restarting services
------------------------

    systemctl enable apache2
    systemctl start cron

Then connect to your Jeedom and reactivate the task engine
and scenarios. You can also restart the demons.

> **Important**
>
> It is recommended after the migration to launch an update of
> Jeedom (even if he does not offer you anything).
