SRT seguro 323 "Termostato"
===========================

\

-   ** ** El módulo

\

![module](../images/secure.srt323/module.jpg)

\

-   ** El jeedom visual **

\

![vuedefaut1](../images/secure.srt323/vuedefaut1.jpg)

\

resumen
------

\

El SRT323 es una batería termostato de pared operado. Tiene
un botón giratorio que permite al usuario ajustar la temperatura
establecido en la habitación. Este termostato incorpora un relé de control
carga. Por lo tanto, no es necesario instalar una cerca actuador
caldera.

Al marcar la temperatura programada con la temperatura real
medido, el termostato decide operar la caldera. también este
termostato incorpora un TPI algoritmo (Tiempo proporcional-integral)
lo que permite la optimización y una más justa regulación de la temperatura
su entorno.

El termostato puede recibir la temperatura fijada de otro
controlador Z-Wave, y también puede ser utilizado como un sensor
temperatura. El termostato en sí no tiene un temporizador incorporado, pero
realiza la Z-Wave comandos y comandos locales.

Puede ser utilizado como un reemplazo directo para los termostatos
existente, sin necesidad de cambios en el cableado. el algoritmo
TPI optimizará el encendido y apagado de la caldera
a fin de mantener mejor la temperatura establecida sin
"Sobreimpulso" de la misma. Se ha demostrado que los controladores de TPI
puede proporcionar un importante ahorro energético en comparación con
controladores de calefacción tradicionales.

El SRT323 es un socio ideal para su uso con puerta de enlace
domótica, que le permite controlar de forma remota el sistema de
calefacción. Usted no tendrá que preocuparse de ir a casa de
una casa fría, siempre y cuando usted tiene un teléfono inteligente, tableta o
PC práctico y conectado a Internet.

\

funciones
---------

\

-   Termostato para aplicaciones domésticas

-   Sustituye a un termostato existente

-   Inalámbrica Z-Wave

-   Pantalla LCD con retroiluminación

-   Fácil de usar

-   Compatible con otros productos Z-Wave

-   Un botón

\

Características técnicas
---------------------------

\

-   Tipo de módulo: Z-Wave Controlador

-   Algorythme integrado TPI

-   Relé: 3 (1) A 230V AC

-   temperatura ajustable rango de 5 ° C a 30 ° C

-   Potencia: 2 pilas AAA (LR3)

-   Duración de la batería: 2 años

-   Frecuencia: 868.42 MHz

-   Rango: hasta 50 m en campo abierto

-   Protección: IP30

-   Temperatura de funcionamiento: 0 ° C a 40 ° C

-   Dimensiones: 86 x 86 x 36,25 mm

\

datos de los módulos
-----------------

\

-   Marca: Horstmann

-   Nombre: SRT 323 Electronic termostato de ambiente y temperatura

-   Identificación del fabricante: 89

-   Tipo de producto: 1

-   Identificación del producto: 4

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
> Para poner esto inclusión modo de módulo debe poner el interruptor 1
> ON y el dial para visualizar L y pulsarlo,
> Acuerdo con su documentación en papel.

\

![inclusion](../images/secure.srt323/inclusion.jpg)

\

> ** Importante **
>
> Este módulo es caprichosa al inicio del estudio. Durante una primera inclusión
> Siempre despertar en el módulo justo después de la inclusión. para hacer
> Que el interruptor 1 en la posición ON y luego con el dial Fijarte
> Posición "N" y pulse el botón. Presione de nuevo después de
> 10 segundos para estar seguro. Una vez hecho esto, haga clic en el botón
> Sincronizar (visibles para expertos) junto a los botones
> Inclusión / exclusión. A continuación, en la página de módulo de clic
> La lente superior derecha.

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/secure.srt323/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/secure.srt323/commandes.jpg)

\

Estos son los comandos:

\

-   Temperatura: el control de la temperatura de medición

-   ConsigneEtat: el orden da el conjunto actual

-   Instrucciones: Este es el comando para ajustar el valor de consigna

-   calentador de Estado: el comando de si el
    termostato está en modo de calefacción o no

-   Batería: el control de la batería

\

### Configuración del módulo

\

A continuación, es necesario la configuración del módulo
Dependiendo de su configuración. Para ello es necesario pasar por el botón
"Configuración" plug-in OpenZwave Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

Se llega en esta página (después de hacer clic en la pestaña
configuraciones)

\

![Config1](../images/secure.srt323/config1.jpg)

\

Detalles de los parámetros:

\

-   1: habilitar o no el sensor de temperatura interno

-   2: Elija la unidad de temperatura

-   3: Establecer la variación de la temperatura de cojinete para
    el módulo de la parte posterior (en unidades de 0,1 ° C)

\

### grupos

\

Para un funcionamiento óptimo de su módulo debe ser Jeedom
asociado con 5 grupos

\

![Groupe](../images/secure.srt323/groupe.jpg)

\

Bueno saber
------------

\

### detalles específicos

\

> ** Importante **
>
> Este módulo se alimenta de la batería. Por eso es importante tener en cuenta que
> Cambio de consigna sólo se considerará estela. por
> Raíz por defecto es de hasta 86.400 segundos. Se recomienda encarecidamente
> Disminución de unos 10 minutos. Así, un cambio de consigna se
> Dirigido por el módulo hasta después de 10 minutos

\

wakeup
------

\

Para despertar este módulo es necesario para cambiar 1 ON y
con el mando seleccione No y pulse el dial.

\

F.A.Q.
------

\

\

Este módulo es un módulo de batería, la nueva configuración se
consideración en la próxima activación.

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
