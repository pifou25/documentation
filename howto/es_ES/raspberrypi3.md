meta
========

Aquí encontrará la documentación de la instalación de un Jeedom
PI frambuesa 3 **sin tarjeta microSD.**

El hecho de PI3 ofrece la posibilidad de arrancar directamente a una
dispositivo USB y así superar la tarjeta microSD veces
problemas de generación (corrupción).

** El procedimiento de instalación es idéntico al de una
tarjeta microSD, pero se asegurará de que tienen un firmware
día.**

Para que abrir una conexión SSH. (Si no sabe cómo hacerlo,
ver la microSD en la instalación:
[Aquí] (https://jeedom.github.io/documentation/installation/fr_FR/index.html)
)

    vcgencmd otp_dump | grep 17:

Debe obtener a cambio:

    17: 3020000a

Si este es el caso, su PI3 está correctamente configurado para arrancar
USB. Si no encuentra nada, se iniciará normalmente en un mapa
microSD.

Si la devolución es diferente, sólo tiene que realizar una actualización
día.

    apt-get update sudo; sudo apt-get install RPI-actualización

después

    sudo update-RPI

A continuación, reinicie la PI3

    reinicio sudo

> **Importante**
>
> Para evitar problemas de energía, vaya para una unidad SSD mSATA
> Bajo consumo.

> **Tip**
>
> Ahora puede instalar Jeedom siguiendo exactamente el mismo
> Procedimiento con una tarjeta SD.
> [Aquí] (https://jeedom.github.io/documentation/installation/fr_FR/index.html)

posibles ajustes
=====================

**Se debe entonces tener en cuenta las siguientes observaciones:**

> **Importante**
>
> Los siguientes cambios son el resultado de problemas
> Usuarios. Hay que adaptarse a ti. El apoyo
> Jeedom no interviene a problemas con su configuración.

-   **Si usted está teniendo problemas de intercambio, usted tiene que cambiar.**

    -   ** ** Aumentar el tamaño:

        -   Cambiar el tamaño del archivo de intercambio al abrirlo:

<! - ->

    sudo nano / etc / dphys-archivo de intercambio

-   Encontrar el ajuste correcto:

<! - ->

    CONF_SWAPSIZE = 100

-   Cambiar el valor de CONF \ _SWAPSIZE 1024, por ejemplo, entonces
    reiniciar:

<! - ->

    reinicio sudo

-   **Cambie la llamada al valor de intercambio.**

Por defecto, el sistema llama al intercambio cuando menos del 40%
Ram.

-   Abrir el archivo para cambiar esta configuración:

<! - ->

    sudo nano /etc/sysctl.conf

-   Añadir esta línea para pedir a la Pi3 utilizar el intercambio que
    cuando todavía tiene 10% de memoria disponible (100 MB
    RAM disponible):

<! - ->

    vm.swappiness = 10

-   A continuación, reinicie:

<! - ->

    reinicio sudo

-   ** Apagar el Bluetooth integrada por ser incompatible con el mapa
    zwave.me GPIO **

    -   Abrir el archivo en cuestión:

<! - ->

    /boot/config.txt sudo nano

-   añadir la línea:

<! - ->

    dtoverlay = ft3-disable-bt

-   Hacer un cierre limpio

<! - ->

    detuvo sudo

-   desconecte el enchufe (sin reinicio sudo!).


