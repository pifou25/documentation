Everspring Minienchufe de encendido / apagado - AN180-6
====================================

\

-   ** ** El módulo

\

![module](../images/everspring.AN180-6/module.jpg)

\

-   **El Jeedom visual**

\

![vuedefaut1](../images/everspring.AN180-6/vuedefaut1.jpg)

\

resumen
------

\

Mini jack de encendido / apagado está diseñado para controlar el encendido y
la extinción de las luces y los aparatos eléctricos en su
casa. Con una tensión de 220 - 240 V, este zócalo puede soportar una
cargar hasta 1500W (resistencia), 800W (incandescente), 200W (motor,
fluorescente, LED).

Mini jack On / Off es un dispositivo compatible con Z-Wave ™ que se pretende
para trabajar con todas las redes compatibles con Z-Wave ™. Ella puede
ser controlado por un mando a distancia, software PC o cualquier
controlador Z-Wave en su red.

\

funciones
---------

\

-   Control de una lámpara o un dispositivo remoto

-   Módulo tomada para ser incorporado directamente entre una toma eléctrica y
    la carga a ser controlado

-   ON / OFF función a la luz piloto o dispositivos (no
    de variación)

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

-   Potencia máxima: carga resistiva: 1500W bombilla de incandescencia
    : 800W, fluorescente: bombilla LED 200W (no regulable):
    200W

-   Frecuencia: 868.42 MHz

-   Rango: hasta 70 m en el exterior, hasta 30 m en edificios

-   Pantalla: LED en el botón

-   Dimensiones: Longitud (incluyendo socket): Diámetro 74 mm: 52 mm

\

datos de los módulos
-----------------

\

-   Marca: Everspring

-   Nombre: Minienchufe de encendido / apagado

-   Identificación del fabricante: 96

-   Tipo de producto: 4

-   Identificación del producto: 7

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
> Para poner este modo la inclusión del módulo se debe presionar tres veces en su
> Button, de acuerdo con su documentación en papel. Es importante
> Tenga en cuenta que este módulo se procederá directamente a la inclusión cuando
> No pertenece a ninguna red y es alimentado

\

![inclusion](../images/everspring.AN180-6/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/everspring.AN180-6/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados a los módulos
disponible.

\

![Commandes](../images/everspring.AN180-6/commandes.jpg)

\

Estos son los comandos:

\

-   Estado: Este es el comando que permite conocer el estado de la
    socket (on / off)

-   Uno: Este es el comando para activar el plug

-   Apagado: Este es el comando para apagar el tapón

\

Una nota sobre el tablero de instrumentos, la información de estado, ON / OFF se puede encontrar en
el mismo icono.

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
configuraciones)

\

![Config1](../images/everspring.AN180-6/config1.jpg)

\

Detalles de los parámetros:

\

-   1: Este parámetro define el valor de estado de control, no es
    recomendadas para cambiar este valor.

-   2: Este parámetro define el retardo envía el cambio de estado
    Grupo 1 (entre 3 y 25 segundos)

-   3: Este ajuste determina si la ingesta de recuperar su condición
    (ON u OFF) después de una recuperación de energía.

### grupos

\

Este módulo tiene 2 grupos de asociación.

\

![Groupe](../images/everspring.AN180-6/groupe.jpg)

\

> **Importante**
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
