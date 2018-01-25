Nodon interruptor - Interruptor de pared
================================

\

-   ** ** El módulo

\

![module](../images/nodon.wallswitch/module.jpg)

\

-   ** El Jeedom visual **

\

![vuedefaut1](../images/nodon.wallswitch/vuedefaut1.jpg)

\

resumen
------

\

El interruptor de pared NodOn® puede controlar directamente cualquier
Z-Wave dispositivo habilitado o Z-Wave Plus® como tomar
NodOn® inteligentes o desencadenar escenas a través de un centro de
Automatización-compatibles.

El interruptor tiene una placa de montaje para montar la facilidad
en la casa mediante un tornillo sosteniendo la olla en el
atornillado a la pared, o simplemente pegando a través de adhesivos
De doble lado presente en la parte posterior de la placa.

\

funciones
---------

\

-   control único o con una central de domótica

-   Fácil de montar y desmontar

-   agradable sensación de apoyo

-   Sin hilos

-   2 años de batería

\

Características técnicas
---------------------------

\

-   Potencia: CR2032 - Batería 1,5 - 2 años

-   4 botones

-   el montaje con adhesivo de doble cara de la pared (incluido) o tornillos (no incluido)

-   Temperatura de funcionamiento: 0 ° C a 40 ° C

-   Altitud: 2000m

-   Protocolo de Z-Wave de radio: 868.4MHz - Serie 500 - compatibles con Z-Wave
    Plus® SDK 06.51.06

-   Rango: 40m 70m interior / exterior

-   Dimensiones: 80 \ 80 * \ * 15mm

-   2 años de garantía

-   EN 60950-1: 2006 + A11: 2009 + A1: 2010 + A12: 2011 + A2: 2013

-   EN 300 220-2 v2.4.1

-   EN301 489-1 v1.9.2

-   V1.6.1 EN301 489-3

-   EN 62479: 2010

\

datos de los módulos
-----------------

\

-   Marca: Nodon

-   Nombre: Interruptor CWS-Wall 03/01/01

-   Identificación del fabricante: 357

-   Tipo de producto: 2

-   Identificación del producto: 3

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
> Para poner esto inclusión modo de módulo debe presionar tanto
> Botón (1 y 2) hasta que la luz se vuelve rosa a continuación, pulse
> Botón 1, de acuerdo con su documentación en papel.

\

![inclusion](../images/nodon.wallswitch/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/nodon.wallswitch/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados a los módulos
disponible.

\

![Commandes](../images/nodon.wallswitch/commandes.jpg)

\

Estos son los comandos:

\

-   Botones: el comando que ascienda el botón pulsado

+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| botones | soporte | Soporte larga | aflojamiento | Doble toque |
================ ================ + + + =============== = + + ================ ================ +
| ** 1 ** | 10 | 12 | 11 | 13 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| ** 2 ** | 20 | 22 | 21 | 23 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| ** 3 ** | 30 | 32 | 31 | 33 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| ** 4 ** | 40 | 42 | 41 | 43 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +

\

### Configuración del módulo

\

> ** Importante **
>
> Cuando inclusión por primera vez todavía despierta en el módulo justo después de
> Inclusión.

\

Entonces, si desea configurar el módulo de acuerdo
su instalación, para ello es necesario pasar por el botón
"Configuración" plug-in OpenZwave Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

Se llega en esta página (después de hacer clic en la pestaña
configuraciones)

\

![Config1](../images/nodon.wallswitch/config1.jpg)

\

Detalles de los parámetros:

\

-   1-2: Elegir perfil de los botones si se utiliza en
    central (innecesario para su uso en Jeedom)

-   3: Un parámetro importante para saber si el interruptor está funcionando
    Escena de modo de escena o central (escena absolutamente poniendo)

-   4-7: Seleccionar los botones de modo de funcionamiento (en caso
    asociaciones grupos)

-   8: selecciona la operación del LED

### grupos

\

Este módulo tiene 7 grupos de asociación.

\

![Groupe](../images/nodon.wallswitch/groupe.jpg)

![Groupe](../images/nodon.wallswitch/groupe2.jpg)

\

-   Grupo 1 - Supervivencia: Este grupo se utiliza generalmente para
    Ver información del Smart Plug el controlador principal
    red.

-   Grupo 2 a 5 - Dispositivos de estos grupos están controlados por el
    botón correspondiente de acuerdo con el perfil MONO

-   Grupo 6-7 - Los dispositivos en estos grupos son controlados por el
    botón correspondiente de acuerdo con el perfil DUO

\

> ** Importante **
>
> Una Jeedom mínimo debería reflejarse en el grupo 1 \

Bueno saber
------------

\

### detalles específicos

\

-   Este módulo puede ser temperamental al inicio del estudio. No dude en el
    despertar después de 1 ó 2 veces el valor basal. así comprobar
    grupo asociación.

\

wakeup
------

\

Para despertar este módulo sólo tiene que pulsar uno de estos botones

\

F.A.Q.
------

\

Este módulo es un módulo de batería, la nueva configuración se
consideración de que si se despierta el mando a distancia.

\

Nota importante
---------------

\

> ** Importante **
>
> Hay que despertar el módulo después de su inclusión, después de un cambio
> La configuración, después de un cambio de wakeup después de una
> Asociación cambiar de grupo

\

** ** @ sarakha63
