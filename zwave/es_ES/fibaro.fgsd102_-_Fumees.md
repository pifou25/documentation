Fibaro FGSD-002 "sensor de humo 2"
================================

\

-   ** ** El módulo

\

![module](../images/fibaro.fgsd102/module.jpg)

\

-   ** El jeedom visual **

\

![vuedefaut1](../images/fibaro.fgsd102/vuedefaut1.jpg)

\

resumen
------

\

Con líneas suaves, una superficie pulida y un tamaño pequeño,
detector de humo se le avisará con una amenaza
LED multicolor RGB y una sirena incorporados. La gran formato
puerta para detectar la cantidad más pequeña de humo para
para obtener una respuesta rápida. Él por lo tanto fácil de encontrar su
lugar en su casa para proteger la seguridad de todos
familia.

El detector de humo Fibaro FGSD-002 es una alarma de sensor
Humo independiente (DAAF) según la norma EN 14604: 2005. Bien
autónoma, sino que también se está comunicando con la tecnología Z-Wave
Más.

Algunos materiales se queman sin fumar. Es por eso que los ingenieros
Fibaro decidió incluir una protección adicional en su
detector de humo en forma de un sensor de temperatura. Si la
cantidad de humo no es suficiente para disparar la alarma,
el dispositivo todavía será capaz de detectar una amenaza detectando
un cambio rápido de la temperatura causada por el fuego. Cambio
rápidos de temperatura o un aumento de hasta 54 ° C es suficiente
de manera que el sensor de humo detecta una amenaza y las señales a
habitantes de la casa. Sólo este tipo de humo ofertas de sensores
alta eficiencia, independientemente de lo que se quema.

\

funciones
---------

\

-   Detector de humo Z-Wave

-   alimentado por batería

-   sensibilidad del sensor regulable (3 niveles)

-   Protección contra el sabotaje

-   Alarma señalizada por el sonido, una luz LED y un Z-onda de la señal

-   detección de incendios mediante la medición de la temperatura del aire

-   prueba automática eficiencia, realizado cada 5 segundos

-   Probador de cubrir la red Z-Wave integrado

-   Cumple con la norma EN 14604: 2005

-   Z-Wave compatibles Más

-   Fácil instalación - sólo tiene que instalar en un lugar
    o hay un riesgo de incendio

\

Características técnicas
---------------------------

\

-   Tipo de módulo: Transmisor Z-Wave

-   Potencia: Litio 3V CR123A

-   Duración de la batería: 3 años

-   Frecuencia: 868.42 MHz

-   Distancia de transmisión: campo libre 50m, 30m en interiores

-   Dimensiones: 65 x 28 mm (diámetro x altura)

-   Temperatura de funcionamiento: 0-55 ° C

-   Humedad de funcionamiento: 0% - 93%

-   Rango de medición de la temperatura: de -20 a 100 ° C

-   sensibilidad al humo: Nivel 1 - 1.20 +/- 0,5% obs / m; segundo
    nivel - 1,80 +/- 0,5% obs / m; Tercero nivel - 2,80 +/- 0,5% obs / m

-   Nivel de ruido: 85 dB a 3 metros

-   Precisión de medida: 0,5 ° C (en un rango de 0 a 55 ° C)

-   Normas: EMC 2004/108 / CE y R & TTE 199/5 / WE

-   Certificaciones: EN 14604: 2005

\

datos de los módulos
-----------------

\

-   Marca: Grupo Fibar

-   Nombre: Fibaro Humo Sensor FGSD-002

-   Identificación del fabricante: 271

-   Tipo de producto: 3074

-   Identificación del producto: 4098

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
> Botón central de la inclusión, de acuerdo con su documentación en papel.

\

![inclusion](../images/fibaro.fgsd102/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/fibaro.fgsd102/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/fibaro.fgsd102/commandes.jpg)

\

Estos son los comandos:

\

-   Humos: el comando de alerta (por módulo de humo,
    calor ...)

-   Temperatura: el control de la temperatura de medición

-   Sabotaje: el sabotaje de control. Se señala la apertura
    la vivienda

-   Prueba de Alerta: Este es el comando que se elevará que el módulo
    es una prueba

-   Alerta de calor: Este es el comando que ascender una alerta de calor
    (Aún no fiable)

-   Batería: el control de la batería

\

### Configuración del módulo

\

> ** Importante **
>
> Cuando inclusión por primera vez todavía despierta en el módulo justo después de
> Inclusión.

\

A continuación, es necesario la configuración del módulo
Dependiendo de su configuración. Para ello es necesario pasar por el botón
"Configuración" plug-in OpenZwave Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

Se llega en esta página (después de hacer clic en la pestaña
Configuraciones)

\

![Config1](../images/fibaro.fgsd102/config1.jpg)

![Config2](../images/fibaro.fgsd102/config2.jpg)

\

Detalles de los parámetros:

\

-   Despertar: este es el intervalo de despertador del módulo (valor
    Recomendado 21600)

-   1: Ajusta la sensibilidad del detector de humo

-   2: Elige qué notificaciones se enviarán a Jeedom
    (Pista: todos)

-   3: Elige qué notificaciones se acompaña de
    indicación visual

-   4: Elige qué notificaciones se acompaña de
    indicación audible (en todos los casos las detecciones de calor y
    fuego sonará el módulo)

-   10: no cambie esto a menos que sepa lo que
    hacer

-   11: ídem

-   12: ídem

-   13: para notificar a otros módulos Zwave (a menos incapacitante
    Sabe por qué se enciende)

-   20: longitud entre dos informes de temperatura

-   21: Diferencia de temperatura a la que, incluso si la duración
    no se alcanza la anteriormente, la temperatura será enviado a Jeedom

-   30: activación de la alarma de temperatura Heat

-   31: intervalo de picos de temperatura de señalización

-   32: intervalo de señal de modo Zwave pérdida

\

### grupos

\

Para un funcionamiento óptimo del módulo. Jeedom debe ser
asociado con mínimos en los grupos 1 4 y 5:

\

![Groupe](../images/fibaro.fgsd102/groupe.jpg)

\

Bueno saber
------------

\

### detalles específicos

\

### alternativa visual

\

![widget1](../images/fibaro.fgsd102/widget1.jpg)

\

wakeup
------

\

Para despertar este módulo se debe presionar 3 veces el botón central

\

F.A.Q.
------

\

Este módulo se despierta pulsando 3 veces en el botón de la inclusión.

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
