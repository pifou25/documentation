Control Nodon - Soft remoto
================================

\

-   ** ** El módulo

\

![module](../images/nodon.softremote/module.jpg)

\

-   **El Jeedom visual**

\

![vuedefaut1](../images/nodon.softremote/vuedefaut1.png)

\

resumen
------

\

NodOn® remoto Soft puede controlar directamente cualquier dispositivo
consistente Z-Wave o Z-Wave Plus® como NodOn® socket inteligente.

También puede provocar escenas a través de una central de domótica
Compatible.

\

funciones
---------

\

-   Controlar cualquier dispositivo compatible con Z-Wave

-   Resistente a los golpes y salpicaduras

-   Se conecta en cualquier lugar con su imán integrado

-   6 colores disponibles

\

Características técnicas
---------------------------

\

-   Potencia: CR2032 - Batería 1,5 - 2 años

-   4 botones

-   Imán integrado para el montaje en superficie de metal

-   Resistente a los golpes y salpicaduras

-   Temperatura de funcionamiento: 0 ° C a 40 ° C - Altitud: 2000m

-   Protocolo de Z-Wave de radio: 868.4MHz - Serie 500 - compatibles con Z-Wave
    Plus® SDK 06.51.06

-   Rango: 40m intéieur / 80m al aire libre

-   Tamaño 56 \ 56 * \ * 20mm

-   2 años de garantía

\

datos de los módulos
-----------------

\

-   Marca: Nodon

-   Nombre: CRC-3-6-0x remoto suave

-   Identificación del fabricante: 357

-   Tipo de producto: 2

-   Identificación del producto: 2

\

configuración
-------------

\

Para configurar OpenZwave plugin y cómo poner en Jeedom
inclusión se refiere a este
[Documentación] (https://jeedom.fr/doc/documentation/plugins/openzwave/fr_FR/openzwave.html).

\

> **Importante**
>
> Para poner esto inclusión modo de módulo debe presionar tanto
> Botón (+ 0 y completo) hasta que la luz se vuelve rosa continuación,
> Pulse el botón + de acuerdo con su documentación en papel.

\

![inclusion](../images/nodon.softremote/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/nodon.softremote/information.png)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/nodon.softremote/commandes.png)

\

Estos son los comandos:

\

-   Botones: el comando que ascienda el botón pulsado

+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| botones | soporte | Soporte larga | aflojamiento | Doble toque |
================ ================ + + + =============== = + + ================ ================ +
| ** 1 (0 | 10 | 12 | 11 | 13 |
| completo) ** | | | | |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| **2 (+)** | 20 | 22 | 21 | 23 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| **3 (0 vacío)** | 30 | 32 | 31 | 33 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +
| **4 (-)** | 40 | 42 | 41 | 43 |
+ ---------------- + ---------------- + --------------- - + ---------------- + ---------------- +

-   Batería: Este es el comando que se remonta a las baterías

\

### Configuración del módulo

\

> **Importante**
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

![Config1](../images/nodon.softremote/config1.png)

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

![Groupe](../images/nodon.softremote/groupe.png)

\

-   Grupo 1 - Supervivencia: Este grupo se utiliza generalmente para
    Ver información del Smart Plug el controlador principal
    red.

-   Grupo 2 a 5 - Dispositivos de estos grupos están controlados por el
    botón correspondiente de acuerdo con el perfil MONO

-   Grupo 6-7 - Los dispositivos en estos grupos son controlados por
    los botones correspondientes de acuerdo con el perfil DUO

\

> **Importante**
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

Para despertar este módulo sólo tiene que pulsar uno de los botones

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

> **Importante**
>
> Hay que despertar el módulo después de su inclusión, después de un cambio
> La configuración, después de un cambio de wakeup después de una
> Asociación cambiar de grupo

\

** ** @ lunarok
