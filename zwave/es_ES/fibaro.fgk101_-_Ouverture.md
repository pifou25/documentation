Detector de apertura Fibaro - FGK-101
======================================

\

-   ** ** El módulo

\

![module](../images/fibaro.fgk101-DS18B20/module.jpg)

\

-   **El Jeedom visual**

\

![vuedefaut1](../images/fibaro.fgk101-DS18B20/vuedefaut1.jpg)

\

resumen
------

\

Esta batería detector de potencia compatible con Z-Wave tiene un sensor
Reed, un interruptor de proximidad magnético en operación, que
puede detectar la apertura de una puerta o ventana cuando el
dos elementos se eliminan.

El dispositivo consta de una parte con un imán (Parte
móvil), fijado a la puerta o ventana, así como la unidad
Principal posicionada en la parte fija de la ventana / puerta con
tornillos o un adhesivo. Cuando ambas partes ya no están frente a una
señal de radio Z-Wave se envía automáticamente.

Además, este sensor tiene una entrada analógica es posible
la conexión de un sensor de temperatura 1-Wire DS18B20. Este detector tiene
como una entrada de cable, que por lo tanto se puede utilizar como una
control universal: dejar de lado su contacto magnético,
conecte sus entradas para atornillar cualquier sensor (normalmente cerrado) de su
elección, tal como un detector de humo, gas o monóxido de carbono,
etcétera

Se requiere un controlador Z-Wave (control remoto, dongle ...) para
para integrar el detector en su red si ya dispone de una red
existente.

\

funciones
---------

\

-   detector de apertura

-   Botón para incluir / excluir el detector

-   Detección de batería baja

-   protección contra la manipulación

-   1 entrada de cable flotante

-   1 entrada analógica 1-Wire (para conectar una sonda
    DS18B20 temperatura)

-   Muy pequeña, de tamaño compacto

-   Facilidad de uso e instalación

\

Características técnicas
---------------------------

\

-   Tipo de módulo: Transmisor Z-Wave

-   Color: Blanco (FGK-101/102/103/104/105/106/107 de acuerdo con color)

-   Energía: Batería ER14250 (1/2 AA) 3.6V

-   Frecuencia: 868.42 MHz

-   Distancia de transmisión: campo libre 50m, 30m en interiores

-   Dimensiones: 76 x 17 x 19 mm

-   Temperatura de funcionamiento: 0-40 ° C

\

datos de los módulos
-----------------

\

-   Marca: Grupo Fibar

-   Nombre: Fibaro FGK-101 con sensor de temperatura (DS18B20)

-   Identificación del fabricante: 271

-   Tipo de producto: 1792

-   Identificación del producto: 4096

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

![inclusion](../images/fibaro.fgk101-DS18B20/inclusion.jpg)

\

Una vez incluido usted debe conseguir esto:

\

![Plugin Zwave](../images/fibaro.fgk101-DS18B20/information.jpg)

\

### comandos

\

Una vez reconocido el módulo, los comandos asociados con el módulo serán
disponible.

\

![Commandes](../images/fibaro.fgk101-DS18B20/commandes.jpg)

\

Estos son los comandos:

\

-   Estado: Este es el comando que va a subir el estado abierto o cerrado
    módulo

-   Batería: Este es el comando para realizar copias de seguridad del estado de la
    batería

\

Puede ocultar o mostrar estos comandos como desee.

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
Configuraciones)

\

![Config1](../images/fibaro.fgk101-DS18B20/config1.jpg)

![Config2](../images/fibaro.fgk101-DS18B20/config2.jpg)

\

Detalles de los parámetros:

\

-   Despertador: Este es el intervalo de la alarma del módulo (valor
    Recomendado 7200)

-   1: Establecer el período de cancelación de entrada de alarma EN
    (Contacto seco)

-   2: Elija si el LED azul parpadeará a la apertura y
    cerrando la puerta con el ejemplo

-   3: Ajuste el tipo de contacto conectado al terminal (IN)

-   5: No se recomienda cambiar esta configuración a menos que sepa por qué
    (Especifica el tipo de señal a Asociación Grupo 1)

-   7: valor enviado a la asociación de grupo 1

-   9: ajustar la transmisión de la señal de cancelación entre la entrada IN
    y la asociación de grupo 1

-   12: ajustar la sensibilidad al cambio de temperatura (si
    un sensor de 1-alambre está conectado al módulo)

-   13: ajustar la señal de transmisión en modo broadcast
    temperatura y tamper

-   14: activar la función de activación de escenas

\

### grupos

\

Este módulo tiene tres grupos de asociación, sólo el tercero es
esencial.

\

![Groupe](../images/fibaro.fgk101-DS18B20/groupe.jpg)

\

Bueno saber
------------

\

### detalles específicos

\

> **Tip**
>
> Este módulo es muy temperamental en la reactivación y requiere muy
> Muy cercano al controlador cuando su inclusión

\

### alternativa visual

\

![vuewidget](../images/fibaro.fgk101-DS18B20/vuewidget.jpg)

\

wakeup
------

\

Para despertar este módulo hay una sola manera de hacer esto:

-   apoyar a 3/4 veces el botón de la inclusión. Puede que sea necesario
    para hacerlo repetidamente (2 o 3)

\

F.A.Q.
------

\

Este módulo se despierta pulsando 3 veces en uno de los botones de manipulación indebida. pero
es necesario que se presiona el otro botón de manipulación indebida.

\

Este módulo en un muy corto alcance. Es aconsejable
la inclusión más cerca de su caja.

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
