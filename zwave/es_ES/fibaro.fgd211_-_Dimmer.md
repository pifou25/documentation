Fibaro Dimmer - FGD-211
=======================

\

-   ** ** El módulo

\

![module](../images/fibaro.fgd211/module.jpg)

\

-   **El Jeedom visual**

\

![vuedefaut1](../images/fibaro.fgd211/vuedefaut1.jpg)

\

resumen
------

\

El controlador micromódulo FGD-211 le permitirá controlar una
lámpara o la distancia hasta el techo con el protocolo Z-Wave mientras
conservando su interruptor existente.

Por lo tanto, usted será capaz de operar la lámpara conectada y variar su
la intensidad con el interruptor existente, un emisor o Z-Wave
directamente desde este botón en el micromódulo. El es
compatible con cualquier tipo de lámpara de apoyo a la variación
(Incandescente, fluorescente compacta, LED, ...). La unidad micromódulo Fibaro
es un concentrado de tecnología, que detecta automáticamente el tipo de
carga conectada y está protegido contra sobretensiones.

Para bombillas fluorescentes que no son compatibles con el cambio, el
módulo actúa automáticamente como un módulo de conmutación (ON / OFF
solamente).

Se puede utilizar en el modo 2 hijo (sin neutro), para reemplazar una
interruptor existente, o de tres hilos con una alimentación convencional
módulo (Fase + Neutro).

Para lámparas con muy bajo consumo de energía (lámpara de LED
), Puede utilizar la carga (bypass) FGB-001 que permite a una
el funcionamiento correcto del módulo. Un controlador Z-Wave (control remoto,
dongle ...) es necesario para integrar el detector en su red
si ya dispone de una red existente. Cada uno funciona el módulo Z-Wave
como un repetidor inalámbrico con otros módulos para asegurar
La cobertura total de su hogar.

\

funciones
---------

\

-   Ordenar la iluminación a distancia

-   Se instala detrás de un interruptor existente

-   ON / OFF función y el Cambio

-   Modo de uso 2 hijo (neutro no es obligatorio)

-   Detección automática de carga

-   Protegido contra sobrecarga

-   Pequeña, discreta y estética

-   Facilidad de uso e instalación

\

Características técnicas
---------------------------

\

-   Tipo de módulo: el receptor Z-Wave

-   Fuente de alimentación: 230V, 50Hz

-   Cableado: neutral no requiere

-   Carga máxima: 25-500W (carga resistiva) o 1.5A (carga inductiva)

-   Tipo de Lámpara Apoyado (regulable): incandescente, CFL,
    Halógeno (230VAC y 12VDC con transformador electrónico), LEDs

-   soportes de tipo lámpara (no regulable): CFL, LED

-   Fusible: 2.5A

-   Frecuencia: 868.42 MHz

-   Distancia de transmisión: campo libre 50m, 30m en interiores

-   Dimensiones: 15 x 42 x 36 mm

-   Temperatura de funcionamiento: 0-40 ° C

-   Límite de temperatura: 105 ° C

-   Normas: EN 55015 y EN 60669-2-1

\

datos de los módulos
-----------------

\

-   Marca: Grupo Fibar

-   Nombre: Fibaro GSMF-001 \ [sensor de movimiento \]

-   Identificación del fabricante: 271

-   Tipo de producto: 256

-   Identificación del producto: 4106

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

![inclusion](../images/fibaro.fgd211/inclusion.jpg)

\

> **Tip**
>
> Si ya ha integrado el módulo a la pared, puede incluir
> Por muchos a volver en el interruptor o muchos
> Soporte si tiene un botón interruptor.

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/fibaro.fgd211/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/fibaro.fgd211/commandes.jpg)

\

Estos son los comandos:

\

-   Intensidad: Este es el comando para ajustar la intensidad de la
    luz

-   Uno: Este es el comando para encender la luz

-   Apagado: Este es el comando para apagar la luz

-   Estado: Este es el comando que permite conocer el estado de la
    luz

Tenga en cuenta que la información completa salpicadero se puede encontrar en la misma
icono

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

![Config1](../images/fibaro.fgd211/config1.jpg)

![Config2](../images/fibaro.fgd211/config2.jpg)

![Config3](../images/fibaro.fgd211/config3.jpg)

\

Detalles de los parámetros:

\

-   1: Funciones ALL ON / OFF ALL: utilizar si se han asociado la
    DGC-211 a otro módulo

-   6: a decir cómo se envía la información al grupo
    asociación 1

-   7: Puede comprobar si el estado del módulo asociado antes
    el envío de un comando

-   8 establece el porcentaje de cambio (automático)

-   9: longitud de la variación entre los dos extremos (manual)

-   10: duración de la variación entre los dos extremos (auto)

-   11: ajusta el porcentaje de cambio (manual)

-   12: Establece el nivel máximo permitido

-   13: Establece el nivel mínimo permitido

-   14: AJUSTE NOTA: se utiliza para seleccionar el interruptor
    BIESTABLE o MONOSTABLE (botón pulsador)

-   15: activa la opción de traer el brillo al máximo
    en doble apoyo (o retorno de la biestable)

-   16: opción para activar el almacenamiento del último estado

-   17: elegir entre la moda va y viene y el modo de
    contactor

-   18: Sincronizar la variación de nivel a la otra
    unidades asociadas

-   19: operación de usuario del conmutador biestable (inversión
    o no)

-   20: Ajuste el nivel mínimo para bombillas LED
    por ejemplo regulable

-   30: Ajuste el modo de funcionamiento del módulo en el caso
    recibir una señal de emisión de alarma

-   duración de la alarma definido parámetro 30: 39

-   41: activar o no la función de activaciones escenas

\

### grupos

\

Este módulo tiene tres grupos de asociación, sólo el tercero es
esencial.

\

![Groupe](../images/fibaro.fgd211/groupe.jpg)

\

Bueno saber
------------

\

### detalles específicos

\

> **Atención**
>
> La configuración de parámetro más importante es 14.
> Selecciona el tipo de interruptor utilizado. El tipo de defecto
> Está establecido en tiro.

\

Si desea excluir / incluir el módulo sin necesidad de retirar su
cambiar puede pulsar repetidamente el conmutador
(O ir y venir en el interruptor de lado bi)

\

### alternativa visual

\

![vuewidget](../images/fibaro.fgd211/vuewidget.jpg)

\

wakeup
------

\

Sin noción de despertar en este módulo.

\

F.A.Q.
------

\

No. este módulo puede incluir o excluir en varias ocasiones
en el interruptor.

\
** ** @ sarakha63
