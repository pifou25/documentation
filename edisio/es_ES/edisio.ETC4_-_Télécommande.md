-   ** ** El módulo

![module](../images/etc4/module.jpg)

-   **El Jeedom visual**

![vue default](../images/etc4/vue_default.jpg)

resumen
======

El mini e-moda de 4 canales a distancia es simple y robusto diseño,
que fue creado para complacer. Se conecta fácilmente a los receptores y
puede controlar las luces de encendido / apagado y regulable, motores,
persianas, persianas, puertas, puertas de garaje. Tiene dos modos
la programación.

Por otra parte, la interacción con otros protocolos es posible, lo que puede
interactuar con los receptores de marca Edisio con Jeedom pero
También por cualquier receptor Z-Wave en su red.

funciones
=========

-   Modo de uso: On / Off, Open / Stop / Cerrar, Drive,
    Motor, estores, persianas, puertas, puertas de garaje

-   2 modos de programación

-   Pequeña, discreta y estética

-   Facilidad de uso e instalación

Características técnicas
===========================

-   Tipo de módulo: Transmisor Edisio

-   Alimentación: 3VDC (CR2430 batería de litio)

-   Canales: 4

-   Frecuencia: 868,3 MHz

-   Temperatura de funcionamiento: -10 ° C + 50 ° C

-   Tamaño: 52x28x12mm

-   Protección: IP40

datos de los módulos
=================

-   Marca: Smart Home Edisio

-   Nombre: etc4

configuración general
======================

Para configurar Edisio plugin y asociar un módulo de Jeedom,
referirse a este
[Documentación] (https://www.jeedom.fr/doc/documentation/plugins/edisio/fr_FR/edisio.html).

> **Importante**
>
> Para Jeedom crea automáticamente los módulos de transmisión, recuerde
> No hay que activar la opción en la configuración del plugin.

Las modas
---------

Comprobar y centralizar su iluminación de encendido / apagado y convertidores
apertura, motores en el mismo botón o dos botones separados. la
Moda e-controles remotos tienen dos modos de funcionamiento, el modo 1 y el modo 2
:

-   MODO 1: Control de la tecla 1: encendido / apagado, abrir / cerrar,
    Cambiar + / variación-, Pulsada

-   MODO 2: Control de 2 botones:

    -   Claves: Detener, Cerrar, variación-, Pulsada

    -   Llaves bajas: Caminar, abierto, Variación, Pulsada

Diagrama de operación
===========================

Dependiendo de si el transmisor está configurado en "clave 1" o "2
llaves", aquí está el funcionamiento del mando a distancia:

![diagramme](../images/etc4/diagramme.jpg)

Cambiar el modo de
===============

-   MODO 1:

    -   Mantenga pulsado el "C4"

    -   1x Pulsar el botón "C1" sigue manteniendo pulsado
        "C4", el LED parpadeará 1 vez

![mode1](../images/etc4/mode1.jpg)

-   MODO 2:

    -   Mantenga pulsado el "C4"

    -   2x Pulse el "C1", sigue manteniendo pulsado
        "C4", el LED parpadeará 2 veces

![mode2](../images/etc4/mode2.jpg)

Jeedom remota Asociación
=======================================

La combinación de transmisor Edisio se hace simplemente y
de forma automática. Sólo tienes que pulsar cada tecla que
quiere tener en su Jeedom.

Una vez que su equipo pareja, usted debe conseguir esto:

![asso equip](../images/etc4/asso_equip.jpg)

comandos
---------

Una vez creada su equipo, debe obtener órdenes
asociado con el módulo:

![Commandes](../images/etc4/commandes.jpg)

Estos son los comandos:

-   BT01: Este es el comando para interactuar con el botón 1

-   BT02: Este es el comando para interactuar con el botón 2

-   BT03: Este es el comando para interactuar con el botón 3

-   bt04: Este es el comando para interactuar con el botón 4

-   Batería: Indica el estado de la batería

información
------------

Una vez que su equipo asociado con Jeedom, diversa información se
disponibles:

![Commandes](../images/etc4/infos.jpg)

-   Creación: Muestra la fecha en que se creó el equipo

-   Comunicación: Indica la última comunicación registrada entre
    Jeedom y el micrófono del módulo

-   Batería: Indica el estado de la batería de los módulos de batería

-   Estado: Devuelve el estado del módulo

uso
-----------

Una vez que el mando está configurado, se puede con la
escenario Jeedom plugin de interactuar con el mando a distancia en Jeedom.

> **Nota**
>
> Cada botón para volver al estado binario.

F.A.Q.
======

Cómo eliminar la asociación de una clave a un receptor?

: Pulse 5 seg en la "R" del receptor, un simple pitidos
    activar el modo de desprogramación. Pulse la tecla "C" para borrar.
    Repita este procedimiento para todas las teclas de borrar.

** ** @ Jamsta
