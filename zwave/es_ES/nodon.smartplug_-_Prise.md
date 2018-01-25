Nodon inteligente de entrada - Smartplug
====================================

\

-   ** ** El módulo

\

![module](../images/nodon.smartplug/module.jpg)

\

-   ** El Jeedom visual **

\

![vuedefaut1](../images/nodon.smartplug/vuedefaut1.jpg)

\

resumen
------

\

El NodOn® socket remoto se puede controlar a través de una central de domótica
Compatible Wave Z- o Z-Wave Plus® directamente oa través de otra
controladores de Z-Wave o Z-Wave Plus® como remoto Soft,
el interruptor de pared o el mando a distancia Octan NodOn®. norma alemana
(Schuko) o francés (tipo E), la decisión puede enchufar 2
dirección, cabeza arriba o cabeza abajo. Combinado con su diseño delgado, estos 2
características permiten una fácil integración, sin obstruir
tambores adyacentes en una tira. Aprendizaje del acoplamiento con su
controlador requiere sólo unos pocos segundos. Un botón de locales
encender o apagar la salida directamente.

\

funciones
---------

\

-   Detectar la pérdida del sector eléctrico

-   Ergonómico: Posibilidad de conectar la cabeza atrapada / al revés
    bajo

-   Gestión inteligente de alarmas

-   un mejor alcance de radio

-   amperaje máxima: 16A

\

Características técnicas
---------------------------

\

-   Fuente de alimentación: 230V CA +/- 10% - 50 Hz

-   la máxima potencia: 3000W continua cíclico 3500W /
    (Carga resistiva) consumo intrínseca: &lt;1W

-   Temperatura de funcionamiento: 0 ° C a 40 ° C - Altitud: 2000m

-   Protocolo de Z-Wave de radio: 868.4MHz - Serie 500 - compatibles con Z-Wave
    Plus® SDK 06.51.01

-   Rango: 40m 80m interior / exterior

-   Tamaño: 104 \ 51 * \ * 36mm

-   2 años de garantía

-   Tipo de la UE

\

datos de los módulos
-----------------

\

-   Marca: Nodon

-   Nombre: Smartplug

-   Identificación del fabricante: 357

-   Tipo de producto: 1

-   Identificación del producto: 1

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
> Hasta que la luz cambie a rojo, de acuerdo con su documentación
> Papel.

\

![inclusion](../images/nodon.smartplug/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/nodon.smartplug/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/nodon.smartplug/commandes.jpg)

\

Estos son los comandos:

\

-   Estado: Este es el comando que permite conocer el estado de la
    socket (ON / OFF)

-   Uno: Este es el comando para activar el plug

-   Apagado: Este es el comando para apagar el tapón

-   Estado: Muestra si la salida tiene poder o no
    (Detección de corriente / fracaso desconexión)

\

Una nota sobre el tablero de instrumentos, la información de estado, ON / OFF se puede encontrar en
el mismo icono.

\

### Configuración del módulo

\

Se puede configurar la función de su módulo
instalación. Para ello es necesario pasar por el botón "Configuración"
Plugin de Zwave Jeedom.

\

![Configuration plugin Zwave](../images/plugin/bouton_configuration.jpg)

\

Se llega en esta página (después de hacer clic en la pestaña
configuraciones)

\

![Config1](../images/nodon.smartplug/config1.jpg)

![Config1](../images/nodon.smartplug/config2.jpg)

\

Detalles de los parámetros:

\

-   1: Este parámetro define el estado (ON / OFF) de la Smart Plug después de
    fallo de alimentación o después de la conexión

-   2: Este parámetro informes con fi gurar notificación de
    de corte / de retorno de corriente, así como los grupos asociados (Grupos
    4, 5, 6, 7, 8). Varias combinaciones son posibles (véase
    la documentación en papel o en la descripción jeedom). El es
    recomendado para configurar este parámetro en 1.

-   3: Utilice esta configuración para activar o desactivar grupos 2 y 3.

-   4: El ajuste obliga al estado de la Smart Plug "ON" (Smart
    Enchufe habilitado). Cuando se habilita el ajuste, no es
    posible apagar el Smart Plug (local o radio)

-   Parámetros 5 a 20: A través de las configuraciones de los parámetros \ # 5 en
    \ # 20, es posible con fi gurar hasta 8 alarmas diferentes.
    Con el fin de adecuadamente con fi gurar sus alarmas, el formulario en línea:
    www.nodon.fr/support/asp3/alarm orientarle

### grupos

\

Este módulo tiene 8 grupos de asociación.

\

![Groupe](../images/nodon.smartplug/groupe.jpg)

\

-   Grupo 1 - Supervivencia: Este grupo se utiliza generalmente para
    Ver información del Smart Plug el controlador principal
    red.

-   Grupo 2 - Monitorización del estado del Smart Plug Cuando el Smart Plug
    se activa (desactivado respectivamente) a través del botón local,
    se envía un comando de activación
    (Respectivamente desactivación) para los dispositivos asociados. no
    comando es enviado si el cambio de estado de la Smart Plug tiene
    fue causado por un control de radio

-   Grupo 3 - Monitorización del estado complementario cuando el Smart Plug
    se activa (desactivado respectivamente) a través del botón local,
    se envía un comando de desactivación
    (Activación respectivamente) a los dispositivos asociados. no
    comando es enviado si el cambio de estado de la Smart Plug tiene
    fue causado por un control de radio.

-   Grupo 4 - Noti fi cación de fallo de alimentación Cuando el tapón eficaz
    detecta se restaura un corte de energía o potencia, un informe
    de la notificación se envía a los dispositivos asociados. El informe enviado
    es un "noti fi cación Informe: Gestión de corriente - CA desconectadas
    / Re conectado).

-   Grupo 5 - interrupción de activación Cuando el Smart Plug
    detecta un fallo de alimentación, activa los dispositivos asociados.

-   Grupo 6 - suspensión del servicio de desactivación Cuando el Smart
    Plug detecta un fallo de alimentación, que desactiva los dispositivos
    conexo

-   Grupo 7 - Activación de retorno de corriente Cuando el Smart Plug
    detecta un retorno de la corriente, que activa los dispositivos asociados.

-   Grupo 8 - Activación de retorno de corriente Cuando el Smart Plug
    detecta un retorno de corriente, desactiva los dispositivos asociados

\

> ** Importante **
>
> Una Jeedom mínimo debe reunirse en los grupos 1 y 4 \

Bueno saber
------------

\

### detalles específicos

\

-   Es inútil tener diversión conectar / desconectar el enchufe
    observar la alarma. Esto va a trabajar cerca de 3 veces. la
    Más allá de la clavija debe ser alimentado un poco de tiempo para recargar
    la batería interna.

\

wakeup
------

\

Sin noción de despertar en este módulo.

\

F.A.Q.
------

\

Usted no debería tener la opción de descargar los widgets de auto
de activado. Puede recuperar widgets móviles y cuadros de mando en
Mercado: Alarma \ _prise.

\

¿Ha definido el parámetro 2? ¿verdad al menos Jeedom
en los grupos 1 y 4? ¿Se permite el tiempo para que la batería
cargar?

\

** ** @ sarakha63
