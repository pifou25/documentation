Veremos cómo instalar Debian, así como
que VM o instalación directa en una máquina física

Conseguir las fuentes
========================

Puede encontrar las últimas Debian versión netinstall (tamaño
mínima, pero necesita internet para la instalación)
[Aquí] (https://www.debian.org/CD/netinst) (que tiene que tomar la imagen
amd64) o hacer clic directamente
[Aquí] (http://cdimage.debian.org/debian-cd/9.1.0/amd64/iso-cd/debian-9.1.0-amd64-netinst.iso)
para descargar la iso.

Inicio de la instalación
===========================

En una máquina física
------------------------

Que o bien quemar el ISO en un CD y poner el CD en la máquina
(Sin embargo, nuestros jugadores el día de CD son cada vez más raro) o de lo contrario
crear una memoria USB de inicio.

Para memoria USB de inicio debe descargar rufus
[No] (http://rufus.akeo.ie/downloads/rufus-2.9.exe), el inicio y
configure de esta manera:

![debian.installation](../images/debian.installation.PNG)

> ** Nota **
>
> Recuerde seleccionar el archivo ISO que descargó
> Justo antes

Sólo tiene que hacer clic en Inicio y, a continuación, poner el stick USB
en la máquina y para arrancarlo.

En una máquina virtual
----------

El manejo es muy sencillo, se crea una nueva máquina
virtual, la conexión, ponga una unidad de CD virtual que apunta anteriormente
a iso (Recuerde conectar) y se inicia la máquina. Ver
[Aquí] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-vmware.creer_une_vm.html)
para más detalles.

instalación
============

Pulse Intro para iniciar la instalación:

![debian.installation1](../images/debian.installation1.PNG)

Seleccione "francés" y pulsar la tecla enter

![debian.installation2](../images/debian.installation2.PNG)

Aquí hay que elegir la opción "Francés" (francés)

![debian.installation3](../images/debian.installation3.PNG)

mismo

![debian.installation4](../images/debian.installation4.PNG)

Introduzca el nombre de su máquina (nabaztag aquí, pero si es un jeedom
poner jeedom)

![debian.installation5](../images/debian.installation5.PNG)

Sólo la entrada de prensa:

![debian.installation6](../images/debian.installation6.PNG)

Poner una contraseña, yo le aconsejo que simplemente aquí (como oooo)
se puede cambiar más tarde (comando passwd):

![debian.installation7](../images/debian.installation7.PNG)

Poner de nuevo el mismo:

![debian.installation8](../images/debian.installation8.PNG)

Dar el nombre de usuario principal (nabaztag aquí, pero si se trata de una
jeedom jeedom opción de venta)

![debian.installation9](../images/debian.installation9.PNG)

Vuelva a colocar la misma cosa:

![debian.installation10](../images/debian.installation10.PNG)

Poner una contraseña, yo le aconsejo que simplemente aquí (como oooo)
se puede cambiar más tarde (comando passwd):

![debian.installation11](../images/debian.installation11.PNG)

Vuelva a colocar la misma cosa:

![debian.installation12](../images/debian.installation12.PNG)

Confirmar con entrada:

![debian.installation13](../images/debian.installation13.PNG)

mismo

![debian.installation14](../images/debian.installation14.PNG)

Una vez más confirmar con la tecla Enter:

![debian.installation15](../images/debian.installation15.PNG)

Nos sigue siendo válida:

![debian.installation16](../images/debian.installation16.PNG)

Y todavia :

![debian.installation17](../images/debian.installation17.PNG)

Elija "Francia" y validar:

![debian.installation18](../images/debian.installation18.PNG)

Confirmar con entrada:

![debian.installation19](../images/debian.installation19.PNG)

mismo

![debian.installation20](../images/debian.installation20.PNG)

Y sin embargo (sí un lote válida acerca de una instalación de Debian):

![debian.installation21](../images/debian.installation21.PNG)

Ahora más complicado, hay que anular la selección de "entorno
oficina de Debian "pulsando la tecla de espacio y seleccione" Servidor
SSH "pulsando espacio (debe moverse con la flecha
teclado), a continuación, confirmar con la tecla ENTER:

![debian.installation22](../images/debian.installation22.PNG)

Nos válida una vez más:

![debian.installation23](../images/debian.installation23.PNG)

Debemos elegir / dev / sda y validar:

![debian.installation24](../images/debian.installation24.PNG)

No sólo hay que quitar la llave USB, el CD-ROM o CD-ROM virtuales
y presione ENTRAR:

![debian.installation25](../images/debian.installation25.PNG)

Aquí se ha terminado la instalación de Debian. Puede detener el
tutorial aquí si quieres o seguir los pasos de unos pocos
cambios en el sistema (útil especialmente para jeedom).

optimización Jeedom
========================

Para preparar la instalación de Jeedom usted puede hacer algo
optimizaciones:

Añadir vim y sudo
-------------------

    sudo apt-get install sudo vim -y

Añadir fail2ban
----------------

Fail2ban es un software que permite el acceso seguro a su debian,
si demasiados fallos en la conexión bloquea el acceso a
IP en cuestión (por lo que no es para todos, sólo el atacante) una
tiempo.

    sudo apt-get install fail2ban -y

Añadir Abrir las herramientas de VMware
-----------------------------

Open las herramientas de VMware instalar controladores específicos para el sistema
Operativo instalado y proporcionar optimizaciones que SO alojado
en un hipervisor ESXi.

    sudo apt-get install -y-vm-herramientas abiertas

Sólo será instalar Jeedom siguiente
[Este] (https://jeedom.github.io/documentation/installation/fr_FR/doc-installation.html#_autre)
