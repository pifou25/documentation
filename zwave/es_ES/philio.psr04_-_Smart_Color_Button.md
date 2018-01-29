Botón Philio Color inteligente
=========================

\

-   ** ** El módulo

\

![module](../images/philio.psr04/module.jpg)

\

-   **El Jeedom visual**

\

![vuedefaut1](../images/philio.psr04/vuedefaut1.jpg)

\

resumen
------

\

Este conmutador ofrece varias características de diseño únicas. Usted
se puede utilizar para encender, apagar o cambiar la iluminación, ajuste
la posición de las persianas, ajustar el termostato o
utilizarlo como un temporizador.

Una vez incluido en su red Z-Wave, el PSR04 cambiar Philio
debe asociarse con (x) dispositivo (s) que desea controlar.
Se puede trabajar sólo a través de la asociación directa con
dispositivos, y no se pueden ejecutar escenas creadas en su controlador
Z-Wave domótica.

Se utiliza como un controlador, que tiene el mismo comportamiento que una unidad
Tradicional. Gire el mando hacia la derecha para aumentar la
luz, y hacia la izquierda para disminuirlo.

Además, puede mover y posicionar el interruptor fácilmente
la ubicación de su elección gracias a sus medios magnéticos. su diseño
sello puede ser instalado en una zona de alta humedad, tal como una
sala de baño.

Utiliza la última serie de chip Z-Wave 500, proporcionando una mayor
una gama de radio de 50% y 250% más de velocidad de comunicación
más rápido que los anteriores productos Z-Wave y una mayor
bajo consomation potencia que permite una mayor autonomía.

\

funciones
---------

\

-   interruptor multifunción

-   Z-Wave Tecnología +

-   ON / OFF y regulación (iluminación y persianas)

-   temporizador integrado

-   impermeable

-   Se adapta a cualquier estilo de decoración

-   recargable

-   Muy bajo consumo de energía

-   Batería de larga duración (6 meses por carga)

-   medios magnéticos

-   indicación RGBW LED

-   Fácil de instalar

\

Características técnicas
---------------------------

\

-   Potencia: polímero de litio de 3.7V, 220mA de vAutonomie
    Batería: 6 meses a 2 horas de carga

-   Consumo en espera: 18μA

-   Consumo de energía: 45 mA

-   Frecuencia: 868.42 MHz

-   La distancia de transmisión: 100m al aire libre, 40 m en interiores

-   dimensiones:

Soporte: 71,16 x 10,94 mm (diámetro x espesor) Botón: 59.99 x 14.89
mm (espesor x diámetro) Superficie + Button: 71,16 x 17,22 mm (diámetro
x grosor) \ * Certificado:

EN 301 489-1, EN 301 489-3 EN 300 220-1, EN 300 220-2 EN62479, EN60950
FCC Parte 15 B, FCC Parte 15 C

\

datos de los módulos
-----------------

\

-   Marca: Philio

-   Nombre: Botón PSR04 Color inteligente

-   Identificación del fabricante: 316

-   Tipo de producto: 9

-   ID del producto: 34

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
> Para poner este modo módulo requiere la inclusión en su posición
> Baja (inclusión) y pulse el botón, según su
> Documentación en papel.

\

![inclusion](../images/philio.psr04/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/philio.psr04/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/philio.psr04/commandes.jpg)

\

Estos son los comandos:

\

-   Estado: Este es el comando que ascienda la posición del botón 0
    100%

-   Batería: este es el comando que se remonta el estado de la batería
    módulo

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

![Config1](../images/philio.psr04/config1.jpg)

\

Detalles de los parámetros:

\

-   1: Establece el terminal más pequeña (totalmente a la izquierda)

-   2 define el terminal más alto (totalmente a la derecha)

-   intervalo de tiempo de ascenso de la batería: 10

-   25: Establece si el módulo envía su positon
    girar automáticamente (a menos de 1 segundo) o si tiene que pulsar
    botón para validar el envío

-   26: activa el envío de escena o no en el botón central de apoyo
    (El parámetro no tiene en cuenta en Jeedom)

\

### grupos

\

Este módulo tiene dos grupos de asociación, el primero es el único
esencial. El segundo se remonta a la posición Jeedom

\

![Groupe](../images/philio.psr04/groupe.jpg)

\

Bueno saber
------------

\

### detalles específicos

Para utilizar este módulo en remoto proceder como sigue:

-   Añadir el controlador en el grupo 2

De hecho este tipo de módulo no está hecho para interactuar directamente
con una caja sino directamente con otros módulos. Sin embargo,
añadiendo Jeedom al grupo 2, se puede recibir la posición de la
botón y por lo tanto utilizar una función para controlar escenario (establecer una
volumen, por ejemplo)

wakeup
------

\

Para despertar este módulo hay una sola manera de hacer esto:

-   poner el módulo en la posición inferior y pulse el botón

\

F.A.Q.
------

\

\

Este módulo es un módulo de batería, la nueva configuración se
consideración de que si se despierta en el módulo.

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
