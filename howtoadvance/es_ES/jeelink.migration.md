Vamos a ver aquí cómo migrar una instalación con el modo Jeedom
esclavo a un Jeedom con el plugin "Jeedom Enlace". modo esclavo
Jeedom siendo abandonado, de paso, Jeedom a la versión 3.0, es
necesaria antes de la migración a la nueva moda
operación.

Preparación antes de la migración
===========================

> **Aviso**
>
> Es importante leer toda esta documentación antes
> Comienza la migración. información importante
> Actualizar requisitos previos, backup y recuperación
> Información son esenciales para la comprensión de
> La operación se lleve a cabo. Se abstengan de leer esta documentación puede
> Conducir a operaciones destructivas sobre su instalación. Si usted
> No entiendo un punto, no dude en preguntar acerca de la
> Foro antes de iniciar el procedimiento!

> **Importante**
>
> Tenga cuidado de no equipos de bucle
> Configuración del complemento "Jeedom Enlace". Por ejemplo, no hacer una
> Equipo-X en una Jeedom1 volver en un Jeedom2 luego hacia arriba
> Una vez más en el Jeedom1. Esto podría provocar la caída de sus Jeedoms!

> **Nota**
>
> Para facilitar la lectura y comprensión de este tutorial, aquí están
> Términos utilizados: \
> \
> - ** ** Jeedom Objetivo: Servidor (su edad Jeedom Maestro) que
> Centraliza equipos / **de Jeedom (s) fuente (s)** \
> Las capturas de pantalla sobre fondo negro coinciden con el Jeedom ** ** Meta. \
> \
> - Jeedom ** ** Fuente: Servidor (tu / su ex (s) Jeedom Esclavo (s))
> Volviendo en su equipo ** ** Jeedom destino. \
> \
> - Los conceptos de Jeedom Maestro ****** ** y Jeedom esclavo ya no están
> Tópica. El nuevo modo de funcionamiento de sincronización
> Equipo de entre varios Jeedoms puede ser bidireccional. una
> Servidor Jeedom ahora puede ser **Fuente de destino****** y mientras
> La vieja manera no permitió el aumento de equipos
> **** esclavo a maestro** **. Con el nuevo método es también
> Posible tener varios objetivos Jeedom ****** para el mismo Jeedom
> ** Fuente. La comunicación entre Jeedoms Ahora también puede
> Hacer de forma remota a través de Internet (DNS Jeedom o de otro tipo). \
> \

![jeelink.migration9](../images/jeelink.migration9.png)

Las actualizaciones y verificación de la configuración
------------------------------------------------

-   **Actualización** Jeedom Maestro a la última versión (incluso si
    ninguna actualización se le ofrece a usted).

-   Actualizar plugins ** ** el último Maestro Jeedom
    versiones disponibles.

-   Compruebe la página de la Salud que la configuración de la red interna
    **** Jeedom del Maestro OK (Y si sus Jeedoms externos** ** Fuentes
    ser a distancia).

Rally Información útil
-------------------------------------

Dependiendo de sus plugins instalados ** ** Jeedom esclavo, es
necesarias para recuperar la siguiente información:

### Zwave Plugin

-   En la página del plugin Zwave la salud en Jeedom ** ** master, seleccione
    ** ** su esclavo en el menú y hacer una captura de pantalla,
    con el fin de tener una lista de los equipos que vienen
    de este.

-   Nota para cada dispositivo del Esclavo ** **: el objeto
    padre de familia, nombre, ID (nodo) del modelo.

-   Obtener el archivo Zwcfg: * Plugins Plugins Gestión ⇒ ⇒
    Z-Wave *. Haga clic en el botón rojo * * Zwcfg y copiar el
    en un archivo de texto en el ordenador.

### RFXCOM Plugin

-   Nota para cada dispositivo del Esclavo ** **: el objeto
    padre de familia, nombre, ID (lógica), el tipo, modelo.

> **Nota**
>
> Una información incompleta perfil nota para la migración
> Está disponible [aquí] (../ images / MemoMigration.xls)

copias de seguridad preventivas
-----------------------

-   Hacer [Copia de seguridad
    Jeedom] (https://jeedom.github.io/documentation/core/fr_FR/doc-core-backup.html)
    **** Jeedom su Maestro y su (su)** Jeedom Esclavo (s) **
    y elegir la (s) -alquilo en su PC / NAS ....

-   Hacer [Copia de seguridad
    SD / disco] (https://jeedom.github.io/documentation/howto/fr_FR/doc-howto-sauvegarde.comment_faire.html#_sauvegarde_restauration_de_la_carte_microsd)
    **** Jeedom su Maestro y su (su)** Jeedom Esclavo (s) **
    y recuperar su PC / NAS ....

migración
=========

> **Nota**
>
> No retire por ahora el equipo viejo
> ****** en el Maestro Esclavo **.

Instalar y activar el plugin "Jeedom Enlace" en la Jeedom Target ** ** (antiguo maestro).
-------------------------------------------------- -----------------------------------

En su Jeedom Target ** ** * * Plugins gestión ⇒ Plugin:

![jeelink.migration1](../images/jeelink.migration1.png)

Jeedom instalación ** ** Fuente:
-----------------------------------

> **Nota**
>
> Si usted tiene un Frambuesa Pi y se agrega otra tarjeta
> SD, puede realizar un protocolo de migración tras otro
> La instalación de nuevo Jeedom ** ** Fuente en paralelo sin
> Toque su existente ** ** Jeedom esclavo. obviamente se mueve
> El Como cualquiera de los controladores entre sí.

> **Aviso**
>
> Si usted utiliza su existente Frambuesa Pi, por favor asegúrese
> Han seguido capítulo copia de seguridad de esta documentación.

> **Nota**
>
> Si utiliza la Frambuesa Pi existente actualmente una
> ** ** Jeedom Esclavo, se recomienda utilizar una tarjeta
> SD / microSD nueva. Esto le permitirá volver al estado anterior
> Fácilmente si es necesario.

-   Instalar un nuevo Jeedom en una tarjeta SD (si
    para poner en su Jeedom ** ** esclavo existente o una
    nueva Frambuesa Pi) después de la [Documentación
    Instalación] (https://jeedom.github.io/documentation/installation/fr_FR/doc-installation.html).

-   Actualización ** ** Fuente Jeedom a la última versión (incluso si
    ninguna actualización se le ofrece a usted).

-   Compruebe la página de la Salud que la configuración de la red interna (y
    externa si es necesario) de Jeedom ** ** Fuente está bien.

Configuración de origen Jeedom
------------------------------

-   Cambiar la contraseña del usuario administrador y / o configurar una
    nuevo usuario.

-   Configurar su cuenta Jeedom Mercado (* ⇒ actualizaciones de configuración
    ⇒ archivos y "Mercado" * tab). Haga clic en la prueba después de
    salvado, para confirmar la entrada de su contraseña
    Mercado Jeedom).

-   La instalación y la activación del complemento "Jeedom Enlace" en el nuevo
    ** ** Fuente Jeedom.

![jeelink.migration2](../images/jeelink.migration2.png)

-   Instalación y activación de los plugins que desea utilizar.
    (Se recomienda hacer uno por uno, comprobando cada pocillo
    Una vez que las dependencias y los demonios están bien).

-   Recreando el árbol de objetos (lo que eres
    ser útil) de Jeedom ** ** Meta (Viejo Maestro) a su nueva
    Jeedom ** ** Fuente (Old Slave).

configuración del equipo en el Jeedom ** ** Fuente
-------------------------------------------------- ----

Para proceder a enviar un equipo presente en el Jeedom ** ** Fuente
a Target ** ** Jeedom a través del plug-in "Jeedom Enlace", es necesario
este último ya se está ejecutando en su nuevo ** Jeedom
** Fuente.

> **Nota**
>
> Piense progresivamente incapacitante órdenes de archivado
> Información de cada dispositivo que se encuentra en la Fuente para Jeedom ** **
> Guardar la tarjeta SD de él (El archivo se hará sobre la
> ** ** Jeedom Target).

> **Nota**
>
> También puede asignar progresivamente a equipos
> Recreated objetos en el ** ** Fuente Jeedom para que más tarde
> Automáticamente en el objeto a la derecha en la Jeedom ** ** Meta en
> Declaración en el plugin "Jeedom Enlace". Si el nombre duplicado
> Con el equipo ya presente en los objetos de Jeedom Target ** **
> Plugin añadirá "XXXX remoto" en el nombre del equipo.

### Zwave plugin:

-   Haga clic en el botón "Sync" para recuperar los módulos
    asociado con el controlador. (Se mantienen en la memoria
    de este)

-   Reemplazar Zwcfg * * Archivo: * Plugins Plugins Gestión ⇒ ⇒
    Z-Wave *. Haga clic en el botón rojo * * Zwcfg y pegar el contenido de
    archivo de texto creado previamente en el ordenador. * Guardar
    los cambios*.

-   Cambiar el nombre de sus módulos y colocarlos en los objetos deseados en usted
    ayudando a su memo de la migración.

### RFXCOM plugin:

#### Sondas, sensores, detectores, ...:

-   Coloque la inclusión modo de complemento.

-   Repita hasta que la inclusión de todos sus equipos
    este tipo.

-   Cambiar el nombre de su equipo y colocarlos en los objetos deseados
    ayudarle en su nota de migración.

#### Actuadores tomadas .... :

-   Añadir nuevos equipos.

-   Establecer el nombre, el ID, el objeto primario, el tipo de equipo y
    modelo en el que le ayuda en su nota de migración.

-   Repita este procedimiento para todos los equipos de este tipo.

configuración del plugin "Jeedom Enlace"
-------------------------------------

El plug-in "Jeedom Enlace", instalada en el ** ** Fuente Jeedom permite
Equipo de ascensores en el Jeedom ** ** Meta (Su antiguo maestro).

> **Nota**
>
> Recordemos, para una mejor lectura y comprensión de este tutorial: \
> \
> Las capturas de pantalla sobre fondo negro coinciden con el Jeedom ** ** Meta. \
> \
> Las capturas de pantalla en el fondo blanco coincide con la Jeedom ** ** Fuente. \

Por Jeedom ** ** Fuente,
[Set] (https://jeedom.github.io/documentation/plugins/jeelink/fr_FR/jeelink)
el plug-in "Jeedom Enlace" especificando:

-   El nombre de la Jeedom Target ** **.

-   La dirección IP o el nombre DNS del Jeedom Target ** **.

-   La clave de API ** ** Jeedom destino.

Y guardar la configuración.

![jeelink.migration3](../images/jeelink.migration3.png)

En * * pestaña Asignación, agregue el equipo que desea
de nuevo a Jeedom ** ** Meta.

![jeelink.migration4](../images/jeelink.migration4.png)

* Haga clic en Agregar dispositivo * Seleccione el objeto y equipos
añadiendo:

![jeelink.migration5](../images/jeelink.migration5.png)

Después de actualizar la página * * Mis JeeLinks ** ** Meta de Jeedom se
debería ver la creación automática de los equipos:

![jeelink.migration6](../images/jeelink.migration6.png)

Al igual que cualquier equipo Jeedom, se puede encender / apagar y visualización
o no el equipo, sus controles ... o cambiar la categoría:

![jeelink.migration7](../images/jeelink.migration7.png)

* * En la ficha Comandos, el acceso a todos los parámetros
controles del equipo:

![jeelink.migration8](../images/jeelink.migration8.png)

La recuperación del histórico
----------------------------

> **Nota**
>
> A al destino ** ** Jeedom (Viejo Maestro) para cada orden
> Equipo de Información del viejo esclavo ** ** el cual queremos recuperar
> Historia.

-   Ir en la configuración de comandos (* rueda dentada a
    derecha*).

-   Ir a la pestaña * * Configuración avanzada.

-   Haga clic en el botón Copiar * la historia de este comando en una
    Otra orden *.

-   Encontrar el correspondiente equipo nuevo orden JeeLink
    corresponsal y confirme.

Sustitución de equipos antiguos esclavos en los escenarios / virtual / ...
-------------------------------------------------- --------------------------

> **Nota**
>
> A al destino ** ** Jeedom (Viejo Maestro) para cada orden
> Información / acción de los equipos de la antigua Esclavo ** ** el que queremos
> Reemplazar apariciones en los escenarios / virtual / ....

-   Ir en la configuración de comandos (* rueda dentada a
    derecha*).

-   * * Ir a la ficha Información.

-   Haga clic en el botón * Reemplazar este comando por el *.

-   Encontrar el correspondiente equipo nuevo orden JeeLink
    corresponsal y confirme.

Recuperación de las configuraciones de visualización avanzada órdenes
-------------------------------------------------- ----------------

> **Nota**
>
> A al destino ** ** Jeedom (Viejo Maestro) para cada orden
> Información / acción de los equipos de la antigua Esclavo ** ** el que queremos
> Recuperar la configuración de visualización avanzadas.

-   Ir en la configuración de comandos (* rueda dentada a
    derecha*).

-   Haga clic en el botón para aplicar * *.

-   Buscar y seleccionar el comando correspondiente de la nueva
    JeeLink equipo y confirmar correspondiente.

Reflejando los controles de configuración avanzada
-------------------------------------------------

> **Nota**
>
> A al destino ** ** Jeedom (Viejo Maestro) para cada orden
> Información / acción de los equipos de la antigua Esclavo ** ** el que queremos
> Recuperar la configuración avanzada.

-   Hay una solución fácil a este nivel, tendrá dos
    pestañas / ventanas abiertas en su navegador.

-   órdenes abiertas de equipos del viejo esclavo ** ** una
    pestaña (Jeedom Target).

-   Abrir órdenes de equipo jeeLink en la otra pestaña
    (Jeedom Target).

-   Y copiar manualmente los ajustes deseados.

> **Nota**
>
> Para evitar volver varias veces en el mismo orden,
> → operaciones 2.6 2.9 se pueden realizar como resultado de la misma
> Solicitar antes de pasar al siguiente.

> **Aviso**
>
> Interacciones en Jeedom ** ** objetivo no puede ser lanzado
> A través de instalaciones de un Jeedom ** ** Fuente través tranférés
> Plugin "Jeedom Enlace".

Limpieza del objetivo ** ** Jeedom
==============================

> **Nota**
>
> Después de confirmar con certeza que su
> Equipo / escenarios / interacciones / virtual / .... función
> Correctamente con el nuevo sistema jeelink, se puede proceder a
> Hogar.

-   Eliminar el equipo restante de la primera Jeedom esclavo ** **.

-   Desactivar y retirar plugins que ya no son útiles
    (A los que tenías único equipo en el esclavo).

-   En el plug-in "Jeedom Enlace", cambiar el nombre de equipo
    podría tener un nombre que termina con "XXXX remota".

-   En la Red de Jeedom, eliminar el antiguo esclavo Jeedom ** **.


