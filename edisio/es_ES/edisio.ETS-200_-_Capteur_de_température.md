-   **El módulo** 

![ets200.module](../images/ets200/ets200.module.jpg)

-   **El Jeedom visual**

![ets200.vue defaut](../images/ets200/ets200.vue-defaut.jpg)

resumen
======

Colocado en una habitación, la temperatura de la parte ascienda deseado
de forma automática. Además, asociado con un receptor de tipo EMR-2000 o
EDR-B4 (4 salidas) que tendrá un termostato conectado y controlable
desde cualquier lugar del mundo a través de Internet.

La señal se envía solamente después de detectar una diferencia
temperatura o 5 ° C o 1 ° C o cada 5 minutos. Además, el sensor
es compacto y discreto.

cambios de estado de señal de indicador de LED integrada.

funciones
=========

-   sensor de temperatura inalámbrico alimentado por baterías

-   ultracompacta

-   señal transmitida instantáneamente cuando un aumento o disminución
    temperatura

-   Facilidad de uso e instalación

-   El montaje en pared mediante tornillos o de doble cara

-   La información sobre el nivel de la batería

Características técnicas
===========================

-   Tipo de módulo: Transmisor Edisio

-   Uso: en la residencia

-   Alimentación: 3VDC (batería de litio ER14250)

-   Duración de la batería: hasta 3 años

-   Frecuencia: 868,3 MHz

-   Temperatura de funcionamiento: 0 ° C + 45 ° C

-   Rango en campo libre: 100M

-   Tamaño: 25x79x19mm

-   Protección: IP20

datos de los módulos
=================

-   Marca: Smart Home Edisio

-   Nombre: ETS-200

configuración general
======================

Para configurar Edisio plugin y asociar un módulo de Jeedom,
referirse a este
[Documentación](https://www.jeedom.fr/doc/documentation/plugins/edisio/fr_FR/edisio.html).

> **Importante**
>
> Para Jeedom crea automáticamente los módulos de transmisión, recuerde
> No hay que activar la opción en la configuración del plugin.

> **Tip**
>
> La inversión es aconsejable a una altura de 150 cm y cerca
> Al igual que la temperatura deseada.

Botón "E"
----------

A continuación, encontrará el botón "E" es la combinación de botones de
sensor de temperatura.

![ets200.bouton e](../images/ets200/ets200.bouton-e.jpg)

Ajuste de la temperatura delta
-------------------------------

Por defecto, la diferencia de temperatura se establece en 1 ° C (+/- 10%) a
maximizar la duración de la batería. Usted tiene la opción de
ajustar este parámetro:

![ets200.delta](../images/ets200/ets200.delta.jpg)

Asociar el sensor a Jeedom
===============================

La combinación del sensor de temperatura es una brisa. Simplemente
presione el botón "E" se encuentra por debajo del sensor. Esto será
reconocido automáticamente. Colocarlo en un objeto, darle un nombre y
guardar.

![ets200.association](../images/ets200/ets200.association.jpg)

Una vez que su equipo pareja, usted debe conseguir esto:

![ets200.general](../images/ets200/ets200.general.jpg)

comandos
---------

Una vez creada su equipo, debe obtener órdenes
asociado con el módulo:

![Commandes](../images/ets200/ets200.commandes.jpg)

Estos son los comandos:

-   Temperatura: Este es el comando que indica la temperatura detectada

-   Batería: Indica el estado de la batería

información
------------

Una vez que su equipo asociado con Jeedom, diversa información se
disponibles:

![Commandes](../images/ets200/ets200.informations.jpg)

-   Creación: Muestra la fecha en que se creó el equipo

-   Comunicación: Indica la última comunicación registrada entre
    Jeedom y el micrófono del módulo

-   Batería: Indica el estado de la batería de módulos de batería

-   Estado: Devuelve el estado del módulo

**@ Jamsta** 
