descripción
===========

Hay dos maneras de ahorrar Jeedom y cada uno tiene
ventajas y desventajas.

Es posible realizar una copia de seguridad desde la interfaz
Jeedom. Sólo se refiere el software y los datos Jeedom.
Tiene la ventaja de ser hecho cálido y archivo
Copia de seguridad se puede exportar a otros medios de comunicación.

También es posible realizar una copia de seguridad al hacer una imagen
Disco de la tarjeta microSD (mini y mini +). Este enfoque tiene la ventaja
siendo una copia de seguridad completa del sistema, así como Jeedom y
datos. Por contra se debe realizar la desconexión y Jeedom
enchufar una tarjeta microSD a otro equipo.

La mejor manera de estar en silencio es utilizar dos: Hacer
tarjeta microSD copia de seguridad de vez en cuando y programar una
Jeedom copia de seguridad regular.

> ** Tip **
>
> El proceso de restauración de la tarjeta microSD puede ser útil para
> Jeedom restaurar un defecto de la imagen proporcionada por
> Vea el equipo
> [Aquí] (https://www.jeedom.fr/doc/documentation/installation/fr_FR/doc-installation.html).

Backup / Restore Jeedom
=================================

Documentación ya está presente para explicar la página
Administración → copias de seguridad. Puede encontrar
[Aquí] (https://github.com/jeedom/documentation/blob/master/howto/fr_FR/sauvegarde.comment_faire.asciidoc).

Copia de seguridad / restauración de la tarjeta microSD
===========================================

preparativos
-----------

Estos copia de seguridad / restauración se realizan desde otro
computadora para hacer un "auto-imagen" de la tarjeta SD. Se tiene en
La primera parada de mini +. Para ello, vaya modo de Jeedom
experto en el menú superior derecho de usuario.

![save restore06](../images/save-restore06.jpg)

Y haga clic en Turn

![save restore07](../images/save-restore07.jpg)

Entonces usted tiene que salir de la tarjeta microSD desde el mini + y conectarse a
ordenador a través de un lector / adaptador de tarjeta / ...

![save restore08](../images/save-restore08.jpg)

en Windows
------------

Se iniciará mediante la descarga de software de terceros, tales como:
[Win32 disco Imager] (http://sourceforge.net/projects/win32diskimager/)

1.  ** ** Respaldo

    -   Ejecutar el software y asegurarse de que la siguiente carta
        * Dispositivo * corresponde a la de su tarjeta / lector
        tarjeta.

    -   En el campo * * Imagen de archivo, especifique el nombre del archivo de imagen
        que desea crear y donde se guardará.

    -   Finalmente haga clic en el botón * Leer *, para crear la imagen.
        Imagen :: ../ images / save-restore09.jpg \ [align = "center" \]

2.  ** ** Alimentos

    -   Ejecutar el software y asegurarse de que la siguiente carta
        * Dispositivo * corresponde a la de su tarjeta / lector
        tarjeta.

    -   En el campo * * Archivo de Imagen, obtener el archivo de imagen
        que desea restaurar.

    -   Finalmente haga clic en el botón * Escribir * para restaurar este
        imagen en la tarjeta microSD.

![save restore10](../images/save-restore10.jpg)

MacOSX
-----------

Para su comodidad, se puede descargar el software
[ApplePi de Baker] (http://www.tweaking4all.com/hardware/raspberry-pi/macosx-apple-pi-baker/)

![save restore11](../images/save-restore11.jpg)

1.  ** ** Respaldo

    -   Con ApplePi panadero: Seleccionar la tarjeta correcta en la lista
        * Pi * corteza y haga clic en * * Crear copia de seguridad para crear una
        archivo de imagen a la tarjeta microSD.

    -   En shell de comandos:

        -   Para encontrar el disco que corresponda a la carta, abierto
            un terminal y escriba el comando: `list` diskutil
            Imagen :: ../ images / save-restore12.jpg \ [align = "center" \]

        -   Empezar a crear la imagen con el comando:
            `sudo dd if=/dev/disk1 of=~/Desktop/Backup_Jeedom.img bs=1m`
            * Nota: En este ejemplo, el nombre del disco del mapa
            est `/dev/disk1`, il faut donc saisir dans la commande de
            sauvegarde \`/dev/disk1\`*

2.  ** ** Alimentos

    -   Con ApplePi panadero: Seleccionar la tarjeta correcta en la lista
        * Pi * Corteza, establece la ruta del archivo de imagen para restaurar
        en el campo * IMG archivo * * Sección Pi-Ingredientes *, y
        * Click * Restaurar copia de seguridad para restaurar la imagen de la
        tarjeta microSD.

    -   En shell de comandos:

        -   Para encontrar el disco que corresponda a la carta, abierto
            un terminal de entrada y el mismo comando como para
            Copia de seguridad: `list` diskutil

        -   Retire el mapa de particiones escribiendo:
            `sudo diskutil unmountDisk /dev/disk1`

        -   Restaurar la imagen en la tarjeta microSD escribiendo el comando
            :
            `sudo dd bs=1m if=~/Desktop/Backup_Jeedom.img of=/dev/disk1`
            * Nota: En este ejemplo, el nombre del disco del mapa
            est `/dev/disk1`, il faut donc saisir dans la commande de
            sauvegarde \`/dev/disk1\`*

bajo Linux
----------

1.  ** ** Respaldo

    -   Para encontrar el disco que corresponda a la tarjeta, abrir una
        terminal et saisissez la commande : `sudo fdisk -l | grep Dis`

        ``` {.bash}
        $ sudo fdisk -l | grep Dis
        Disk /dev/sda: 320.1 GB, 320072933376 bytes
        Disk /dev/sdb: 16.0 GB, 16012804096 bytes
        Disk /dev/sdc: 8.0 GB, 8006402048 bytes
        ```

    -   Empezar a crear la imagen con el comando:
        `sudo dd if=/dev/sdc of=Backup_Jeedom.img bs=1m` *Remarque: Dans
        este ejemplo, el nombre de la unidad de la tarjeta es /dev/sdc.*

2.  ** ** Alimentos

    -   Para encontrar el disco que corresponda a la tarjeta, abrir una
        terminal et saisissez la commande : `sudo fdisk -l | grep Dis`

    -   Retire el mapa de particiones escribiendo (en
        la sustitución de X con los números de partición):
        `sudo umount /dev/sdcX`

    -   Restaurar la imagen en la tarjeta microSD con el comando:
        `sudo dd if=Backup_Jeedom.img of=/dev/sdc bs=1m` *Remarque: Dans
        este ejemplo, el nombre de la unidad de la tarjeta es /dev/sdc.*


