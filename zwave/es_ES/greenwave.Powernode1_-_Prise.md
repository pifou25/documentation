Greenwave nodo de poder - 1 tomada
=============================

\

-   ** ** El módulo

\

![module](../images/greenwave.Powernode1/module.jpg)

\

-   ** El Jeedom visual **

\

![vuedefaut1](../images/greenwave.Powernode1/vuedefaut1.jpg)

\

resumen
------

\

El módulo de nodo de poder GreenWave tomada es un dispositivo inteligente que
se conecta a uno de sus electrodomésticos y electrónica para
le permiten supervisar y controlar el consumo de energía a
remota a través de un navegador web o un teléfono inteligente.

Utilizando la tecnología de Z-Wave, zócalo controlado nodo de poder es
compatible con la mayoría del mercado de automatización del hogar como caja de Fibaro
Home Center 2, o eedomus Zipabox.

Nodo de poder de la unidad de receptáculo recopila datos sobre el consumo
la energía dispositivo conectado y transmitirlas a dicho cuadro de automatización del hogar.
Este zócalo controlado también le permite activar o desactivar
el dispositivo de forma remota a través de un navegador web o un teléfono inteligente o un conjunto
un calendario para activar o desactivar el dispositivo automáticamente
a horas preestablecidas.

Un pequeño dial en el lado del conector para elegir un color
que representa la parte a la que se le asigna. Por ejemplo "
azul para la habitación. "Este truco le ayudará a diferenciar su
diferentes tomas y tiras de nodo de poder. También se puede ajustar
este dial para un candado. Esta función bloquea la
tomar para evitar que por accidente, pero el control desde
domótica boxeo no será posible.

La toma de corriente controlada nodo de poder también cuenta con un indicador de estado
luz que da información diferente dependiendo de su color:
tomado encendido o apagado, radio limitado rango, la moda y la inclusión
la exclusión.

Nodo de poder de la unidad de receptáculo está equipado con una protección contra
sobrecorriente para proteger el dispositivo conectado. La decisión nodo de poder
desactiva cuando el mal funcionamiento de un aparato defectuoso o una
cortocircuito. protección adicional es proporcionado por el fusible
internamente en el enchufe.

\

funciones
---------

\

-   Control de una lámpara o un dispositivo remoto

-   Módulo tomada para ser incorporado directamente entre una toma eléctrica y
    la carga a ser controlado

-   Permite que el dispositivo de control del consumo conectado

-   Encendido / apagado

-   Posibilidad de asignar un número y un color de
    diferenciar la misma instalación diferentes nodo de poder

-   Botón de encendido / apagado directamente en espera

-   Protección contra sobrecorriente

-   condición de la luz indicadora

\

Características técnicas
---------------------------

\

-   Fuente de alimentación: 250 V \ ~ CA, 50Hz

-   corriente de carga máxima: 10A

-   potencia de carga máxima: 2400W (@ 240 V)

-   Consumo de energía: 0,4 W

-   Precisión de la medición: ± 0,1 W

-   La protección contra la sobretensión: fusible interno 10A

-   Tipo de enchufe: DIN49440 / CEE 7/7 (Schuko)

-   Radio Frecuencia Z-Wave: 868.42MHz

-   Máximo Z-Wave Rango: 30m

-   Temperatura de funcionamiento: 0 ° C a + 25 ° C

-   Temperatura de almacenamiento: -20 ° C a + 60 ° C

-   máximo de humedad: 5% a 90%

-   Valoración de IP (tolerancia de humedad): IP20

\

datos de los módulos
-----------------

\

-   Marca: GreenWave

-   Nombre: GreenWave \ [1 socket \]

-   Identificación del fabricante: 153

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
> Para poner este modo la inclusión del módulo tiene que pulsar el botón
> La inclusión en esta decisión.

\

![inclusion](../images/greenwave.Powernode1/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/greenwave.Powernode1/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/greenwave.Powernode1/commandes.jpg)

\

Estos son los comandos:

\

-   Estado: Este es el comando para conocer el estado de la
    toma

-   Uno: Este es el comando para activar el plug

-   Apagado: Este es el comando para apagar el tapón

-   Potencia: Este es el comando que era la potencia instantánea
    consumida

-   Contras: Este es el comando que fue el consumo total

\

Tenga en cuenta que el salpicadero controla el interruptor ON / OFF / STATUS se agrupan
en un solo botón.

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

![Config1](../images/greenwave.Powernode1/config1.jpg)

\

Como se puede ver que no hay muchos de configuración
para este módulo.

\

Detalles de los parámetros:

\

-   1: Retardo antes de que el botón parpadeante: número de segundos
    mínima entre dos comunicaciones (si se supera el botón de este período
    teniendo flash)

-   2 seleccionada del color de línea (detectado automáticamente)

\

### grupos

\

Este módulo tiene cuatro grupos de asociación, sólo el tercer grupo
esencial.

\

![Groupe](../images/greenwave.Powernode1/groupe.jpg)

\

Bueno saber
------------

\

A diferencia de su gran franja hermana, esta decisión no requiere
Sondeo de hasta el consumo.

\

### reajustar

\

![Config2](../images/greenwave.Powernode1/config2.jpg)

\

Usted puede configurar su medidor de consumo haciendo clic
este botón disponible en la ficha Sistema. Hay que elegir
Botón de control.

\

### detalles específicos

\

wakeup
------

\

Sin noción de despertar en este módulo.

\

F.A.Q.
------

\

Cómo se asocia el grupo 3 del módulo Jeedom?

\

No. El módulo no lo permite. Poner en un pequeño trozo de cinta
adhesivo negro.

\

** ** @ sarakha63
