Es importante tener copias de seguridad de su VM y esto no es un punto
sobre todo, no negligencia, por no hablar de los fallos de hardware puede
un solo día de cuerda deberá volver a una copia de seguridad debido a la incorrecta
manipulación o problema después de una actualización. La precaución es aquí
habla de cuadro completo de las máquinas virtuales, que no es sólo una aplicación de copia de seguridad,
por lo que será bastante grande.

Una limitación de copia de seguridad de VMware está teniendo
2 almacenes de datos absolutamente. Para ello tienes varias opciones:

-   2 HDD / SSD con un almacén de datos en cada

-   NAS (Synology especie) que comparte un montaje NFS. En este caso,
    debe agregar un sistema de archivos de red para VMware ve
    del mismo como un almacén de datos

Para este tutorial voy a utilizar la interfaz web del ESXi es decir
disponible ya sea mediante la instalación de un Vib ya sea desde la versión
6.0 actualización 2. Recuerde que para acceder a esta interfaz simplemente
ir a la IP \ _ESXI / ui

> **Nota**
>
> En este tutorial voy a utilizar la interfaz web del ESXi es decir
> Disponible ya sea mediante la instalación de un Vib ya sea desde el
> Actualización 6.0 2. recordatorios para acceder a esta interfaz se
> Sólo tienes que ir a IP \ _ESXI / ui

Instalación ghettoVCB
=========================

Hay que recuperar esta
[Script] (https://raw.githubusercontent.com/lamw/ghettoVCB/master/ghettoVCB.sh)
y la transferencia a la ESX (en el mismo almacén de datos que se
sede de copias de seguridad, por ejemplo).

> **Nota**
>
> En el resto de este tutorial Creo que usted ha puesto el guión
> GhettoVCB.sh en /vmfs/volumes/Backup/ghettoVCB.sh. Para adaptar
> Dependiendo de sus comandos de configuración / scripts proporcionados.

conexión SSH
================

Vas a tener que conectarse a través de SSH en ESXi, para ello tenemos que en
desde la interfaz

![vmware.backup](../images/vmware.backup.PNG)

Luego, con masilla o registro gatito en anterior con un IP
su ESXi y el uso de sus identificaciones de ella

Creación del archivo de configuración
====================================

> **Nota**
>
> Para el resto de este tutorial considero que su almacén de datos
> Copia de seguridad tiene la ruta / vmfs / Volumes / Copia de seguridad, atención a cambiar si
> Este no es el caso con usted

En la copia de seguridad del almacén de datos debe crear un archivo que ghettoVCB.conf
contiene:

    VM_BACKUP_VOLUME = / vmfs / Volumes / Copia de seguridad /
    DISK_BACKUP_FORMAT = delgada
    VM_BACKUP_ROTATION_COUNT = 2
    POWER_VM_DOWN_BEFORE_BACKUP = 0
    ENABLE_HARD_POWER_OFF = 0
    ITER_TO_WAIT_SHUTDOWN = 3
    POWER_DOWN_TIMEOUT = 5
    ENABLE_COMPRESSION = 0
    VM_SNAPSHOT_MEMORY = 0
    VM_SNAPSHOT_QUIESCE = 0
    ALLOW_VMS_WITH_SNAPSHOTS_TO_BE_BACKEDUP = 0
    ENABLE_NON_PERSISTENT_NFS = 0
    UNMOUNT_NFS = 0
    NFS_SERVER = 172.30.0.195
    Nfs_mount = / nfsshare
    NFS_LOCAL_NAME = nfs_storage_backup
    NFS_VM_BACKUP_DIR = MyBackups
    SNAPSHOT_TIMEOUT = 15
    EMAIL_LOG = 0
    EMAIL_SERVER = auroa.primp-industries.com
    EMAIL_SERVER_PORT = 25
    EMAIL_DELAY_INTERVAL = 1
    EMAIL_TO=auroa@primp-industries.com
    Email_from = root @ ghettoVCB
    WORKDIR_DEBUG = 0
    VM_SHUTDOWN_ORDER =
    VM_STARTUP_ORDER =

Los parámetros que debe ajustar son los siguientes:

-   **VM \ _BACKUP \ _VOLUME** ⇒ ubicación de su almacén de datos de copia de seguridad

-   **VM \ _BACKUP \ _rotation \ _count** ⇒ número de copia de seguridad por máquina virtual para mantener

> **Nota**
>
> Puede comprobar
> [Aquí] Documentación (https://communities.vmware.com/docs/DOC-8760)
> GhettoVCB completa con una descripción de cada opción

> **Importante**
>
> Tenga cuidado de poner la final / para el parámetro
> VM \ _BACKUP \ _VOLUME de lo contrario el script error

copia de seguridad de prueba
==============

Aquí, vamos a poner en marcha una primera copia de seguridad inicial de todas las máquinas virtuales para
ver si todo está bien. A partir de entonces vamos a planificar de forma automática.
Retorno de la ESXi (SSH reconectarse si es necesario) y ejecute:

    /vmfs/volumes/Backup/ghettoVCB.sh -a -g /vmfs/volumes/Backup/ghettoVCB.conf

Esto abrirá una copia de seguridad de todas sus máquinas virtuales (y puede tomar bastante
de tiempo). Al final se debe tener en su copia de seguridad de un almacén de datos
por carpeta de máquina virtual y cada subcarpeta carpeta VM por fecha
4 archivos que contienen:

![vmware.backup2](../images/vmware.backup2.PNG)

-   \ * - flat.vmdk ⇒ el disco virtual en su máquina

-   \ *. Vmdk ⇒ el descriptor del disco

-   \ *. Vmx ⇒ el archivo que contiene la configuración de la máquina

-   STATUS.ok ⇒ indica que la copia de seguridad está bien

Aquí hay otra opción para la línea de comandos:

-   simulación de copia de seguridad:

<! - ->

    /vmfs/volumes/Backup/ghettoVCB.sh dryrun -d -a -g /vmfs/volumes/Backup/ghettoVCB.conf

-   Lanzamiento en modo de depuración:

<! - ->

    /vmfs/volumes/Backup/ghettoVCB.sh -d -a debug -g /vmfs/volumes/Backup/ghettoVCB.conf

-   Sólo copia de seguridad "foo" VM

<! - ->

    /vmfs/volumes/Backup/ghettoVCB.sh -a -m -g foo /vmfs/volumes/Backup/ghettoVCB.conf

copias de seguridad automáticas de lanzamiento
=================================

Hay que añadir la línea de comandos para el crontab pero el VMware
crontab es un poco especial, sobre todo aplastado en cada arranque. Para
evitar esto por lo que añadir un pequeño script que actualizará la
crontab en el arranque (no se preocupe esto es bastante simple y rápido), en
SSH en el ESXi a:

    vi /etc/rc.local.d/local.sh

Y antes de que el "exit 0" añadir las siguientes líneas:

    / Bin / kill $ (/var/run/crond.pid gato)
    / Bin / echo "0 0 1 * * /vmfs/volumes/Backup/ghettoVCB.sh -a -g /vmfs/volumes/Backup/ghettoVCB.conf> / dev / null 2> & 1" >> / var / spool / cron / crontabs / root
    / Usr / lib / vmware / busybox / bin / crond busybox

> **Nota**
>
> Aquí solicito una copia de seguridad cada primero de mes, puede cambiar
> Esta modificando: 0 0 1 \ * \ *

> **Nota**
>
> Aquí hago una copia de seguridad de todas las máquinas virtuales, se puede incorporar en
> Sustitución de la -a con mi -m \ _vm, tenga cuidado si quieres
> Varias máquinas virtuales debe duplicar la línea "/ bin / echo" 0 0 1 \ * \ *
> /vmfs/volumes/Backup/ghettoVCB.sh -a -g
> /vmfs/volumes/Backup/ghettoVCB.conf &gt; / dev / null 2&gt; & 1 "&gt;&gt;
> / Var / spool / cron / crontabs / root "y poner una máquina virtual por Backuper

> **Importante**
>
> Asegúrese de ajustar la ruta de acceso al archivo de configuración
> GhettoVCB dependiendo de su configuración:
> /vmfs/volumes/Backup/ghettoVCB.conf

El último paso: debe reiniciar el ESXi para que se tome la cron
cuenta, se puede ver el resultado por (siempre SSH):

    cat / var / spool / cron / crontabs / root

Aquí hay que tener una línea:

    0 0 1 * * /vmfs/volumes/Backup/ghettoVCB.sh -a -g /vmfs/volumes/Backup/ghettoVCB.conf> / dev / null 2> & 1
