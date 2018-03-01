paquetes de útiles
==============

Aquí están algunos paquetes de votos para poner en una instalación limpia:

-   Fail2ban ** **: Para expulsar IP intentar conectar
    máquina.

-   Vim ** **: Este es un editor de texto de línea de comandos, puede ser
    También reemplazar nano y muchos otros.

-   net-tools ** ** programas de recogida para gestionar la red

-   Dos2unix ** ** herramienta de conversión de texto

<! - ->

    aptitude install -y vim fail2ban de herramientas de red dos2unix

Si estás en VMware, puede agregar herramientas adicionales
:

    apt-get install -y-vm-herramientas abiertas

Colorear la consola
====================

Si desea que su consola (bash) utiliza colores:

    rm-rf /root/.bashrc
    Wget https://raw.githubusercontent.com/jeedom/core/stable/install/bashrc -O /root/.bashrc
    /root/.bashrc dos2unix

Permitir el acceso root a través de SSH
==================================

Debe editar el archivo / etc / ssh / sshd \ _CONFIG y el cambio:

    PermitRootLogin sin contraseña

por:

    PermitRootLogin sí

> **Importante**
>
> Asegúrese de utilizar una contraseña de raíz! El uso de
> También se recomienda Fail2ban.

Montar un recurso compartido Samba
=======================

Instalación del paquete CIFS

    apt-get install -y CIFS-utils

Crear el punto de montaje:

    mkdir /mnt/mon_partage

> **Nota**
>
> Mi \ _partage debe adaptarse para satisfacer sus necesidades

La adición de edición / etc / fstab

    //IP_SERVER_SAMBA/mon_partage /mnt/mon_partage cifs uid=0,rw,user=TODO,password=TODO 0 0

> **Nota**
>
> Es necesario cambiar el TODO por su nombre de usuario y su Linux
> Contraseña

Jessie paso Stretch
===========================

Después de probar la restauración de actualización y estiramiento de instalación
una copia de seguridad, confirmo que la instalación de un tramo
Crush le ahorrará tiempo.

-   **Método 1: instalar Stretch** 1 2 horas gran max, y
    especialmente un sistema operativo limpio.

-   **Método 2: Actualización a Jessie Tramo:** medio día
    limpie los insectos.

Método 1: Instalación de estiramiento y copia de seguridad restaurar
-------------------------------------------------- ---------------

Antes de empezar, hacer una copia de seguridad completa de la vía Jeedom
instalación bajo Jessie, a continuación, exportar la copia de seguridad a otro
medio de almacenamiento.

> **Tip**
>
> Descargar la copia de seguridad que no sea a través de la interfaz web (SSH, FTP,
> SAMBA, otros de su elección), ya que si su archivo es grande
> Se puede ser fácilmente dañado a través de descarga HTTP.
> Sin embargo, si es menos de 100 MB, que se puede jugar.

-   Instalación de Debian extiende tu caja.

-   Reconfigurar su red local, asegúrese de que su máquina está
    operativa y actual.

-   Instalar Jeedom siguiendo el doc:
    <Https://github.com/jeedom/documentation/blob/master/installation/fr_FR/other.asciidoc>

\ [ADVERTENCIA \] MariaDB ya no permite el acceso al perfil de 'root', que
puede bloquear la restauración de una base de datos que lo haría
cambiado el nombre (como yo) para que no se restablezca de inmediato la
copia de seguridad. Si el usuario 'jeedom' no tiene los permisos adecuados,
restauración fallará.

referencia:
<Http://jc.etiemble.free.fr/abc/index.php/realisations/trucs-astuces/deb9php7>
(Capítulo 5a)

En resumen, dos líneas de comando para permitir al usuario 'root'
MySQL bajo estiramiento:

    $ mysql -u root -p mysql
    Enter password:
    Welcome to the MariaDB monitor.  Commands end with ; or \g.
    Your MariaDB connection id is 2
    Server version: 10.1.21-MariaDB-5 Debian 9.0
    Copyright (c) 2000, 2016, Oracle, MariaDB Corporation Ab and others.
    Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

    MariaDB [mysql]>
    MariaDB [mysql]> GRANT ALL PRIVILEGES ON *.* TO root@'localhost' IDENTIFIED BY 'monpass';
    Query OK, 0 rows affected (0.00 sec)
    MariaDB [mysql]> exit;
    Bye

> **Tip**
>
> Reemplazar 'mypass' por su contraseña MySQL usada para
> Cuenta de raíz bajo la "Debian 8 - Jessie". Doy derechos a la raíz
> La inclusión de la gestión de mis bases con 'PHPMYADMIN', pero darles
> Usuario de MySQL 'jeedom' debería ser suficiente.

> **Tip**
>
> Encontrará el modo cambia de usuario de MySQL jeedom aquí:
> Administración → Configuración → OS / DB Base de datos →

Para encajar este comando dependiendo de la configuración
anterior:

    GRANT ALL PRIVILEGES ON *.* TO root@'localhost' IDENTIFIED BY 'monpass';

o

    GRANT ALL PRIVILEGES ON *.* TO jeedom@'localhost' IDENTIFIED BY 'monpass';

-   Copiar la copia de seguridad en `carpeta / var / www / html / backup`

-   Dar derechos a www-data:
    `Chown -R www-data / var / www / html / copia de seguridad / *`

-   Iniciar la restauración a través de la interfaz Jeedom (→ Administración
    Las copias de seguridad → copias de seguridad locales: Seleccione la copia de seguridad correcta
    y haga clic en Restaurar ** ** justo por debajo)

-   Espere a que la restauración

-   Devolverle los derechos a www-data en toda Jeedom:
    `Chown -R www-data / var / www / html /`

-   Reiniciar la caja: `reboot`

-   Iniciar sesión con su antigua contraseña a través de Jeedom
    la interfaz web

-   Roll en cada plugin para volver a instalar las dependencias (incluyendo
    esos o demonio es "NOK" KO).

Método 1: Actualización (menos posibilidades de éxito)
-----------------------------------------------

La actualización de la versión del sistema operativo de Jessie.

    apt-get -y update
    apt-get upgrade -y
    apt-get dist-upgrade -y

Debe editar /etc/apt/sources.list y reemplazar todos
Jessie estiramiento con el archivo de copia de seguridad antes, por:

    cp /etc/apt/sources.list /etc/apt/sources.list_backup
    sed -i 's / jessie / estiramiento / g' /etc/apt/sources.list

La actualización de la versión del SO estiramiento.

    apt-get -y update
    apt-get upgrade -y
    apt-get dist-upgrade -y

Cambia a MariaDB.

    apt-get -y install MariaDB-servidor MariaDB MariaDB cliente común

actualización Jeedom

    sh /var/www/html/install/install.sh -s 2
    sh /var/www/html/install/install.sh -s 5
    sh /var/www/html/install/install.sh -s 7
    sh /var/www/html/install/install.sh -s 10

Eliminación de bibliotecas innecesarias

    apto remove -y `-F %p aptitude search '~ o' | grep -E -v ^ lib`
    apto remove -y `-F %p aptitude search '~ ---- o'`
