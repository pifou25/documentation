Controlador de puerta de garaje Aeotec
====================================

\

-   ** ** El módulo

\

![module](../images/aeotec.garagedoorcontroller/module.jpg)

\

-   **El Jeedom visual**

\

![vuedefaut1](../images/aeotec.garagedoorcontroller/vuedefaut1.jpg)

\

resumen
------

\

Se conecta fácilmente al motor ya existente a su operador de puerta
la puerta del garaje mejora con una suite de seguridad y sensores
seguridad. El controlador de puerta de garaje no sólo permite
controlar la puerta del garaje, sino que también le permite comprobar
su condición. Tanto si se utiliza por motor o manualmente, el detector
Inteligente viene con el controlador de puerta de garaje sabe si la puerta
está abierto o cerrado, y le puede avisar cuando esto ocurre hacer
no debería.

\

funciones
---------

\

-   Controlar y vigilar la puerta del garaje a distancia.

-   Módulo simplemente instalando en su motor
    actual de la puerta.

-   puerta de la sala de control a través del botón integrado.

-   Envía un / alertas de cierre controlador abertura Z-Wave.

-   alertas apertura / cierre audible y visual.

-   volumen de la alarma ajustable (105 dB max)

-   puerto USB para cargar sus propios sonidos MP3.

-   botón de estado LED integrado.

-   Parte de la gama Gen5 Aeon Labs.

-   comunicaciones por radio de seguridad mediante el cifrado AES-128.

-   Se integra inteligente serie Z-Wave 500.

-   Comunicación 250% más rápido en comparación con los dispositivos
    estándar Z-Wave.

-   Mensajes de Z-Wave repetidor.

-   antena optimizado rango de 300 metros.

\

Características técnicas
---------------------------

\

-   Tipo de módulo: El receptor y el transmisor Z-Wave + 500 Series

-   Feed: actuador: 5 VDC (adaptador) Sensor: Pila
    Litio CR2 3V 800mA

-   Consumo de energía: 1W

-   alarma Consumo: 2W

-   Volumen máximo: 105 dB

-   Formatos de audio compatibles: MP3 y WMV a una frecuencia de 320 Kbps

-   Frecuencia: 868.42 MHz

-   La distancia de transmisión: 300m en campo abierto

-   Intervalo de temperatura: -20 ° C a 50 ° C

-   Humedad de funcionamiento: 80%

-   Certificaciones: FCC, UL, CE, RoHS

\

datos de los módulos
-----------------

\

-   Marca: Aeotec

-   Nombre: Controlador de puerta de garaje (ZW062)

-   Identificación del fabricante: 134

-   Tipo de producto: 3

-   Identificación del producto: 62

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
> Z-Wave, de acuerdo con su documentación en papel.

\

![inclusion](../images/aeotec.garagedoorcontroller/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/aeotec.garagedoorcontroller/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/aeotec.garagedoorcontroller/commandes.jpg)

\

Estos son los comandos:

\

-   Abrir / Cerrar: abrir, cerrar o detener la puerta del garaje.

-   Posición: La posición actual de la puerta del garaje.

-   Volumen: volumen actual del altavoz.

-   Temperatura: Temperatura de la zona, no automático vuelve a montar.

-   Sabotaje: Estado de texto sabotaje.

\

### Configuración del módulo

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

![Config1](../images/aeotec.garagedoorcontroller/config1.jpg)

![Config1](../images/aeotec.garagedoorcontroller/config2.jpg)

\

Detalles de los parámetros:

\

-   34: Se utiliza para iniciar la calibración del tiempo de apertura de
    la puerta.

-   41: Permite la selección resetter de sabotaje estado "Aliviar
    el estado de alarma "

-   80: granizo sobre

-   255: Resetter permite la configuración de fábrica

\

### grupos

\

Este módulo tiene dos grupos de asociación. La primera "línea de vida" es
esencial.

\

![Groupe](../images/aeotec.garagedoorcontroller/groupe.jpg)

\

Bueno saber
------------

\

### detalles específicos

Tiempo de apertura de la calibración de la puerta del garaje:

-   1: La puerta del garaje debe estar completamente cerrada.

-   2: Activar el parámetro 34 a "hacer la calibración".

-   3: Iniciar la apertura de la puerta

-   4: Espere hasta que la puerta está completamente abierta.

-   5: empezar a cerrar de la puerta

La calibración se completa

-   El parámetro 34 se actualizará a "Normal".

-   El parámetro 35 se ajusta con el tiempo de apertura de abertura calculada.

\

Restablecer el sabotaje:

-   1: El sensor debe estar configurado correctamente.

-   2: Activar el ajuste de 41 "Aliviar el estado de alarma".

-   3: Actualizar la configuración.

La calibración se completa

-   El parámetro será 41 perforación con "sensor no se quita".

\

F.A.Q.
------

\

\

** ** @ nechry
