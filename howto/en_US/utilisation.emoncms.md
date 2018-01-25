EmonCMS is a PHP energy monitoring application (Emon:
Energy Monitor)

With regard to data sharing between Jeedom and EmonCMS (in
one way or the other), you will find in this documentation the means
to implement it.

A brief memo to install emoncms is also proposed (this
installation is not currently offered natively in Jeedom)

EmonCMS can be installed next to Jeedom or elsewhere. You can
even use the emoncms.org instance

Send Jeedom value to EmonCMS
=========================================

To send a value of Jeedom to EmonCMS, the simplest solution
since it is available natively is to use the push URL of a
information

In Jeedom, you can access the advanced parameters by clicking on the
notched wheel on the right.

Then in "Advanced configuration", we find the last parameter
Push URL, it must be filled with the EmonCMS API address for the feed
we want to fill

The url of push is of the form:

[https: //serveur/emoncms/input/post.json json = {power: \ # value \} & # apikey = xxx](https://serveur/emoncms/input/post.json?json={power:#value#}&apikey=xxx)

With the parameters:

-   id: the id of the feed found on emoncms

-   apikey: the API key of read & write for emoncms

-   value: you have to leave * value * for Jeedom to send the
    value of the info

-   power: it is to modify for

Notification to Jeedom or recovery from Jeedom
================================================== ====

To take a piece of emoncms in Jeedom, there are two possibilities
:

-   The first is to create an info via the script plugin in Jeedom
    and use the API URL of the feed. This method requires to recover
    the value regularly or via scenario for example and normally
    not useful because the data has its source in jeedom \ _setting

        https: //serveur/emoncms/feed/value.json id = 1 & apikey = xxx?

-   The second possibility is to use the emoncms Event plugin
    to trigger an action on certain conditions. This method
    could be useful if we have a data that is calculated or
    directly retrieved by emoncms (eg OpenBEM) With
    the advantage of notifying when needed, against the plugin
    event does not allow to push and it will go through MQTT
    for the Jeedom connection

Memo for EmonCMS installation
================================

The installation is described on this page github:

<Https://github.com/emoncms/emoncms/blob/master/docs/LinuxInstall.md>

Note that some plugins seem obsolete with the latest version
EmonCMS (v9 at the end of 2015)

If we install them, there are problems with the menus. Anyway,
we only need to:

git clone <https://github.com/emoncms/event.git> (He will be able to
allow to create reactions on event in emoncms for
to notify Jeedom)

git clone <https://github.com/emoncms/openbem.git> (This is a plugin for
track energy consumption of the house)

git clone <https://github.com/emoncms/energy.git>

git clone <https://github.com/emoncms/report.git>

git clone <https://github.com/elyobelyob/mqtt.git>

Nginx configuration
===================

Here is an example configuration for Nginx. For Apache there is no
need to conf particular a classic repertoire

    location / emoncms {
           alias / var / www / emoncms /;
           index index.php;
            try_files = $ uri $ uri / @missing;

       location ~ [^ /] \. php (/ | $) {
               fastcgi_split_path_info ^ (. +? \. php) (/.*) $;
               fastcgi_pass unix: /var/run/php5-fpm.sock;
               fastcgi_index index.php;
               include fastcgi_params;
               fastcgi_param REMOTE_USER $ remote_user;
               fastcgi_param PATH_INFO $ fastcgi_path_info;
               fastcgi_param SCRIPT_FILENAME /var/www/emoncms/index.php;
           }

    }

    location @missing {
            rewrite ^ / emoncms /(.*)$ /emoncms/index.php?q=$1&$args last;
    }
