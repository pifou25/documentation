Hardware
========

Hardware | State | Remarks
--- | --- | ---
Jeedomboard             | Stable                  |
Hummingboard            | Stable                  |
Odroid C2               | Stable                  |                          
Smart                   | Stable                  |                          
RPI1                    | Stable                  |                          
RPI2                    | Unofficial / Stable     |                          
RPI3                    | Unofficial / Stable     | Attention if you use a Razberry the wifi / bluetooth will not work
64 bits                 | Stable                  |                          
32 bits                 | Unsupported            |                          
vmware                  | Stable                  | No support for VMware, only for Jeedom. CAUTION VmWare 6.5 requires the installation of a VMWare patch for Zwave support.

Images
======

Vous pouvez retrouver toutes les images Jeedom
[ici](https://images.jeedom.com/),
puis dans le dossier Images

> **Note**
>
> A netinstall image goes on the first boot to install the
> last stable version of Jeedom, this startup is a bit more
> long and requires access to the internet. You can follow
> the progress of it by going to the IP of your Jeedom with your
> browser

| imagery         | Hardware       | State           | SSH access      | Remarks      |
|----------------|----------------|----------------|----------------|----------------|
| Jeedomboard    | jeedomboard and | Beta           | root / Mjeedom96 |                |
| netinstall     | hummingboard   |                |                |                |
| Jeedomboard    | jeedomboard and | Stable         | root / Mjeedom96 |                |
|                | hummingboard   |                |                |                |
| Docker         |                | Beta           | root / Mjeedom96 |                |


All other previously downloadable images are no longer
maintained, it is better to go through the manual installation of Jeedom
[Doc](https://github.com/jeedom/documentation/blob/master/installation/fr_FR/other.asciidoc)
after installing a linux distribution corresponding to your
Hardware: Debian (vm, pc, ...), Raspbian Lite (Raspberry pi), Armbian
(Ordoid, ...), ...

Logiciel
========

> **Important**
>
> Jeedom only supports Debian Jessie (stable) and Stretch (stable).
> Any other version (Wheezy ...) or distribution (Ubuntu ...) is not
> supported by Jeedom.


| Name                     | State                    | Remarks                |
|-------------------------|-------------------------|--------------------------|
| PHP 5.5 or less        | Unsupported            |                          |
| PHP 5.6                 | Stable                  |                          |
| PHP 7.X                 | Stable                  |                          |
| Mysql 5.5 / 5.6           | Stable                  |                          |
| Mysql 5.7               | Beta                    |                          |
| MariaBD                 | Stable                  |                          |

Other
=====

Clef USB/Module d’extension
---------------------------

ENOCEAN controller:

-   EnOcean USB300 USB Key
-   EnOcean USB310 USB Key (Recommended)

RFXCOM interface:

-   RFXtrx433 USB
-   RFXtrx433E USB (Recommended)

EDISIO gateway:

-   Dongle Edisio (Recommended)

Led indicator:

-   blink (1) mk2 (Recommended)

GSM Dongle:

-   HUAWEI E220 (Recommended)
-   Alcatel one touch X220L
-   HSDPA 7.2MBPS 3G Wireless

Z-WAVE controller:

-   SIGMA DESIGNS USB Z-Wave Plus Controller
-   Z-WAVE.ME - UZB1 Z-Wave Plus USB Mini Controller
-   AEON LABS Z-Wave Controller Aeon Labs Z-Stick S2
-   AEON LABS - Z-Wave USB Controller Z-Wave Plus GEN5 (Recommended)


Contrôleur Zigbee :

- [Phoscon Conbee I/II](http://bit.ly/2n4VyWc)

Modules Zwave
-------------

Vous trouverez la liste
[ici](https://jeedom.github.io/documentation/zwave/fr_FR/equipement.compatible)

Modules EnOcean
---------------

Vous trouverez la liste
[ici](https://jeedom.github.io/documentation/enocean/fr_FR/equipement.compatible)

Modules Edisio
--------------

Vous trouverez la liste
[ici](https://jeedom.github.io/documentation/edisio/fr_FR/equipement.compatible)

Modules RFXcom
--------------

Vous trouverez la liste
[ici](https://jeedom.github.io/documentation/rfxcom/fr_FR/equipement.compatible)

Caméras
-------

Vous trouverez la liste
[ici](https://jeedom.github.io/documentation/camera/fr_FR/equipement.compatible)

Plateforme matérielle recommandée
---------------------------------

L’équipe jeedom vous recommande (en fonction de votre budget) :

-   Jeedom Smart (tout est préinstallé, vous n’avez rien à faire)

-   Odroid C2 (meilleur rapport performance/prix)

-   Intel Nuc gen6 (des performances extrêmes, voir la catégorie tuto
    pour le choix dans les differents modèles et l’installation)
