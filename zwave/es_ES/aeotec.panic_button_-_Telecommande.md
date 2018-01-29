Botón de pánico Aeotec
===================

\

-   ** ** El módulo

\

![module](../images/aeotec.panicbutton/module.jpg)

\

-   **El Jeedom visual**

\

![vuedefaut1](../images/aeotec.panicbutton/vuedefaut1.jpg)

\

resumen
------

\

Este llavero de control remoto en el diseño atractivo y moderno tiene una
botón para controlar cualquier tipo de dispositivos Z-Wave como
lámparas, persianas, etc.

Con su tamaño compacto, se puede poner fácilmente
en el bolsillo. Fácil de usar y elegante, está equipado con una
anillo para adjuntarlo a la llave, que pone a disposición de
al salir de la casa o al volver a su hogar.

El botón se utiliza para controlar dos dispositivos o escenas a través
gestión de prensas cortas y largas. Este mando a distancia también puede
bien utilizado como controlador principal y secundaria.

Esta distancia también se puede utilizar como un botón
emergencia o pánico. En caso de peligro o cuando su titular
se enfrenta a otra situación de emergencia, basta con pulsar sobre ella
Se emitirán botón y una señal Z-Wave. En este caso, este dispositivo
También se puede utilizar como un medallón alrededor de su cuello.

\

funciones
---------

\

-   llavero de control remoto

-   controlador primario o secundario

-   Ultra compacto y diseño ultra

-   1 botón configurable

-   Gestiona hasta 2 dispositivos / escenas

-   Se puede utilizar como un botón de emergencia / pánico

-   Usar alrededor del cuello como medallón de emergencia

\

Características técnicas
---------------------------

\

-   Tipo de módulo: Transmisor Z-Wave

-   Fuente de alimentación: 1 batería de litio de 3V CR2450

-   duración de la batería: 2 a 3 meses de 10 a 20 usos
    por día

-   Frecuencia: 868.42 MHz

-   Distancia de transmisión: 30m cubierta

-   Dimensiones: 55 x 30 x 11 mm (L x W x H)

\

datos de los módulos
-----------------

\

-   Marca: Aeotec

-   Nombre: Botón de pánico

-   Identificación del fabricante: 134

-   Tipo de producto: 1

-   Identificación del producto: 38

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
> Para poner este modo la inclusión del módulo tiene que pulsar el botón
> LEARN, de acuerdo con su documentación en papel.

\

![inclusion](../images/aeotec.panicbutton/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/aeotec.panicbutton/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/aeotec.panicbutton/commandes.jpg)

\

Estos son los comandos:

\

-   Botones: el comando que ascienda el botón pulsado

1: el botón corto

2: Botón de pulsación larga

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
Configuraciones)

\

![Config1](../images/aeotec.panicbutton/config1.jpg)

\

Detalles de los parámetros:

\

-   250: modo de funcionamiento del mando a distancia (absolutamente poner
    Escenas a ser utilizado en el control remoto)

-   255: Permite el Mando resetter de la fábrica

\

### grupos

\

Este módulo tiene un solo grupo de asociación. El es
esencial.

\

![Groupe](../images/aeotec.panicbutton/groupe.jpg)

\

Bueno saber
------------

\

### detalles específicos

Para utilizar este módulo en remoto proceder como sigue:

-   1: Incluir el control remoto

-   2: El despertar del control remoto

-   3: establece el valor true 250 Cambio (lo hacen bien, incluso si él
    aparece ya en true)

-   4: El despertar del mando a distancia y para asegurar que el cambio ha sido
    tener en cuenta

-   5: El cambio en el modo de funcionamiento permanente de los restantes remoto
    presionando los dos botones en la parte posterior durante 3 segundos.

wakeup
------

\

Para despertar este módulo hay una sola manera de hacer esto:

-   mantenga pulsado 3 segundos en el botón LEARN

\

F.A.Q.
------

\

Este módulo se despierta de prensa restante 3 segundos en el botón LEARN.

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

** ** @ sarakha63
