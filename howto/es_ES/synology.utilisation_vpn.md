Instalar un servidor VPN
====================

Desde un navegador Web en un ordenador conectado a la misma red
Synology

Ir a la interfaz DSM y acceder con la cuenta de administrador y
vaya al menú principal y seleccione Centro de paquetes

Arriba a la izquierda en la ventana de búsqueda con la palabra VPN.
Servidor VPN debería aparecer, a continuación, haga clic en instalar.

![synology.utilisation vpn1](../images/synology.utilisation_vpn1.png)

Vuelve al menú principal y seleccionar un servidor VPN

![synology.utilisation vpn2](../images/synology.utilisation_vpn2.png)

En la apertura de la ventana, vaya a L2TP / IPSec

Seleccione la opción Habilitar servidor L2TP / IPSec VPN

En Dirección IP dinámica, introduzca un número que corresponde a la sub
la asignación de red IP de su dispositivo VPN en la red interna
usted. NB: No seleccione la misma que
Los ajustes de subred a su caja de subred ex libre de
máquinas es 192.168.1.0 por lo que en el ejemplo que pones 2

a continuación, introduzca el número máximo de conexiones que desea permitir
en el servidor VPN y el número máximo de conexiones simultáneas
para un usuario

Finalmente introducir una clave compartida Nota: esta es una contraseña que
entrará en la configuración de la VPN en el móvil o tableta.

Entonces aplique

![synology.utilisation vpn3](../images/synology.utilisation_vpn3.png)

Un mensaje indica que los puertos deben redirigirse a su
Caja de Internet a su NAS.

![synology.utilisation vpn4](../images/synology.utilisation_vpn4.png)

Permitir a los usuarios utilizar el servicio de VPN en el NAS
================================================== =============

Vuelve al menú principal y seleccionar un servidor VPN

![synology.utilisation vpn2](../images/synology.utilisation_vpn2.png)

En el privilegio de selección izquierda

Desactive todas las casillas debajo de PPTP y L2TP VPN abierto

Sólo marque la casilla al lado del usuario que desea
Permitir el uso de la VPN.

> ** Tip **
>
> Se recomienda crear un usuario sólo para VPN
> Sin otros derechos / potenciación que hacen que el VPN.

![synology.utilisation vpn5](../images/synology.utilisation_vpn5.png)

Redirigir en su caja
===============================

En el navegador de introducir 192.168.1.1. Haga clic en configuración
freebox

![synology.utilisation vpn6](../images/synology.utilisation_vpn6.png)

Seleccione el modo avanzado

![synology.utilisation vpn7](../images/synology.utilisation_vpn7.png)

Seleccione Gestión de Puertos

![synology.utilisation vpn8](../images/synology.utilisation_vpn8.png)

Añadir una redirección

![synology.utilisation vpn9](../images/synology.utilisation_vpn9.png)

Introduzca la configuración de la siguiente manera.

> ** Tip **
>
> ID de destino es el único que depende de su instalación,
> Es necesario ser el IP de su NAS de Synology

Parada

![synology.utilisation vpn10](../images/synology.utilisation_vpn10.png)

mientras que la creación Nota se tiene en cuenta

![synology.utilisation vpn11](../images/synology.utilisation_vpn11.png)

Repita el proceso con los puertos UDP 500 y 4500

Configurar la VPN en tu móvil
==================================

Ir de aplicaciones y seleccione Configuración

![synology.utilisation vpn12](../images/synology.utilisation_vpn12.png)

Haga clic en Más ...

![synology.utilisation vpn13](../images/synology.utilisation_vpn13.png)

Haga clic en VPN

![synology.utilisation vpn14](../images/synology.utilisation_vpn14.png)

Haga clic en el signo + en la parte superior derecha

![synology.utilisation vpn15](../images/synology.utilisation_vpn15.png)

Nombrando acceso VPN, como el tipo de L2TP / IPSec PSK, introduzca
megafonía de su caja de Internet (o el nombre DNS si avvez
a) e introduzca la clave compartida en la parte llena Configurar
servidor VPN:

![synology.utilisation vpn16](../images/synology.utilisation_vpn16.png)

Ahora para iniciar la VPN, simplemente haga clic en el nuevo
línea que apareció con el nombre de su túnel VPN

![synology.utilisation vpn17](../images/synology.utilisation_vpn17.png)

A continuación, introduzca el nombre de usuario y contraseña de usuario que estaba
configurado en la Parte configurar un servidor VPN

![synology.utilisation vpn18](../images/synology.utilisation_vpn18.png)

Y eso es todo lo que hacen en su teléfono es como si
Wifi que eran!
