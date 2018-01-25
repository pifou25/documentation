polylock
========

\

-   ** ** El módulo

\

![module](../images/polycontrol.polylock/module.jpg)

\

-   ** El Jeedom visual **

\

![vuedefaut1](../images/polycontrol.polylock/vuedefaut1.jpg)

\

resumen
------



Asegure su casa mediante el uso de la cerradura electrónica Z-Wave
Poli-Control!

La cerradura electrónica poli-Lock está diseñado para adaptarse a casi
todas las puertas que existen. Se monta fácilmente en 5
minutos, sólo cambian la puerta del cilindro.

Una vez emparejado con el controlador Z-Wave (tales como sistemas de Vera
VeraControl), se puede tener un control completo de la cerradura
desde cualquier ordenador o teléfono inteligente, donde quiera que
están en el mundo. También es posible usar el bloqueo
con el teclado inalámbrico Poli-Pad para abrir o cerrar la puerta.

Es posible bloquear su casa de manera similar
bloquear el coche - con un mando a distancia, pulsando
de un botón y su casa es segura. La cerradura
Poli-control también puede trabajar con otras escenas Z-Wave, donde
las luces se encienden y el sistema de alarma se desactiva cuando
desbloqueado a través del mando a distancia.

sistema de poli-Control se puede utilizar en un entorno
casa o trabajo. cerradura poli-Lock es alimentado por
batería, y fue probado para funcionar durante un año sin
reemplazo de la batería.

\

funciones
---------

\

-   Controlar su puerta de forma remota

-   Se adapta a la mayoría de las puertas

-   Se puede integrar en escenas Z-Wave, por ejemplo para un sistema de
    alarma

-   Adecuado para uso privado o profesional

-   Rueda de cierre manual

-   fácil instalación

\

Características técnicas
---------------------------

\

-   Fuente de alimentación: 3.6V Batería de Litio Cloruro

-   Frecuencia: 868.42 MHz

-   Rango: hasta 100 m en espacios abiertos hasta 30 m de
    edificios

-   Dimensiones: 120 x 52 x 60 mm (L x W x H)

-   Peso: 370g

\

datos de los módulos
-----------------

\

-   Marca: Poli-Control

-   Nombre: polylock

-   ID Fabricante: 270

-   Tipo de producto: 1

-   Identificación del producto: 1

\

configuración
-------------

\

Para configurar OpenZwave plugin y cómo poner en Jeedom
inclusión se refiere a este
[Documentación] (https://jeedom.fr/doc/documentation/plugins/openzwave/fr_FR/openzwave.html).

\

> ** Importante **
>
> Para poner este modo la inclusión del módulo hay que pulsar 1 tanto en el
> Botón de inclusión, de acuerdo con su documentación en papel.

\

![inclusion](../images/polycontrol.polylock/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/polycontrol.polylock/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/polycontrol.polylock/commandes.jpg)

\

Estos son los comandos:

\

-   Estado: Este es el comando que se elevará la última acción
    ejecutado (abrir / cerrar)

-   Abierto: el comando para abrir la cerradura

-   Cerca: el comando para cerrar la cerradura

-   Batería: el control de la batería

\

### Configuración del módulo

\

> ** Aviso **
>
> A pesar de que este módulo está alimentado por batería que utiliza la tecnología Flirs.
> Eso significa que no tiene un concepto de despertador y servicio de despertador. lo
> Recuperar todos los cambios configutation casi en tiempo real
> Como un módulo sector.

\

Si desea configurar en función de su módulo
instalación, esto requiere pasar por el botón "Configuración"
OpenZwave plug-in Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

Se llega en esta página (después de hacer clic en la pestaña
configuraciones)

\

![Config1](../images/polycontrol.polylock/config1.jpg)

\

Detalles de los parámetros:

\

-   0: Cambia el sentido de giro de los pedidos
    apertura / cierre

-   1: establecer el tiempo que dará vuelta a la cerradura para
    abiertos (0 a 15 s)

-   2: establecer el tiempo que dará vuelta a la cerradura para
    cercanos (0 a 15 s)

-   3: Ajuste la velocidad de rotación de la cerradura (0 a 15,
    15 siendo más lento)

-   4: elegir entre diferentes modos de operación
    (Par, fuerza, potencia, etc ...)

\

### grupos

\

Este módulo tiene un solo grupo de asociación.

\

![Groupe](../images/polycontrol.polylock/groupe.jpg)

\

Ejemplos de uso
----------------------

\

![exemple](../images/polycontrol.polylock/exemple.jpg)

\

El evento de disparo es el comando de un teclado zipato
(Puede ser cualquier otra cosa). Si el valor es 6 (casa) es
cierra la puerta. De hecho acabamos de regresar para que podamos cerrar
la clave de la puerta. Si no (necesariamente 5) se abre la puerta a la tecla 2 minutos
después de que se cierre. De hecho, al salir, la puerta se abre y se
se cierra poco después.

\

Bueno saber
------------

\

### detalles específicos

\

> ** Tip **
>
> A pesar de que este módulo está alimentado por batería que utiliza la tecnología Flirs.
> Eso significa que no tiene un concepto de despertador y servicio de despertador. lo
> Recuperar todos los cambios configutation casi en tiempo real
> Como un módulo sector.

\

> ** Tip **
>
> Este módulo no devuelve su estado, si se pulsa el bloqueo de
> Mano el estado seguirá siendo el mismo. \

### alternativa visual

\

![vuewidget](../images/polycontrol.polylock/vuewidget.jpg)

\

despertarse
-------

\

No existe el concepto de despertador para este módulo.

\

F.A.Q.
------

\

Sin noción de despertador en este módulo, leer las características de párrafo.

\

** ** @ sarakha63
