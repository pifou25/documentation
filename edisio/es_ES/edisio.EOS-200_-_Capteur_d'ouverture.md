-   ** ** El módulo

![eos200.module](../images/eos200/eos200.module.jpg)

-   ** El Jeedom visual **

![eos200.vue defaut](../images/eos200/eos200.vue-defaut.jpg)

resumen
======

Colocado en una puerta, ventana, puerta del garaje, cajón, toda abrirlo
sensor compacto y discreto le permitirá saber el estado
apertura o el cierre de este último.

Dependiendo de la condición, el sensor de control de la ignición o la extinción de su
luces, apertura o cierre de las aletas, o la
una alarma a través de un script.

La señal es enviada sólo a la separación del sensor de sonido
elemento magnético. El indicador LED integrado muestra todos los cambios
Estado. bajo nivel de la batería se indica por 3 "bip" sonido en
receptor

funciones
=========

-   sensor magnético inalámbrico alimentado por baterías

-   Detecta la apertura / cierre

-   ultracompacta

-   De fácil instalación y la libertad

-   La señal es transmitida instantáneamente durante una apertura / cierre

-   tamper arranque

-   La información sobre el nivel de la batería

-   El montaje en pared mediante tornillos o cinta de doble cara

Características técnicas
===========================

-   Tipo de módulo: Transmisor Edisio

-   Alimentación: 3VDC (batería de litio ER14250)

-   Frecuencia: 868,3 MHz

-   Temperatura de funcionamiento: 0 ° C + 45 ° C

-   Rango en campo libre: 100M

-   Tamaño: 25x79x19mm

-   Protección: IP20

-   Uso: en la residencia

datos de los módulos
=================

-   Marca: Smart Home Edisio

-   Nombre: EOS-200

configuración general
======================

Para configurar Edisio plugin y asociar un módulo de Jeedom,
referirse a este
[Documentación] (https://www.jeedom.fr/doc/documentation/plugins/edisio/fr_FR/edisio.html).

> ** Importante **
>
> Para Jeedom crea automáticamente los módulos de transmisión, recuerde
> No hay que activar la opción en la configuración del plugin.

Botón "E"
----------

A continuación, encontrará el botón "E" es la combinación de botones de
sensor de temperatura.

![eos200.bouton e](../images/eos200/eos200.bouton-e.jpg)

configuración
-------------

De manera predeterminada, el sensor está configurado NO (normalmente abierto)

![eos200.nf no](../images/eos200/eos200.nf-no.jpg)

> ** Nota **
>
> Debemos, por tanto, establecer su sensor si desea una
> Widget con una puerta cerrada cuando lo es.

![eos200.mode](../images/eos200/eos200.mode.jpg)

Asociar el sensor a Jeedom
===============================

La combinación del sensor de movimiento es simple. lo
Sólo tiene que pulsar el botón "E" que se encuentra debajo del sensor. Esto será
automáticamente reconocido por Jeedom. Es suficiente para visitar el
Plugin de Edisio. Así que se puede colocar en un objeto, darle una
un nombre y guardar.

Una vez que su equipo pareja, usted debe conseguir esto:

![eos200.general](../images/eos200/eos200.general.jpg)

> ** Tip **
>
> Para que el widget para estar presente en el salpicadero, considere colocar
> Su equipo en un objeto.

comandos
---------

Una vez creada su equipo, debe obtener órdenes
asociado con el módulo:

![Commandes](../images/eos200/eos200.commandes.jpg)

Estos son los comandos:

-   Puerta: Este es el comando que indica si la puerta está abierta o
    cerrado

-   Batería: Indica el estado de la batería

información
------------

Una vez que su equipo asociado con Jeedom, diversa información se
disponibles:

![Commandes](../images/eos200/eos200.informations.jpg)

-   Creación: Muestra la fecha en que se creó el equipo

-   Comunicación: Indica la última comunicación registrada entre
    Jeedom y el módulo

-   Batería: Indica el estado de la batería de módulos de batería

-   Estado: Devuelve el estado del módulo

alternativa visual
=================

![eos200.vue alternative](../images/eos200/eos200.vue-alternative.jpg)

F.A.Q.
======

Cómo conducir un receptor Z-Wave?

: Con el plugin Escenario Jeedom.

¿Cómo puedo tener la misma visual?

: Con el plugin widgets de Jeedom.

** ** @ Jamsta
