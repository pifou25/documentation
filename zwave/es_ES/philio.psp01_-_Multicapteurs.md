Philio PSP01
============

\

-   ** ** El módulo

\

![module](../images/philio.psp01/module.jpg)

\

-   ** El Jeedom visual **

\

![vuedefaut1](../images/philio.psp01/vuedefaut1.jpg)

\

resumen
------

\

El detector de PSP01 ofrece 3 funciones diferentes: detección
movimiento, sensor de temperatura, y el detector de luz.

Este detector se puede utilizar para la seguridad o
automatización. Cuando el detector se asocia con dispositivos
la seguridad, que sirve como una alerta de activación por detección de
cambios en los niveles de la radiación infrarroja. Si una persona
se mueve en el campo de visión del detector, una señal de radio es
transmitida, lo que desencadena una alarma para disuadir a los intrusos.

El sensor también puede ser usado en combinación con una
controlador Z-Wave para fines de automatización, mediante la detección tanto
cambios en los niveles de radiación de infrarrojos (presencia) y
los cambios en el nivel de brillo. Por lo tanto, se puede desencadenar una
iluminación después de la detección de movimiento en la oscuridad.

El detector también ascender el brillo y la temperatura, ya sea
Si cambio significativo, y cada vez que un movimiento es
detectado. Se requiere un controlador Z-Wave (control remoto, dongle ...)
para integrar el detector en su red si ya tiene una
red existente.

\

funciones
---------

\

-   Detector 3 en 1: el movimiento, temperatura, luz

-   Adopta el último chip Z-Wave para apoyar 400series
    operaciones multicanal y una velocidad de datos
    alta (9,6 / 40/100 kbps)

-   Utilizar el Z-Wave SDK 6.02

-   Ámbito de aplicación de la antena optimizado

-   El uso para la automatización del hogar o aplicaciones de seguridad

-   Botón para incluir / excluir el detector

-   manosear

-   Indicador de batería baja

-   Pequeña, discreta y estética

-   Facilidad de uso e instalación

\

Características técnicas
---------------------------

\

-   Tipo de módulo: Transmisor Z-Wave

-   Fuente de alimentación: 1 CR123A 3V

-   Duración de la batería: 2 años

-   Frecuencia: 868.42 MHz

-   Distancia de transmisión: 30m cubierta

-   Sensor de temperatura: -10 a 70 ° C

-   sensor de luminosidad: 0 a 500 lux

-   PIR ángulo de detección: 90 °

-   PIR rango de detección: 8 a 10m

-   Dimensiones: 28 x 96 x 23 mm

-   Peso: 39g

-   Rango de temperatura de funcionamiento: -10 a 40 ° C

-   Humedad de funcionamiento: 85% HR max

-   CE: EN300 220-1

-   La certificación Z-Wave: ZC08-13050003

\

datos de los módulos
-----------------

\

-   Marca: Philio Technology Corporation

-   Nombre: Philio PSP01

-   Identificación del fabricante: 316

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

> ** Importante **
>
> Para poner este modo la inclusión del módulo debe ser presionado 3 veces en el
> Botón de inclusión, de acuerdo con su documentación en papel.

\

![inclusion](../images/philio.psp01/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/philio.psp01/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/philio.psp01/commandes.jpg)

\

Estos son los comandos:

\

-   Presencia: es el comando que ascienden detección de presencia

-   Apertura: este es el comando que se elevará la detección
    apertura

-   Temperatura: la orden de copia de seguridad del
    temperatura

-   Brillo: el comando para aumentar el brillo

-   Sabotaje: el comando de sabotaje (que se dispara
    Si lagrimeo)

-   Batería: el control de la batería

\

Todos los módulos de la gama con los mismos ID para ver los
correspondiente a su módulo.

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
Configuraciones)

\

![Config1](../images/philio.psp01/config1.jpg)

![Config2](../images/philio.psp01/config2.jpg)

\

Detalles de los parámetros:

\

-   2 ajusta la señal enviada a los módulos del grupo
    Asociación 2

-   3: Ajuste de la sensibilidad del sensor de presencia (0:
    99 desactivado: sensibilidad máxima)

-   4: se utiliza para ajustar el nivel de brillo a la que la
    señal especificada por el parámetro 2 será enviado a los módulos asociados con el
    el grupo 2

-   5: Modo de funcionamiento (no se recomienda cambiar: ver
    en la documentación del fabricante)

-   6: funcionamiento de multi-sensor (no se recomienda cambiar la
    : Consulte la documentación del fabricante)

-   9: juego después de cuánto tiempo la señal estará apagado
    enviado a los módulos asociados con el grupo 2

-   10: ajusta el tiempo entre los informes de la batería (una
    unidad = 30 minutos)

-   12: establecer el tiempo entre dos relaciones de brillo
    (Unidad = 30 minutos)

-   13: Ajuste el tiempo entre dos informes de temperatura
    (Unidad = 30 minutos)

\

### grupos

\

Este módulo tiene dos grupos de asociación, sólo la primera es
esencial.

\

![Groupe](../images/philio.psp01/groupe.jpg)

\

Bueno saber
------------

\

### detalles específicos

\

> ** Tip **
>
> Este módulo tiene una característica, no tener un informe basado en
> Variaciones, pero sólo con el tiempo, se envía toda la información a
> Cada detección. También envió varias veces la señal
> Detección de presencia como resultado. Por tanto, es aconsejable comprobar la
> Box "evento de cambio" de la presencia si se utiliza este
> Activador de guión de comando.

\

### alternativa visual

\

![vuewidget](../images/philio.psp01/vuewidget.jpg)

\

wakeup
------

\

Para despertar este módulo hay una sola manera de hacer esto:

-   manipular suelte el botón y pulse de nuevo

\

F.A.Q.
------

\

Este módulo se despierta pulsando el tamper botón.

\

Marque la casilla "Evento de cambio".

\

Este módulo es un módulo de batería, la nueva configuración se
consideración en la próxima despertador.

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
