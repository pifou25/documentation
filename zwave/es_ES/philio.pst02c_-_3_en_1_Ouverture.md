Philio PST02 C - 3 en 1 Apertura
=================================

\

-   ** ** El módulo

\

![module](../images/philio.pst02c/module.jpg)

\

-   **El Jeedom visual**

\

![vuedefaut1](../images/philio.pst02c/vuedefaut1.jpg)

\

resumen
------

\

El sensor postal-PSM01 ofrece tres funciones diferentes: la detección
apertura, sensor de temperatura, y el detector de luz. El se
consta de dos partes: un sensor y un imán. Están diseñados
para ser colocado en una puerta o ventana con el imán unido a la
parte que se abre y el detector en la parte fija.

La apertura de la puerta o ventana se apartan del imán
detector, que activará el detector enviará una señal Z-Wave
alarma si el sistema está armado (esta señal puede ser operado por una
sirena o una caja de automatización, por ejemplo). El sensor puede también
ser utilizado para el control automático de la iluminación, dependiendo de la
nivel de brillo. Por ejemplo, el sensor enviará una señal a
Interruptor de Z-Wave para encender la luz cuando la puerta se abre
y que la habitación está oscura.

El detector también ascender el brillo y la temperatura, ya sea
Si cambio significativo, y cada vez la apertura / cierre
se detecta.

Se requiere un controlador Z-Wave (control remoto, dongle ...) para
para integrar el detector en su red si ya dispone de una red
existente.

\

funciones
---------

\

-   Detector 3 en 1: Apertura, temperatura, luz

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

-   Duración de la batería: 3 años (14 viajes al día)

-   Frecuencia: 868.42 MHz

-   Distancia de transmisión: 30m cubierta

-   Sensor de temperatura: -10 a 70 ° C

-   sensor de luminosidad: 0 a 500 lux

-   dimensiones:

-   Detector: 28 x 96 x 23 mm

-   Imán: 10 x 50 x 12 mm

-   Peso: 52g

-   Rango de temperatura de funcionamiento: -10 a 40 ° C

-   Humedad de funcionamiento: 85% HR max

-   CE: EN300 220-1

-   La certificación Z-Wave: ZC08-13050003

\

datos de los módulos
-----------------

\

-   Marca: Philio Technology Corporation

-   Nombre: C-PST02 puerta / ventana del sensor 3 en 1

-   Identificación del fabricante: 316

-   Tipo de producto: 2

-   Identificación del producto: 14

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
> Para poner este modo la inclusión del módulo debe ser presionado 3 veces en el
> Botón de inclusión, de acuerdo con su documentación en papel.

\

![inclusion](../images/philio.pst02c/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/philio.pst02c/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/philio.pst02c/commandes.jpg)

\

Estos son los comandos:

\

-   Apertura: este es el comando que se elevará la detección
    apertura

-   Temperatura: la orden de copia de seguridad del
    temperatura

-   Brillo: el comando para aumentar el brillo

-   Batería: el control de la batería

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

![Config1](../images/philio.pst02c/config1.jpg)

![Config2](../images/philio.pst02c/config2.jpg)

![Config3](../images/philio.pst02c/config3.jpg)

\

Detalles de los parámetros:

\

-   2 ajusta la señal enviada a los módulos del grupo
    Asociación 2

-   4: se utiliza para ajustar el nivel de brillo a la que la
    señal especificada por el parámetro 2 será enviado a los módulos asociados con el
    el grupo 2

-   5: modo de funcionamiento (consulte la
    Valor documentación del fabricante) Recomendado: 8

-   6: operación de multi-sensor (véase la
    Valor documentación del fabricante) Recomendado: 4

-   7: Modo personalizado del multisensor (véase
    en la documentación del fabricante) Valor recomendado: 20 (para
    que tiene una abertura funcional)

-   9: juego después de cuánto tiempo la señal estará apagado
    enviado a los módulos asociados con el grupo 2

-   10: ajusta el tiempo entre los informes de la batería (una
    parámetro individual = 20)

-   11: Ajuste el tiempo entre dos informes de apertura automática
    (A parámetro de unidad = 20)

-   12: Establecer la duración entre dos informes de auto
    brillo (unidad = parámetro 20) Recomendado valor 3

-   13: Establecer la duración entre dos informes de auto
    temperatura (unidad = 20 parámetros) Valor recomendado: 2

-   20: duración de un intervalo de parámetros 10-13 Valor
    recomendada: 10

-   21: cantidad de cambio en la temperatura ° F para desencadenar una
    relación

-   22: Valor de% de variación de brillo para desencadenar una
    reportar el valor recomendado: 10

\

### grupos

\

Este módulo tiene dos grupos de asociación, sólo la primera es
esencial.

\

![Groupe](../images/philio.pst02c/groupe.jpg)

\

Bueno saber
------------

\

### alternativa visual

\

![vuewidget](../images/philio.pst02c/vuewidget.jpg)

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

Este módulo es un módulo de batería, la nueva configuración se
consideración en la próxima despertador.

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
