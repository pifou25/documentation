Aquí hay un tutorial para instalar VMware en Intel NUC (Gen6). nosotros
ver más adelante cómo añadir más Jeedom

El material
===========

Intel NUC
---------

El procesador Intel NUC es un pequeño ordenador, no es el más potente, pero muy eficiente
energía y pequeñas dimensiones. Esto hace que sea un pequeño servidor perfecta
virtualización basada en VMware.

En este momento hay 2 6ª generación (NUC otros caminan
VMware también, pero hay que poner más conductores en la
VMware núcleo):

-   Intel Core i3-6100U (2,3 GHz de doble núcleo - - 4 hilos - 3 MB de caché -
    TDP 15W)

-   Intel Core i5-6260U (1,8 GHz de doble núcleo del procesador - Turbo 2.9 GHz - 4 hilos -
    Caché de 4 MB)

El i5 es mucho más potente porque tiene un poco más caché
y sobre todo un modo turbo que le permite ir mucho más alta en
frecuencia.

Y viene con dos tipos de casos:

-   Una carcasa final sólo puede contener un tipo de disco M2

-   carcasa más gruesa puede contener un tipo de disco M2 y una
    disco de 2,5 pulgadas

Eso hace cuatro referencias:

-   i3 M2: [Intel NUC
    NUC6I3SYK] (http://www.ldlc.com/fiche/PB00203086.html) \ ~ 320 €

-   2.5pouces i3 M2 +: [Intel NUC
    NUC6I3SYH] (http://www.ldlc.com/fiche/PB00203148.html) \ ~ 320 €

-   i5 M2: [Intel NUC
    NUC6I5SYK] (http://www.ldlc.com/fiche/PB00203084.html) \ ~ 460 €

-   2.5pouces i5 M2 +: [Intel NUC
    NUC6I5SYH] (http://www.ldlc.com/fiche/PB00202760.html) \ ~ 430 €

SSD
---

Hay que añadir a esto un SSD y la memoria. DSS Nivel I se
recomienda 240 GB o más, a menos que tome el modelo con una
2,5 pulgadas ubicación (que le permite conducir más)
o tener una especie de Synology NAS para iSCSI LUN. No olvidar
una base de VM (sin almacenamiento) es de entre 20 a 40 GB, añadir a
este 40GB por sí mismo VMware se llena rápido.

> ** Importante **
>
> VMware no admite la adición de disco USB, es difícil
> Para ampliar el espacio disponible

-   [2280 LDLC SSD M.2 F6 PLUS 120
    GB] (http://www.ldlc.com/fiche/PB00203635.html) \ ~ 55 €

-   [120 GB SSD Samsung 850 EVO
    M.2] (http://www.ldlc.com/fiche/PB00185923.html) \ ~ 100 €

-   [C-LDL SSD M.2 2280 F6 MAS 240
    GB] (http://www.ldlc.com/fiche/PB00203636.html) \ ~ 105 €

-   [250 GB SSD Samsung 850 EVO
    M.2] (http://www.ldlc.com/fiche/PB00185924.html) \ ~ 120 €

-   [LDLC SSD M.2 2280 F6 MÁS 480
    GB] (http://www.ldlc.com/fiche/PB00207301.html) \ ~ 190 €

memoria
-------

Advertencia para la memoria es imprescindible para DDR4 en So-DIMM 260
pinos, se necesitan al menos 4 GB de VMware, pero por experiencia os
recomienda al menos 8 GB (personalmente hasta fui hasta 16 GB,
la NUC admite un máximo de 32 GB). Hay, sin memoria recomendada,
más barato es fina (Siempre tomo 2 paquetes de cuidado
bares, esto mejora el rendimiento):

-   [Crucial SO-DIMM DDR4 8 GB (2 x 4 GB) 2133 MHz CL15 SR
    X8] (http://www.ldlc.com/fiche/PB00204134.html) \ ~ 35 €

-   [Crucial DDR4 SO-DIMM 16 GB (2 x 8 GB) 2133 MHz CL15 DR
    X8] (http://www.ldlc.com/fiche/PB00204135.html) \ ~ 65 €

-   [Crucial DDR4 SO-DIMM 32 GB (2 x 16 GB) 2133 MHz CL15 DR
    X8] (http://www.ldlc.com/fiche/PB00204136.html) \ ~ 120 €

Preparación de la instalación
=============================

Antes de instalar una, estrictamente hablando, primero tendrá
VMware recuperar y poner en una llave USB.

Descargar VMware
------------------------

> ** Importante **
>
> Si pones VMware 6.5, hay un problema con la nueva gestión
> USB y Zwave clave, para que esto funcione debe aplicar esta
> [KB] (https://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=2147650)

Esto es en realidad la más difícil creo, para hacer que su vida debe
:

-   seguir
    [aquí](https://my.vmware.com/en/web/vmware/evalcenter?p=free-esxi6)
    y registrar

-   esperar a que el correo electrónico para confirmar así el registro

-   regreso
    [aquí](https://my.vmware.com/en/web/vmware/evalcenter?p=free-esxi6)
    y conectar (se pide que acepte
    condiciones deben ser validados)

-   luego ir
    [hay](https://my.vmware.com/fr/web/vmware/details?productId=491&downloadGroup=ESXI60U2)
    y añadir a la "imagen ISO ESXi (Incluye las herramientas de VMware)" su cuenta

-   finalmente volver
    [aquí](https://my.vmware.com/en/web/vmware/evalcenter?p=free-esxi6)
    y no es necesario tener en "Paquetes downlaod", el paquete "ESXi
    imagen ISO (Incluye las herramientas de VMware) "es necesario descargar

![installation.vmware.nuc](../images/installation.vmware.nuc.PNG)

Justo por encima de usted también tiene su clave de licencia, puede
tardará en recuperarse.

Descargar rufus
-----------------------

Hay mucho más sencillo solo clic
[La] (http://rufus.akeo.ie/downloads/rufus-2.9.exe). A continuación, deberá
ejecutar el .exe

Crear memoria USB de inicio
--------------------------------

De nuevo, esto es fácil es cómo establecer rufus:

![installation.vmware.nuc2](../images/installation.vmware.nuc2.PNG)

Sólo tiene que hacer clic en Inicio y esperar.

Desembalaje y montaje NUC
==============================

Estos son los tres componentes a mi NUC:

-   Intel NUC NUC6I5SYH

-   Samsung SSD 250 GB 850 EVO M.2

-   CORSARIO VENGEANCE SO-DIMM DDR4 16 GB (2 X 8 GO) CL16 2400 MHZ

![installation.vmware.nuc3](../images/installation.vmware.nuc3.jpg)

El cuadro de NUC:

![installation.vmware.nuc4](../images/installation.vmware.nuc4.jpg)

La apertura de esta:

![installation.vmware.nuc5](../images/installation.vmware.nuc5.jpg)

Los componentes de la caja:

![installation.vmware.nuc6](../images/installation.vmware.nuc6.jpg)

La apertura de la NUC, entonces es muy simple, coloque boca abajo, desenroscar
4 tornillos de terreno (que no entran en estacionaria es normal
Usted acaba de desatornillar), a continuación, tire suavemente de los tornillos para abrir
el NUC:

![installation.vmware.nuc7](../images/installation.vmware.nuc7.jpg)

SSD instalado (a la izquierda), el gato de tornillo para bloquear una
poco doloroso a mano, por suerte lo hacemos una vez

![installation.vmware.nuc8](../images/installation.vmware.nuc8.jpg)

La instalación de la memoria (a la derecha):

![installation.vmware.nuc10](../images/installation.vmware.nuc10.jpg)

Y ahora, puede cerrar (a menos que, por supuesto, que haya tomado una
2.5 SSD pulgadas necesita en este caso de inserción en la tapa).

Instalación de VMware
======================

Aquí es muy simple, sólo hay que poner el stick USB en uno de los puertos
NUC USB para conectar un monitor al puerto HDMI, un teclado y
los alimentos. Gire el NUC, la instalación se iniciará todo
solamente:

![installation.vmware.nuc11](../images/installation.vmware.nuc11.jpg)

> ** Nota **
>
> Me olvidé de tomar la validación de la licencia,
> Sólo tienes que estar de acuerdo siguiendo las instrucciones

Aquí seleccione bien el disco que corresponda a la SSD (se puede
identificado por nombre o por tamaño)

![installation.vmware.nuc13](../images/installation.vmware.nuc13.jpg)

Seleccione "francés":

![installation.vmware.nuc14](../images/installation.vmware.nuc14.jpg)

Poner una contraseña, al principio me aconsejo que poner un simple truco
como "oooo" (el cambio es a partir de entonces):

![installation.vmware.nuc15](../images/installation.vmware.nuc15.jpg)

Para confirmar, F11:

![installation.vmware.nuc16](../images/installation.vmware.nuc16.jpg)

La instalación tardará de 10 a 20 minutos, entonces debe tomar
llave USB y esperar a que el sistema se reinicie

![installation.vmware.nuc17](../images/installation.vmware.nuc17.jpg)

Una vez terminado el reinicio debe tener:

![installation.vmware.nuc18](../images/installation.vmware.nuc18.jpg)

Este VMware está instalado (es más divertido que le da su dirección IP)
simplemente jugar con !!!

Para el resto aquí es una
[Tutorial] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-vmware.creer_une_vm.html)
para la creación de su primera máquina virtual. Y encontrará
[Aquí] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-vmware.trucs_et_astuces.html)
una serie de consejos y trucos tutorial (por ejemplo, poner su licencia
VMware)
