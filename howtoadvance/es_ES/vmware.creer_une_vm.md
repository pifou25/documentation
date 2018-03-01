Veremos cómo crear una máquina virtual de VMware bajo.

Hay una pequeña cosa hacia adelante importante saber acerca de VMware hace 2
utilizando el administrador:

-   la interfaz web (presente de forma predeterminada en 6.0 actualización 2, o la
    a través de un Vib para otras versiones) y se accede por
    IP \ _ESXI / ui

-   pesado e histórico VMware cliente (cliente vSphere)

Aquí, he utilizado principalmente la interfaz web porque creo que es
el futuro de VMware al que deja al cliente cada vez más pesada
(Además de todos los nuevos artículos de la 5.1 no son utilizables
con el cliente pesado).

También tenga en cuenta que la interfaz web se sigue aplicando
VMware, de hecho, también se puede encontrar algunos errores o
desaceleraciones pero con un poco Scuba Review de la página y se
deja sin preocupaciones.

Inicia sesión para la interfaz web
===========================

Ir a la IP \ _ESXI / UI con su navegador web, debe tener:

![vmware.createvm3](../images/vmware.createvm3.PNG)

> **Nota**
>
> Si usted no tiene que sugeriría que hacer la instalación de
> La interfaz web, toda la información
> [Aquí] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-vmware.trucs_et_astuces.html)

Introduzca su nombre de usuario con ESXi:

![vmware.createvm4](../images/vmware.createvm4.PNG)

Como se puede ver la interfaz es bastante agradable y permite
hacer un montón de cosas, no voy a entrar en detalles pero
ya pueda de esta pantalla:

-   detener / reiniciar las ESXi

-   ver el uso de recursos (CPU, memoria y disco)

-   obtener información sobre su sistema (tiempo de funcionamiento,
    VMware versión, la versión del BIOS, almacenes de datos de visualización)

-   botón para crear una máquina virtual (lo vamos a utilizar justo después)

-   un botón de acción que permite a otro para entrar en modo de mantenimiento
    (Útil si usted tiene un grupo de ESXi Si lo hace,
    Nunca sirva), activar / desactivar el servicio SSH (utilizado
    en las copias de seguridad de configuración tutorial)

El envío de la ISO de instalación
=============================

Tras descargar la ISO de instalación
([Aquí] (http://cdimage.debian.org/debian-cd/8.5.0/amd64/iso-cd/debian-8.5.0-amd64-netinst.iso)
por ejemplo, en Debian 8.5 netinstall), hay que ponerla en
el almacén de datos.

Para ello haga clic almacén de datos:

![vmware.createvm18](../images/vmware.createvm18.PNG)

Seleccione el almacén de datos (por lo general se le llama datastore1)

![vmware.createvm19](../images/vmware.createvm19.PNG)

Haga clic en "Database Browser":

![vmware.createvm20](../images/vmware.createvm20.PNG)

Haga clic en "Download" (el primero):

![vmware.createvm21](../images/vmware.createvm21.PNG)

Seleccione previamente iso subido y validar:

![vmware.createvm22](../images/vmware.createvm22.PNG)

A continuación, puede seguir el progreso del envío:

![vmware.createvm23](../images/vmware.createvm23.PNG)

Una vez terminado se puede ver que su iso ha llegado a la
almacén de datos:

![vmware.createvm24](../images/vmware.createvm24.PNG)

Creación de la primera máquina virtual
=============================

Haga clic en "Crear / guardar una máquina virtual":

![vmware.createvm5](../images/vmware.createvm5.PNG)

Haga clic en Siguiente:

![vmware.createvm6](../images/vmware.createvm6.PNG)

A continuación, dar un nombre a su máquina y especificar su Sytem
operativo (en este caso vamos a instalar una Debian):

![vmware.createvm7](../images/vmware.createvm7.PNG)

Indicar el almacén de datos de destino:

![vmware.createvm8](../images/vmware.createvm8.PNG)

Aquí puede configurar la configuración de su máquina (disco
duro, CPU, memoria ...)

![vmware.createvm9](../images/vmware.createvm9.PNG)

> **Nota**
>
> Todos estos parámetros son modificables nota después sin preocupaciones
> De todos modos, no es realmente posible reducir el tamaño
> Una unidad de disco duro, puede ser aumentado (pero hay que gestionarla de
> Nivel continuación OS), pero no reducirlo.

En la unidad de CD / DVD, seleccione "banco archivo ISO
datos "

![vmware.createvm10](../images/vmware.createvm10.PNG)

A continuación, seleccione la ubicación donde guardó el ISO (véase
capítulo anterior) y valide:

![vmware.createvm11](../images/vmware.createvm11.PNG)

A continuación, haga lo siguiente:

![vmware.createvm12](../images/vmware.createvm12.PNG)

A continuación, tiene un resumen de la configuración, haga clic
"Terminar":

![vmware.createvm13](../images/vmware.createvm13.PNG)

Un mensaje en la parte superior le dirá que es bueno, a continuación, haga clic
"máquinas virtuales":

![vmware.createvm14](../images/vmware.createvm14.PNG)

Usted debe ver a su máquina virtual (si este no es el caso, haga clic
"Actualizar"), haga clic en:

![vmware.createvm15](../images/vmware.createvm15.PNG)

Debe tener una página como esta, haga clic en el botón Reproducir:

![vmware.createvm16](../images/vmware.createvm16.PNG)

Su máquina se inicia y será capaz de instalar
Su sistema operativo:

![vmware.createvm17](../images/vmware.createvm17.PNG)

> **Importante**
>
> Una vez que su máquina está instalada debe instalar ABSOLUTAMENTE
> herramientas de VMware (VMware que permite disponer de información sobre su VM
> Y extinguirlo correctamente). Debian sólo lo hacen
> "Sudo apt-get -y install-vm-herramientas abierta".

Para el resto de la instalación de los invito a leer este
[Tutorial] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-debian.installation.html#_installation)

Instalar los periféricos USB en la máquina virtual
=======================================

> **Nota**
>
> Si usted no tiene las opciones de abajo es que haces
> Actualizar el ESXi Embedded anfitrión al cliente, toda la información
> [Aquí] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-vmware.trucs_et_astuces.html)

Esta es una necesidad poco frecuente, pero tuve que usarlo para Jeedom en
efecto que tengo en mi llave Zwave ESXi, RFXCOM, edisio, EnOcean y GSM
moda y tuve que conectan con el fin VM Jeedom
usarlo.

> **Nota**
>
> Para Zwave, RFXCOM, edisio EnOcean y no hay preocupaciones para
> Teclas GSM que tiene que seguir
> [Tutorial] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-gsm.huawei_mode_modem.html)
> Antes de forzar la llave como un módem sólo si es
> No ver correctamente la ESXi.

Cesta de la máquina virtual y luego hacer "Cambiar la configuración":

![vmware.createvm25](../images/vmware.createvm25.PNG)

Haga clic en "Añadir otro dispositivo" y el controlador USB:

![vmware.createvm26](../images/vmware.createvm26.PNG)

> **Nota**
>
> En el siguiente paso se debe repetir para cada dispositivo USB
> Usted desea conectar

Registrar, efectúe "Cambiar configuración" y luego "Añadir otro
Dispositivo "y" dispositivo USB ":

![vmware.createvm27](../images/vmware.createvm27.PNG)

Seleccione el dispositivo USB de la lista desplegable:

![vmware.createvm28](../images/vmware.createvm28.PNG)

Y que el dispositivo esté conectado a la máquina virtual. A cada
se reiniciará automáticamente vuelto a conectar a la máquina virtual y si
sign off / conectarse físicamente a continuación, se vuelve a conectar
su VM. En otras palabras, su uso es ahora totalmente
transparente.
