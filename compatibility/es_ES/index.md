hardware
========

hardware | estado | observaciones
--- | --- | ---
Jeedomboard             | estable                  |
Hummingboard            | estable                  |
ODROID C2               | estable                  |                          
inteligente                   | estable                  |                          
RPI1                    | estable                  |                          
RPI2                    | No oficial / Estable     |                          
RPI3                    | No oficial / Estable     | Advertencia si utiliza una conexión Wi-Fi Razberry / bluetooth no puede caminar
64 bits                 | estable                  |                          
32 bits                 | no es compatible            |                          
VMware                  | estable                  | No hay soporte para VMware solamente Jeedom. PRECAUCIÓN VMware 6.5 requiere la instalación de una solución para el apoyo de VMWare para Zwave.

imágenes
======

Usted puede encontrar todas las imágenes Jeedom
[Aquí](https://www.amazon.fr/clouddrive/share/OwYXPEKiIMdsGhkFeI3eUQ0VcvTEBq0qxQevlXPvPIy/folder/IT3WZ3N0RqGzaLBnBo0qog)
a continuación, en la carpeta Imágenes

> **Nota**
>
> Una imagen se NetInstall cuando se empieza la instalación
> La última versión estable de Jeedom, esta bota es un poco más
> Largo y requiere acceso a Internet. Puede seguir
> Promoción de ella por ir a la IP con su Jeedom
> navegador

| imágenes         | hardware       | estado           | acceso SSH      | observaciones      |
|----------------|----------------|----------------|----------------|----------------|
| Jeedomboard    | y jeedomboard | beta           | root / Mjeedom96 |                |
| netinstall     | hummingboard   |                |                |                |
| Jeedomboard    | y jeedomboard | estable         | root / Mjeedom96 |                |
|                | hummingboard   |                |                |                |
| estibador         |                | beta           | root / Mjeedom96 |                |


Todas las demás imágenes descargables anteriores no son
mantenido, es mejor ir a través de la instalación manual de Jeedom
[Doc](https://github.com/jeedom/documentation/blob/master/installation/fr_FR/other.asciidoc)
Después de instalar una distribución Linux para su
Hardware: Debian (vm, PC, ...), Raspbian Lite (Frambuesa Pi), Armbian
(Ordoid, ...), ...

software
========

> **Importante**
>
> Jeedom sólo es compatible con Debian Jessie (estable) y estiramiento (estable).
> Cualquier otra versión (sibilante ...) o la distribución (Ubuntu ...) no es
> Con el apoyo de Jeedom.


| apellido                     | estado                    | observaciones                |
|-------------------------|-------------------------|--------------------------|
| PHP 5.5 o menos        | no es compatible            |                          |
| PHP 5.6                 | estable                  |                          |
| PHP 7.X                 | estable                  |                          |
| MySQL 5.5 / 5.6           | estable                  |                          |
| mySQL 5.7               | beta                    |                          |
| MariaBD                 | estable                  |                          |

otro
=====

llave USB / módulo de expansión
---------------------------

Controller ENOCEAN:

-   EnOcean USB300 llave USB

-   EnOcean clave USB310 USB (recomendado)

Interfaz RFXCOM:

-   RFXtrx433 USB

-   RFXtrx433E USB (recomendado)

EDISIO puerta de enlace:

-   Dongle Edisio (Otro)

Indicador LED:

-   parpadear (1) mk2 (Otro)

Dongle GSM:

-   HUAWEI E220 (Otro)

-   Alcatel One Touch X220L

-   HSDPA 7,2 Mbps inalámbrica 3G

Controlador de Z-WAVE:

-   Sigma Designs USB controlador Z-Wave Más

-   Z-WAVE.ME - Mini USB controlador Z-Wave Más UZB1

-   AEON LABS controlador Z-Wave Aeon Labs de Z-Stick S2

-   AEON LABS - controlador USB Z-Wave Z-Stick Más GEN5 (Recomendado)

módulos Zwave
-------------

Una lista
[Aquí](https://jeedom.github.io/documentation/zwave/es_ES/equipement.compatible)

módulos EnOcean
---------------

Una lista
[Aquí](https://jeedom.github.io/documentation/enocean/es_ES/equipement.compatible)

módulos Edisio
--------------

Una lista
[Aquí](https://jeedom.github.io/documentation/edisio/es_ES/equipement.compatible)

módulos RFXCOM
--------------

Una lista
[Aquí](https://jeedom.github.io/documentation/rfxcom/es_ES/equipement.compatible)

cámaras
-------

Una lista
[Aquí](https://jeedom.github.io/documentation/camera/es_ES/equipement.compatible)

Plataforma de hardware recomendados
---------------------------------

El equipo recomienda que jeedom (dependiendo de su presupuesto)

-   Jeedom inteligente (todo es pre-instalado, no tiene nada que ver)

-   ODROID C2 (mejor rendimiento / precio)

-   Intel NUC Gen6 (rendimiento extremo, véase la categoría tutorial
    la elección de los diferentes modelos y la instalación)


