D-Link DCH-Z110 - "3 en 1 Apertura"
====================================

\

-   ** ** El módulo

\

![module](../images/dlink.dchz110/module.jpg)

\

-   ** El Jeedom visual **

\

![vuedefaut1](../images/dlink.dchz110/vuedefaut1.jpg)

\

resumen
------

\

El sensor DCH-Z110 ofrece tres funciones diferentes: la detección
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
se detecta. Un controlador Z-Wave (mando a distancia, dongle ...?) ¿Es
necesario integrar el detector en su red si tiene
ya una red existente.

\

funciones
---------

\

-   Detector 3 en 1: Apertura, temperatura, luz

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

Sitio web oficial:
<Http://www.dlink.com/-/media/Consumer_Products/DCH/DCH%20Z110/Datasheet/DCH_Z110_Datasheet_FR.pdf>

Otro enlace técnica:
<Http://www.kafkas.gr/uploads/Pdf/182732/DCH-Z120_183010381_01_Z02.PDF>

![caracteristiques
techniques](../images/dlink.dchz110/caracteristiques_techniques.jpg)

\

datos de los módulos
-----------------

\

-   Marca: D-Link

-   Modelo: DCH-Z110 puerta del detector y la abertura de la ventana
    mydlink ™ Inicio

-   Fabricante: Sistema Fibaro

-   Identificación del fabricante: 264 \ [0x0108 \]

-   Tipo de producto: 2 \ [0x0002 \]

-   Identificación del producto: 14 \ [0x000E \]

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
> No instale el módulo en la ventana / puerta antes de tener
> Configurado correctamente y prestar atención a la alineación de
> El imán durante las pruebas en la superficie plana y durante la instalación.
> Utilice cuñas (si es necesario) para activar este modo Módulo
> Inclusión debe ser presionado 3 veces en el botón de asociación 1,5
> En segundo lugar, de acuerdo con su documentación. (Constante roja intermitente
> En el modo de asociación)

\

![config inclusion](../images/dlink.dchz110/config-inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/dlink.dchz110/apres_inclusion.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/dlink.dchz110/commandes.jpg)

\

Estos son los comandos:

\

-   Apertura: este es el comando que se elevará la detección
    apertura

-   Temperatura: la orden de copia de seguridad del
    temperatura

-   Brillo: el comando para aumentar el brillo

-   Sabotaje: el comando de sabotaje (que se dispara
    Si lagrimeo)

-   Batería: el control de la batería

\

### Configuración del módulo

\

> ** Importante **
>
> La primera vez que la inclusión o modificación, a continuación, guardar
> Siempre despertar el módulo pulsando el botón de emparejamiento.
> Debe parpadeará en rojo y cambiar de estado.

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

![Config1](../images/dlink.dchz110/config1.jpg)

![Config2](../images/dlink.dchz110/config2.jpg)

\

Detalles de los parámetros:

\

-   2 ajusta la señal enviada a los módulos del grupo
    Asociación 2

-   4: se utiliza para ajustar el nivel de brillo a la que la
    señal especificada por el parámetro 2 será enviado a los módulos asociados con el
    el grupo 2

-   5: modo de funcionamiento (consulte la
    documentación del fabricante)

-   6: operación de multi-sensor (véase la
    documentación del fabricante). Valor recomendado: 7

-   7: operación personalizada del multisensor (véase
    en la documentación del fabricante). Valor recomendado: 20 (para
    que tiene una abertura funcional)

-   9: juego después de cuánto tiempo la señal estará apagado
    enviado a los módulos asociados con el grupo 2

-   10: ajusta el tiempo entre los informes de la batería (una
    parámetro individual = 20)

-   11: Ajuste el tiempo entre dos informes de apertura automática
    (A parámetro de unidad = 20)

-   12: Establecer la duración entre dos informes de auto
    brillo (unidad = parámetro 20). Valor recomendado: 6

-   13: Establecer la duración entre dos informes de auto
    temperatura (unidad = parámetro 20). Valor recomendado: 2

-   20: duración de un intervalo para los parámetros 10 a 13. Valor
    recomendada: 10

-   21: cantidad de cambio en la temperatura ° F para desencadenar una
    relación

-   valor% de la variación de brillo para trigger: 22
    un informe. Valor recomendado: 10

\

### grupos

\

Este módulo tiene dos grupos de asociación, sólo la primera es
esencial.

\

![Groupe](../images/dlink.dchz110/groupe.jpg)

\

Bueno saber
------------

Asociación / Notificación posible con otros módulos (por ejemplo Siren
DCH-Z510 notificación de timbre en la puerta de apertura / ventana)

\

alternativa visual
-----------------

\

![Groupe](../images/dlink.dchz110/autre_visuel_jeedom.jpg)

\

wakeup
------

\

Para despertar este módulo hay una sola manera de hacer esto:

-   Suelte el botón y vuelva a pulsarlo Asociación

-   Reducir el intervalo de atención en el sistema de configuración / módulo
    (segundos)

\

F.A.Q.
------

\

Este módulo se despierta pulsando el botón de combinación.

\

Este módulo es un módulo de batería, la nueva configuración se
consideración en la próxima despertador. (Botón de emparejamiento para
fuerza, de ahí el interés de no implementar el módulo antes
buena configuración)

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

