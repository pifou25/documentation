En el 90% de los casos no es necesario forzar el modo GSM clave
Sólo GSM (en lugar de GSM + CDROM + lector de tarjetas), el único caso
en que es obligatorio es decir, si desea utilizar la clave en una
Jeedom en una máquina virtual (VMware ESXi). De hecho, si usted no va en
Sólo GSM el modo de clave no aparece en la lista de
Los dispositivos USB se puede cambiar a la máquina virtual.

> **Importante**
>
> Este tutorial ha sido realizado en un Windows 10

Instalación del controlador
========================

Una vez que la llave conectada a un PC con Windows 10 debe tener una
nueva unidad de CD-ROM. Debemos doble clic en él e instalar
software propuesto (no hay nada que cambiar después de sólo hacer todo
de largo).

![gsmonly](../images/gsmonly.PNG)

Recuperando el puerto COM
========================

Entonces tenemos que obtener el número de puerto de comunicaciones. ir a
el menú "Inicio" y busque "Administrador de dispositivos", inicio
A continuación, se desarrollan los "Puertos (COM y LPT)" que debe tener
un elemento que contiene "Huawei", el siguiente acaba de celebrar el número
puerto COM:

![gsmonly2](../images/gsmonly2.PNG)

descargar Putty
=======================

A continuación, descarga la masilla
[Aquí] (https://the.earth.li/~sgtatham/putty/latest/x86/putty.exe) y
ejecutar el archivo descargado

configuración de masilla y la conmutación al modo de sólo GSM
================================================== =====

Una vez puesto en marcha masilla configure como esto (la extinción de su número de
puerto COM que vea el paso anterior):

![gsmonly3](../images/gsmonly3.PNG)

Aparecerá una ventana en negro (que puede ser en ocasiones una
mensaje "de arranque ...", esto es normal, significa que usted está
conectado a la tecla de GSM). En esta ventana se tiene que escribir y pulse
en la tecla "Enter":

    AT ^ U2DIAG = 0

> **Importante**
>
> Tenga cuidado cuando se escribe el texto que no se va a ver nada
> La pantalla, esto es normal, el texto está siendo considerado así.

Normalmente, en cambio, usted debe tener el visto bueno.

Que todo ha terminado. Su clave está en modo GSM y sólo usted
se puede utilizar a través de un VMware ahora.
