-   ** ** El módulo

![module](../images/emv.400/module.jpg)

-   ** El Jeedom visual **

![vue default](../images/emv.400/vue_default.jpg)

resumen
======

El módulo de micro-EMV-400 le permitirá gestionar un motor
equipos bidireccional o eléctrica. Permite el control
2 salidas de encendido / apagado o obturador abierto / Stop / Cerrar.

Por otra parte, la interacción con otros protocolos es posible, es
controlable por los interruptores y / o de la marca de control remoto
Edisio directamente de Jeedom sino por cualquier
Z-Wave red de transmisores.

Cada módulo Edisio red eléctrica, la posibilidad de
función como un repetidor inalámbrico con otros módulos a
para asegurar una cobertura completa de su hogar.

Por último, cada módulo se puede utilizar en modo remoto, que es muy
la práctica ya que permite la asociación de un transmisor sin tener que acceder a la
receptor.

> ** Importante **
>
> El neutro es necesaria para el "disparador" modo de

funciones
=========

-   2 salidas suministrada por el relé

-   Se mueve en una caja de montaje o directamente en 55mm
    los pocillos de la abertura

-   Modo de uso: On / Off, Open / Stop / Cerrar

-   Compatible con motores y de carrera electrónico
    mecánico

-   modo remoto

-   La función del temporizador: Modo de encendido / apagado: 30min o 60min

-   Réplica de la señal (repetidor)

-   micromódulo bidireccional

-   Nivel de batería baja del transmisor

-   Pequeña, discreta y estética

-   Facilidad de uso e instalación

Características técnicas
===========================

-   Tipo de módulo: Receptor Edisio

-   Fuente de alimentación: 230 V CA, 50 Hz

-   Cableado: 4 hijo, 2 órdenes y 2 para los alimentos

-   Frecuencia: 868,3 MHz

-   salidas de suministro de corriente: 2 relé

-   la potencia máxima: 2A por salida

-   Carga resistiva: 460W

-   Otros gastos: 100W

-   Temperatura de funcionamiento: -10 ° C + 45 ° C

-   Tamaño: 48x46x26mm

-   Protección: IP20

datos de los módulos
=================

-   Marca: Smart Home Edisio

-   Nombre: EMV-400

configuración general
======================

Para configurar Edisio plugin y asociar un módulo de Jeedom,
referirse a este
[Documentación] (https://www.jeedom.fr/doc/documentation/plugins/edisio/fr_FR/edisio.html).

> ** Importante **
>
> Para Jeedom crea automáticamente los módulos de transmisión, recuerde
> No hay que activar la opción en la configuración del plugin.

> ** Importante **
>
> A la inversa, los receptores son Edisio para crear manualmente
> Jeedom.

Interruptor DIP y el botón "R":
--------------------------

![bouton association](../images/emv.400/bouton_association.jpg)

-   El interruptor DIP le permite ajustar la configuración
    (/ Manual de obturador / luz / Temporizador Repetidor) módulo:

![dip switch](../images/emv.400/dip_switch.jpg)

> ** Nota **
>
> Para evitar la duplicación innecesaria, nunca se activará el modo de
> "Repetidor" en todos los receptores, los receptores 5 máximo por
> Instalación.

-   El botón "R" permitirá asociar un emisor y un receptor,
    para activar o desactivar el temporizador y activar el modo de
    remoto:

![bouton r](../images/emv.400/bouton_r.jpg)

> ** Nota **
>
> 3x Pulse R para activar el modo remoto.

Diagrama de operación
---------------------------

A continuación, si el transmisor está configurado en "clave 1" o "2
llaves", aquí está el funcionamiento del módulo:

> ** Nota **
>
> Consulte la documentación del fabricante, con el fin de
> Establecer su transmisor.

![diagramme](../images/emv.400/diagramme.jpg)

función de temporizador
------------------

La función de temporizador permite el apagado automático después de los relés
30 o 60 minutos.

> ** Nota **
>
> Esta función se utiliza sólo en la moda "Iluminación"

El modo "disparador"
===============

El modo "persiana" permite controlar un extremo del motor bidireccional
carrera electrónico y mecánico a distancia.

> ** Importante **
>
> El neutro es necesario

Configuración y conexiones eléctricas:
--------------------------------------------

![mode moteur](../images/emv.400/mode_moteur.jpg)

> ** Importante **
>
> Para el módulo está en "Shutter 'modo de interruptor DIP 2 es la
> baja

> ** Importante **
>
> NUNCA ENCIENDA

Creación módulo en Jeedom
------------------------------

Para asociar un módulo receptor Jeedom Edisio, crear
equipos de mano.

![ajout equip](../images/emv.400/ajout_equip.jpg)

Una vez que haya creado su equipo, usted debe conseguir esto:

![crea equip](../images/emv.400/crea_equip.jpg)

> ** Nota **
>
> Recuerde que debe activar la opción.

En la lista de equipos, a la derecha, seleccione "panel Micro módulo
rodante ":

![infos equip](../images/emv.400/infos_equip.jpg)

comandos
---------

Una vez guardado el equipo, debe obtener órdenes
asociado con el módulo:

![Commandes](../images/emv.400/commande.jpg)

Estos son los comandos:

-   Estado: Este es el comando que simule la realimentación de estado

-   Ajuste: Este es el comando para abrir la puerta

-   Stop: Este es el comando para detener el movimiento de la aleta

-   Abajo: Este es el comando para cerrar el obturador

-   E: Este es el comando para utilizar el modo remoto

> ** Importante **
>
> El regreso de estado se simula mediante Jeedom. Por lo tanto, si
> Uso de otro transmisor, Jeedom no actualizará el estado
> Receptor.

información
------------

Una vez que su equipo asociado con Jeedom, diversa información se
disponibles:

![Commandes](../images/emv.400/infos_moteur.jpg)

-   Creación: Muestra la fecha en que se creó el equipo

-   Comunicación: Indica la última comunicación registrada entre
    Jeedom y el micrófono del módulo

-   Batería: Indica el estado de la batería de los módulos de batería

-   Estado: Devuelve el estado del módulo

Asociación micromódulo Jeedom
===================================

Para que pueda interactuar con Jeedom, como si se tratara de una
transmisor Edisio.

> ** Nota **
>
> Una gran ventaja de Edisio es que un receptor puede tener
> Más transmisores asociados

método estándar
----------------

Cada salida está asociado con un comando Jeedom:

-   Asociar la salida 1:

    -   1x prensa sobre el "R" del receptor, solo pitido (corto
        repetición) dijo la programación de la salida 1 activado.

    -   Dentro de 10 segundos, pulse el botón "Test" en el "abierto"
        en Jeedom, un pitido continuo indica la combinación de
        salida 1 a Jeedom.

    -   Dentro de 10 seg, pulse de nuevo "R" del receptor, para
        validar la asociación, el pitido se detiene.

-   Asociar la salida 2:

    -   2x prensa sobre el "R" del receptor, dos pitidos (corto
        repetición) dijo la programación de la salida 2 activado.

    -   Dentro de 10 segundos, presione comando "Test" "Cerca"
        en Jeedom, un pitido continuo indica la combinación de
        salida 2 a Jeedom.

    -   Dentro de 10 seg, pulse de nuevo "R" del receptor, para
        validar la asociación, el pitido se detiene.

> ** Nota **
>
> No hay necesidad de asociar el comando "Stop", se
> Automáticamente.

método remoto
----------------

Hablamos al principio de esta documentación, en el caso de
módulo ya incrustado en falsos techos o incluso el ático. Este
método permite la adición de un nuevo transmisor sin acceso a la "R"
receptor.

-   Vincular el botón "R":

    -   Pulsar 3 veces "R" del receptor, el triple pitido (corto
        Repetición) indica el modo de programación activado.

    -   Dentro de 10 segundos, pulse el botón "Test" del comando "E" en
        Jeedom, un pitido continuo indica la asociación Jeedom.

    -   Dentro de 10 segundos, pulse de nuevo "E" del receptor, por
        validar la asociación, el pitido se detiene.

Está hecho, su Jeedom se asocia con esto y el orden "E"
reemplaza el botón "R" en el receptor.

-   Asociar un nuevo transmisor a un receptor con Jeedom ya asociado
    :

    -   Salida 1:

        -   1x Prensa "de prueba" comando "E" en Jeedom sencilla
            pitido (a corto repetición) dijo programación
            salida 1 activado.

        -   En 10 segundos, pulse cualquier tecla "C" de la nueva
            transmisor para asociar una señales de pitido continuo
            la combinación de la salida 1.

        -   Dentro de 10 segundos, pulse de nuevo "prueba" de la
            comando "E" en Jeedom para validar la asociación, el pitido
            paradas de sonido.

    -   Salida 2:

        -   Pulsar 2 veces "prueba" de la orden "E" en Jeedom,
            tono doble (a corto repetición) señala el
            Salida de la programación 2 activado.

        -   En 10 segundos, pulse cualquier tecla "C" de la nueva
            transmisor para asociar una señales de pitido continuo
            la combinación de la salida 2.

        -   Dentro de 10 segundos, pulse de nuevo "prueba" de la
            comando "E" en Jeedom para validar la asociación, el pitido
            paradas de sonido.

> ** Nota **
>
> Se puede repetir tantas veces como se desee asociar
> Transmisor al receptor

alternativa visual
=================

![vue alt moteur](../images/emv.400/vue_alt_moteur.jpg)

F.A.Q.
======

Cómo borrar la memoria del receptor?

: 10 sec presionado el "R" para el pitido continuo.

Cómo controlar el receptor a través de un transmisor de Z-Wave?

: Con el plugin Escenario Jeedom.

¿Cómo puedo tener la misma visual?

: Con el plugin widgets de Jeedom.

** ** @ Jamsta
