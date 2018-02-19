Veremos cómo actualizar manualmente
Jeedom, a través de la consola SSH.

Requisitos previos
=========

-   si SSH en Jeedom

-   SSH conoce la contraseña (véase el documento de instalación)

-   tener acceso a Internet desde el cuadro de Jeedom

> **Importante**
>
> Recuerde que para hacer y exportar una copia de seguridad antes de actualizar
> Manual.

Descargar y descomprimir
===============================

SSH, utilice:

    sudo su -
    cd /root
    wget https://github.com/jeedom/core/archive/stable.zip
    unzip stable.zip
    cp -R core-stable/* /var/www/html
    cp -R core-stable/.[^.]* /var/www/html

Actualización
===========

También en SSH:

    sudo su -
    modo php /var/www/html/install/update.php = resistencia
    chmod -R 775 / var / www / html
    chown www-data: www-data -R / var / www / html

> **Importante**
>
> Si su instalación de Jeedom es un poco viejo, reemplace
> Todos los / var / www / html / usr / share / nginx / www / jeedom
