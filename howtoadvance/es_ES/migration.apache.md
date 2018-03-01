Por qué ?
==========

-   Apache poco se convertirá en la norma con Jeedom

-   Deja para tener las últimas actualizaciones de seguridad en
    el acceso de archivos (a través de .htaccess) durante las actualizaciones
    Jeedom

-   Corrige algunos problemas de acceso y la estabilidad (especialmente para aquellos
    que tienen un montón de cámaras)

-   Mejora el rendimiento global de Jeedom.

Requisitos previos
=========

-   Saber cómo conectar a través de SSH en la caja (encontrará
    IDs en la documentación de la instalación)

-   Al estar conectado a Internet.

> **Importante**
>
> En caso de problemas del equipo Jeedom no se hace responsable,
> Refuseany solicitud de soporte. El manejo es su
> Riesgos.

> **Importante**
>
> Cuidado con algunos plugins no oficiales no son compatibles
> Apache, preguntar antes.

Como hacer
=============

Desactivar los servicios Jeedom y nginx
------------------------------------------

En Jeedom, ir en cada plugin con un demonio, a continuación,
desactivar daemon gestión automática y corte de los mismos. Hay que
Luego, en las tareas motoras, desactivar cualquier tarea (hay una
botón de desactivación general) y los escenarios, desactivar todos
escenarios (hay un botón de desactivación en general).

    systemctl cron parada
    systemctl nginx parada
    systemctl MySQL parada

Instalación y configuración de Apache
--------------------------------------

    mkdir -p / var / www / html / registro
    apt-get -y install NTP ca-certificados descomprimir sudo rizo
    apt-get -y install apache2 php5 mysql-cliente-servidor MySQL libapache2-mod-php5
    apt-get -y install php5-cli php5-common php5-rizo php5-FPM php5-json php5-mysql php5-gd
    Wget https://raw.githubusercontent.com/jeedom/core/stable/install/apache_security -O /etc/apache2/conf-available/security.conf
    /etc/apache2/conf-enabled/security.conf rm
    /etc/apache2/conf-available/security.conf ln -s / etc / apache2 / conf-activado /
    /etc/apache2/conf-available/other-vhosts-access-log.conf rm
    /etc/apache2/conf-enabled/other-vhosts-access-log.conf rm
    systemctl reiniciar apache2
    /var/www/html/index.html rm

> **Nota**
>
> Si durante la instalación se le preguntará si desea o
> No conservar una versión modificada de un archivo, hacer: "Mantener los locales
> Versión instalada".

Copia de Jeedom
---------------

    cp -R /usr/share/nginx/www/jeedom/* /var/www/html/
    cp -R /usr/share/nginx/www/jeedom/.[^.]* /var/www/html/
    rm /var/www/html/log/nginx.error
    chmod 775 -R /var/www/html
    chown www-data:www-data -R /var/www/html

Acceso de prueba
------------

    systemctl iniciar MySQL

Ahora debería ser capaz de acceder a la misma URL desde Jeedom
antes. Si es bueno se puede continuar más haga MOSTLY
NO LA SUITE.

La actualización del crontab
-------------------------

Hacer :

    crontab -e

A continuación, actualizar la ruta a Jeedom, reemplace:

    * * * * * Conocía --shell = / bin / bash - -c www-data '/ usr / bin / php /usr/share/nginx/www/jeedom/core/php/jeeCron.php' >> / dev / null 2> & 1

por:

    * * * * * Conocía --shell = / bin / bash - -c www-data '/ usr / bin / php /var/www/html/core/php/jeeCron.php' >> / dev / null 2> & 1

La limpieza y la eliminación de nginx
---------------------------------

    apt-get remove nginx *
    rm-rf cp -R / usr / share / nginx
    apt-get autoremove
    systemctl desactivar nginx

Reinicio de los servicios
------------------------

    systemctl permitir apache2
    systemctl iniciar cron

A continuación, conectarse a su Jeedom y volver a activar el motor de tareas
y escenarios. También puede reiniciar los demonios.

> **Importante**
>
> Se recomienda después de la migración a lanzar una actualización
> Jeedom (incluso si no ofrece nada).
