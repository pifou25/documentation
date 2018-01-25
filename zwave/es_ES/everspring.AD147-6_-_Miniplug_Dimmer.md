Everspring miniconector Dimmer - AD147-6
====================================

\

-   ** ** El módulo

\

![module](../images/everspring.AD147-6/module.jpg)

\

-   ** El Jeedom visual **

\

![vuedefaut1](../images/everspring.AD147-6/vuedefaut1.jpg)

\

resumen
------

\

Mini zócalo atenuador está diseñado para controlar el encendido y
la extinción de las luces y los aparatos eléctricos en su
casa. También permite una función de atenuación que es compatible
solamente con bombillas. Con una tensión de 220 - 240 V, esto
Toma de Dimmer puede soportar una carga de 6 W a 250 W.

Mini zócalo del amortiguador es un dispositivo compatible con Z-Wave ™ es
diseñado para funcionar con todas las redes compatibles con Z-Wave ™. Ella
puede ser controlado por un control remoto, un software de PC, o cualquier
lo Z-Wave controlador de la red.

\

funciones
---------

\

-   El control de una lámpara remoto

-   Módulo tomada para ser incorporado directamente entre una toma eléctrica y
    la carga a ser controlado

-   ON / OFF y la función de inversor para lámparas de conducir

-   El control de apoyo local a través del botón integrado

-   La tecnología Z-Wave Más

-   Dimensiones reducidas para pasar casi desapercibida

-   LED de estado en el botón integrado

-   función de repetidor Z-Wave

\

Características técnicas
---------------------------

\

-   Tipo de módulo: el receptor Z-Wave

-   Fuente de alimentación: 230 V, 50 Hz

-   Consumo: 0.6W

-   Potencia máxima: carga resistiva: 250W incandescencia bombilla
    : LED bombilla de 250 W (no regulable): 6W

-   Frecuencia: 868.42 MHz

-   Rango: hasta 70 m en el exterior, hasta 30 m en edificios

-   Pantalla: LED en el botón

-   Dimensiones: Longitud (incluyendo socket): Diámetro 74 mm: 52 mm

\

datos de los módulos
-----------------

\

-   Marca: Everspring

-   Nombre: miniconector Dimmer

-   Identificación del fabricante: 96

-   Tipo de producto: 3

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
> Para poner este modo la inclusión del módulo se debe presionar tres veces en su
> Button, de acuerdo con su documentación en papel. Es importante
> Tenga en cuenta que este módulo se procederá directamente a la inclusión cuando
> No pertenece a ninguna red y es alimentado

\

![inclusion](../images/everspring.AD147-6/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/everspring.AD147-6/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/everspring.AD147-6/commandes.jpg)

\

Estos son los comandos:

\

-   Intensidad: Este es el comando para ajustar la intensidad de la
    toma

-   Uno: Este es el comando para activar el plug

-   Apagado: Este es el comando para apagar el tapón

-   Estado: Este es el comando que permite conocer el estado de la
    toma

\

Una nota sobre el tablero de instrumentos, la información de estado, encendido / apagado, la intensidad es
encontrarse en el mismo icono.

\

### Configuración del módulo

\

Se puede configurar la función de su módulo
instalación. Para ello es necesario pasar por el botón "Configuración"
OpenZwave plug-in Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

Se llega en esta página (después de hacer clic en la pestaña
Configuraciones)

\

![Config1](../images/everspring.AD147-6/config1.jpg)

\

Detalles de los parámetros:

\

-   1: Este parámetro define el valor de estado de control, no es
    recomendadas para cambiar este valor.

-   2: Este parámetro define el retardo envía el cambio de estado
    Grupo 1 (entre 3 y 25 segundos)

-   3: Este ajuste determina si la ingesta de recuperar su condición
    (ON u OFF) después de una recuperación de energía.

-   4: Este parámetro determina si el modo de toma con los cortafuegos
    el modo de variación o de encendido / apagado

### grupos

\

Este módulo tiene 2 grupos de asociación.

\

![Groupe](../images/everspring.AD147-6/groupe.jpg)

\

> ** Importante **
>
> Una Jeedom mínimo debería reflejarse en el grupo 1 \

Bueno saber
------------

\

### detalles específicos

\

-   La realimentación de estado no puede ser inferior a 3
    segundos. \

wakeup
------

\

Sin noción de despertar en este módulo.

\

F.A.Q.
------

\

Sí este es el parámetro 2 y no se puede ajustar por debajo de 3
segundos.

\

** ** @ sarakha63
