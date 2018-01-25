Asegure SIR 321 "temporizador"
======================

\

-   ** ** El módulo

\

![module](../images/secure.sir321/module.jpg)

\

-   ** El jeedom visual **

\

![vuedefaut1](../images/secure.sir321/vuedefaut1.jpg)

\

resumen
------

\

El SIR321 temporizador digital es un simple interruptor de
pulsador que recuerda a apagar, para usted, sus dispositivos
eléctrica. son posibles grandes ahorros de energía mediante la adición
este sencillo dispositivo en cualquier dispositivo eléctrico de alta potencia,
Ir con cargas de hasta 3 kW (resistiva).

Estas unidades son ideales para su uso en los signos
de calentamiento, calentadores de inmersión, toalla y enfriadores de aceite. la
impulso es de 30 a 120 minutos.

SIR 321 soporta sensores de temperatura externa SES001,
SES002 y SES003.

\

funciones
---------

\

-   calentador de refuerzo, el panel radiador, toalla,
    baño de aceite radiador

-   Temporizador para la caldera

-   La ventilación forzada en salas de conferencias

-   Medición de la temperatura de calentamiento de suelo (con sensores opcionales)

-   Fácil de usar y fiable

-   Darse cuenta de ahorro de energía

\

Características técnicas
---------------------------

\

-   Tipo: Temporizador electrónico

-   RELAIS 13 (3) A, 230V AC, idóneo para cargas de hasta llegados
    3 kW

-   Fuente de alimentación: 230 V CA, 50 Hz

-   dimensiones 85x85x44mm

-   Protección: IP30

-   Temperatura de funcionamiento: 0 ° C a 35 ° C

\

datos de los módulos
-----------------

\

-   Marca: Horstmann

-   Nombre: SIR 321 temporizador de cuenta regresiva de RF

-   Identificación del fabricante: 89

-   Tipo de producto: 1/2 (dependiendo de si se incluye con una sonda
    temperatura o no)

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
> Para poner este modo la inclusión del módulo hay que pulsar 1 segundo
> Botón (a parpadeo rápido) y la liberación de conformidad con
> Su documentación en papel.

\

![inclusion](../images/secure.sir321/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/secure.sir321/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/secure.sir321/commandes.jpg)

\

Estos son los comandos:

\

-   Uno: la orden de entregar

-   Apagado: este es el comando para apagar el relé

-   Temperatura: la medición de la temperatura de control si una
    sonda externa está presente

\

### Configuración del módulo

\

Si desea configurar el módulo que tiene que utilizar el botón
"Configuración" plug-in OpenZwave Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

Se llega en esta página (después de hacer clic en la pestaña
configuraciones)

\

![Config1](../images/secure.sir321/config1.jpg)

\

Detalles de los parámetros:

\

-   1: Habilitar o no la función de temporizador a prueba de fallos (véase
    la documentación del módulo)

-   2: Ajuste la unidad de temperatura

-   3: Establecer el intervalo de enviar el tiempo de la temperatura
    a Jeedom (en segundos)

-   4: ajustar la cantidad debe variar la temperatura para ese
    el módulo envía a Jeedom (en 0,1 10- → 0.1)

-   5: Ajuste una temperatura de corte más allá del cual
    el módulo de relé

\

### grupos

\

Este módulo tiene dos grupos de asociación. Si el primero es
esencial, el segundo es activa y es esencial si una sonda
temperatura está conectado.

\

![Groupe](../images/secure.sir321/groupe.jpg)

F.A.Q.
------

\

** ** @ sarakha63
