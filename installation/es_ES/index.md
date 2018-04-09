hardware
========

Jeedom se puede instalar en varios componentes de hardware:

-   un ft frambuesa 2 o 3

-   Synology NAS

-   cualquier sistema Linux basado en Debian

También puede comprar una caja confeccionada con Jeedom preinstalado
que adicionalmente contiene un paquete de servicio (más apoyo y servicios)
plugins disponibles de:

-   [Inteligente Jeedom
    Z-Wave +](https://www.domadoo.fr/fr/box-domotique/3959-jeedom-controleur-domotique-jeedom-smart-z-wave.html)

-   [Jeedom Smart + y Z-Wave
    RFXCOM](https://www.domadoo.fr/fr/box-domotique/4043-jeedom-controleur-domotique-jeedom-smart-z-wave-et-interface-rfxcom.html)

-   [Inteligente Jeedom
    EnOcean](https://www.domadoo.fr/fr/box-domotique/4041-jeedom-controleur-domotique-jeedom-smart-enocean.html)

-   [Jeedom y EnOcean inteligente
    RFXCOM](https://www.domadoo.fr/fr/box-domotique/4044-jeedom-controleur-domotique-jeedom-smart-enocean-et-interface-rfxcom.html)

Aquí es una configuración de "tipo" para un buen comienzo con Jeedom Z-Wave:

1.  Pi frambuesa 3:

    -   Una caja de frambuesa + \ ~ 50 €

    -   Una clave Aeon Gen 5 \ ~ 60 €

    -   Una tarjeta micro SD \ ~ 7 €

    -   Un USB de potencia \ ~ € 8

Un total de € 125 para una caja con domótica de código abierto
el control completo de su instalación.

> **Tip**
>
> Es posible añadir o cambiar una antena RFXCOM, o
> Clave EnOcean.

> **Tip**
>
> Jeedom es un software que es y seguirá siendo de código abierto, su uso
> Es completamente gratuito y no depende de una nube o
> Suscripción. Sin embargo, algunos plugins que aumentan la
> Capacidad de Jeedom o su uso puede ser gravosos y **
> Es posible que tenga una conexión a Internet **. Puede encontrar
> La lista de plugins
> [Aquí](http://market.jeedom.fr/index.php?v=d&p=market&type=plugin).

> **Tip**
>
> Service Pack? Quézako? Podéis ver
> [Aquí](https://blog.jeedom.fr/?p=1215) los beneficios de los paquetes de servicio.


Jeedomboard
===========

Aquí se encuentra el paso a paso la documentación para instalar en Jeedom
la Jeedomboard (o Hummingboard).

> **Tip**
>
> El nombre de la imagen Jeedom puede ser diferente de la captura
> Hecho en esta documentación

Paso 1: Instalar Etcher
---

Debe descargar el Etcher logicel [aquí] (https://etcher.io/), entonces
instalarlo en su PC

Paso 2: Recuperación Jeedom Imagen
---

Tiene que ir
[Aquí](https://www.amazon.fr/clouddrive/share/OwYXPEKiIMdsGhkFeI3eUQ0VcvTEBq0qxQevlXPvPIy/folder/IT3WZ3N0RqGzaLBnBo0qog)
a continuación, en la carpeta Imágenes recuperar la imagen jeedom-jeeboard - \ *. rar o
Jeedomboard \ _ \ _ Debian \ _Jessie \ *. Rar

![install humming 1](../images/install_humming_1.PNG)

Paso 3: Descompresión imagen Jeedom
---

Décompresser l’image de Jeedom (si vous n’avez rien pour la décompresser
vous pouvez installer
[winrar](http://www.clubic.com/telecharger-fiche9632-winrar.html)), vous
devez obtenir :

![install humming 2](../images/install_humming_2.PNG)

![install humming 8](../images/install_humming_8.PNG)

Paso 4: La quema de la imagen en la tarjeta SD
---

Insérez votre carte SD dans votre ordinateur puis lancez le logiciel
Etcher, donnez-lui le chemin de l’image, le chemin de la carte SD et
cliquez sur "Flash!". Le logiciel va graver la carte SD et vérifier la
gravure.

Sólo hay que poner la tarjeta SD en la Jeedomboard (o
Hummingboard) para conectar la red y la potencia, su voluntad Jeedom
empezar (5 min) y debería ver en la red.

> **Tip**
>
> identificadores SSH son jeedom / Mjeedom96

Pour la suite, vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index.html)

Miniplus / Hummingboard
=====================

Aquí se encuentra el paso a paso la documentación para instalar en Jeedom
Mini más (mapa Hummingboard Solid-Run).

![jeedom](../images/jeedom.jpg)

Paso 1: Instalar Etcher
---

Debe descargar el Etcher logicel [aquí] (https://etcher.io/), entonces
instalarlo en su PC

Paso 2:
---

Récupération de l’image Jessie. Attention la humingboard n’est pas
un raspberry. **Vous devez impérativement récupérer cet iso spécifique
qui est une jessie pour IMX6.**

Tiene que ir
[Aquí](https://images.solid-build.xyz/IMX6/Debian/sr-imx6-debian-jessie-cli-20171108.img.xz)
y guardar la imagen en su PC.

Paso 3: La descompresión de la imagen
---

Décompresser l’image de Jeedom (si vous n’avez rien pour la décompresser,
vous pouvez installer
[winrar](http://www.clubic.com/telecharger-fiche9632-winrar.html)).

Paso 4: La quema de la imagen en la tarjeta SD
---

Insérer votre carte SD dans votre ordinateur puis lancer le logiciel
Etcher, donnez-lui le chemin de l’image, le chemin de la carte SD et
cliquez sur "Flash!". Le logiciel va graver la carte SD et vérifier la
gravure.

Sólo hay que poner la tarjeta SD en el Mini + para conectar el
la red y la potencia, su Jeedom se iniciará.

Paso 5: Instalar jeedom - Guión lanzamiento
---

Abra una consola SSH con masilla por exemmple.

> **Tip**
>
> Debian de usuario / contraseña debian

> **Tip**
>
> La contraseña de root es debian

1 / Configuración de intercambio el Mini + como inactiva por defecto con este
distribución.

Conectar con SSH a su sistema y hacer:

    sudo imx6-config

Introduzca la contraseña de root ( "debian")

Haga clic en OK (aparece su IP local - la nota a continuación para conectarse a
el fin)

pulse Intro

Elige la categoría 4 de intercambio con las teclas de flecha y luego intall
Se recomienda de intercambio (SWAP un 512, se puede cambiar al final de
crear el canje por defecto). Siga el procedimiento.

**Reiniciar** y comprobar la activación del intercambio con el comando

    reinicio sudo

    gratis - m

2 / Finalmente inicie la escritura oficial con estos tres comandos:

    wget https://raw.githubusercontent.com/jeedom/core/stable/install/install.sh

    chmod + x install.sh

    sudo ./install.sh

**La durée d’installation varie de 60 à 120 minutes**. Vous ne devez pas
interrompre cette procédure. A défaut il faut tout reprendre. Il est
vivement conseillé de rebooter à la fin de l’installation.

Los siguientes argumentos pueden ser utilizados:

-w fichero = servidor web

dependencias z = sistema de onda z

-m = raíz contraseña de MySQL requiere

    ./install.sh -w / var / www / html z -m Jeedom

Es recomendable hacer un reinicio de la mini +

    reinicio sudo

Después, simplemente ir a IP \ _MACHINE \ _JEEDOM en su
navegador.

> **Nota**
>
> La contraseña por defecto es admin / admin

> **Importante**
>
> Si necesita inyectar una copia de seguridad, usted tiene que esperar entre 5 y 10
> minutos para conseguir todo en orden (el usuario admin /
> Administración ya no existe ...). Especialmente tienes que no fuera
> Eléctricamente su mini más.

Para el resto se puede seguir la documentación [Introducción a
Jeedom](https://www.jeedom.fr/doc/documentation/premiers-pas/fr_FR/doc-premiers-pas.html)

frambuesa Pi
===========

Aquí encontrará la documentación de la instalación de un Jeedom
PI frambuesa **con una tarjeta SD.**

> **Important**
>
> Debian 9 (Stretch) est la distribution officiellement supportée pour
> la version 3.1.5 de jeedom (mais Jessie reste parfaitement
> fonctionnelle).

**1 / Descarga la última foto "light", es decir, sin interfaz
gráfico**
[Aquí](https://downloads.raspberrypi.org/raspbian_lite/images/raspbian_lite-2017-12-01/2017-11-29-raspbian-stretch-lite.zip)

**2 / descomprimir la imagen con winrar** [Aquí](http://www.win-rar.com)

**3/ Gravez cette image sur une SD avec etcher par exemple**
[ici](https://etcher.io/)

> **Nota**
>
> Si utiliza Etcher para quemar su imagen, la etapa
> La descompresión se innecesarias (reconocida directamente en formato Zip
> Seleccione el archivo de imagen).

**4 / Habilitar el acceso SSH**

> **Aviso**
>
> Por razones de seguridad, el acceso SSH no está activado por defecto
> Esta distribución. así que hay que activarlo.

Hay que crear la partición de arranque (la única disponible en Windows)
ssh un archivo vacío.

clic justo: nueva / texto y
cambiar el nombre de "ssh" ** ** sin extensión

> **Importante**
>
> En Windows, en el Explorador de fin de comprobar su
> Configuración de visualización / Opciones / Opciones de cambio
> Carpeta y Búsqueda /

![ExtensionFichier](../images/ExtensionFichier.PNG)

**5 / IP de inicio**

Insérez votre carte SD, branchez le cable réseau, branchez
l’alimentation.

**6 / sesión SSH**

Identifiez votre Pi sur le réseau

Il faut connaître l’adresse Ip de votre PI. Plusieurs solutions :

-   Consultez la configuration DHCP dans votre routeur

-   Utilisez un scanner de port type "angyipscanner"
    [aquí](http://angryip.org/download/#windows)

establecer la conexión

Ensuite utilisez par exemple putty pour établir votre connexion
[Ici](http://www.putty.org/)

Retraer la dirección IP de su IP (192.168.0.10 aquí) y haga clic
abierta. Aceptar el mensaje predeterminado por la seguridad en el
primera conexión.

ID de sesión con **pies / frambuesa**

> **Importante**
>
> Por razones de seguridad, es imprescindible para cambiar la contraseña
> Predeterminados. Los casos de piratería basan en la explotación de
> Inicio de sesión / contraseña por defecto son frambuesa
> Particularmente frecuente. (Passwd y sudo passwd)

**7 / Iniciar el jeedom script de instalación**

    wget -O https://raw.githubusercontent.com/jeedom/core/stable/install/install.sh | fiesta sudo

**La contraseña sudo es frambuesa**

> **Nota**
>
> Dependiendo de su velocidad de Internet, la instalación puede tardar 45
> 90 minutos. Usted Particularmente, no debe interrumpir el proceso antes
> El final. De lo contrario, se repetirá el procedimiento completo.

Después, simplemente ir a IP \ _MACHINE \ _JEEDOM

> **Nota**
>
> La contraseña por defecto es admin / admin

> **Nota**
>
> Los siguientes argumentos pueden ser utilizados: w = z = archivo de servidor web
> -m dependencias de instalación de onda z = contraseña root mysql deseada

    ./install.sh -w / var / www / html z -m Jeedom

**8/ Optimisation système

Si vous utilisez votre Raspberry pour Jeedom sans écran connecté, il est recommandé d'effectuer le minimum de RAM à la partie vidéo.

Il suffit de se connecter en **SSH** et de modifier le fichier config : `sudo nano /boot/config.txt`

Ajoutez **et/ou**De-commentez (en supprimant le #)**et/ou** Modifiez les lignes : 

`gpu_mem=16`

`disable_l2cache=0`

`gpu_freq=250`

Quittez en sauvegardant : `CTRL+X` puis `O `puis `ENTREE`

Rebootez votre RPI

Ensuite, vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index)

VM
==

Si vous voulez découvrir Jeedom sans risque, vous pouvez aussi le
virtualiser sur votre PC, voici la démarche à suivre. Vous ne prenez
aucun risque dans une VM, l’intégrité de votre Pc est protégé :

Etape 1 : Téléchargement et installation de VMware Player 
---

Vous devez télécharger le logicel Virtual Box
[ICI](http://download.virtualbox.org/virtualbox/5.1.28/VirtualBox-5.1.28-117968-Win.exe)

Etape 2 : Téléchargement d’une image Debian strecht - netinstall 
---

Téléchargez une image minimaliste debian 9 Stretch
[Ici](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-9.3.0-amd64-netinst.iso)

Téléchargez le pack d’extensions, et installez-le.
[ICI](http://download.virtualbox.org/virtualbox/5.1.28/Oracle_VM_VirtualBox_Extension_Pack-5.1.28.vbox-extpack)

Etape 3 : Configuration de l’environnement de la VM 
---

Cliquez sur nouvelle et renseignez les champs comme ci dessous :

![VirtualBox1](../images/VirtualBox1.PNG)

-   Cliquez sur suivant, adapter la taille de la mémoire par rapport à
    votre système (1024 sont suffisants)

-   Cliquez sur suivant, créer un disque virtuel maintenant

-   Cliquez sur Créer, choisissez VDI

-   Cliquez sur suivant, dynamiquement alloué

-   Cliquez sur suivant, Choisissez une taille pour l’espace
    (4Go suffisent)

-   Cliquez sur créer

Etape 4 : Lancement de la VM 
---

-   Cliquez sur configuration

-   Sélectionnez stockage

-   Ajoutez un lecteur optique

-   Choisissez un disque

![VirtualBox2](../images/VirtualBox2.PNG)

-   Indiquez l’image précédemment téléchargée

-   Sélectionnez ensuite réseau et choisissez "accès par pont" dans le mode
    d’accès réseau.

![VirtualBox3](../images/VirtualBox3.PNG)

-   Cliquez sur OK \*Cliquez sur démarrer

Etape 5 : Installation de debian 9 
---

C’est du classique …​

![VirtualBox4](../images/VirtualBox4.PNG)

-   Choisissez Graphical install

-   Installez la debian de préférence sans interface graphique
    car inutile. Le nom d’utilisateur n’a aucune importance. Dans la
    plupart des écrans, il suffit de valider le choix par défaut. Vous
    pouvez laissez des champs vides, ce n’est pas bloquant.

-   Pour la sélection des logiciels :

![VirtualBox5](../images/VirtualBox5.PNG)

-   Pour Grub, pas d’inquiétude, le secteur de démarrage est celui de la
    VM, pas celui de votre PC. Aucun risque de casser quoi que ce soit.

Etape 6 : Installation de jeedom 
---

-   Lancez votre VM

-   Identifiez-vous avec l’utilisateur et le mot de passe choisis
    pendant l’installation

-   Passez en root

<! - ->

    su

-   Saisissez le mot de passe root défini pendant l’installation

-   Récupérez le script jeedom, le rendre exécutable, le lancer

<!-- -->

    wget https://raw.githubusercontent.com/jeedom/core/stable/install/install.sh

    chmod +x install.sh

    ./install.sh

-   et laissez faire…​

Etape 7 : Lancement de jeedom 
---

-   Pour connaitre l’adresse Ip Lan de la VM

<!-- -->

    ip -s -c -h a

Votre adresse Ip, type 192.168.0.XX apparait en rouge. Il vous suffit de
la saisir dans votre navigateur.

> **Warning**
>
> Si cela ne fonctionne pas, vous n’avez pas configuré votre carte
> réseau en Pont réseau comme indiquée au départ.

Ensuite, vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index)

Docker
======

> **Important**
>
> Attention, nous partons ici du principe que vous maîtrisez déjà Docker

Pour découvrir Jeedom, vous pouvez aussi le faire tourner dans un
conteneur Docker :


Etape 1 : Installation de docker 
---

Docker est maintenant disponible sur toutes les distributions récentes.
Pour l’installer sur une distribution

-   à base de rpm

<!-- -->

    $ yum install docker

-   à base de deb

<!-- -->

    $ apt-get update
    $ apt-get install docker
    $ apt-get install docker.io

Etape 2 : Installation d’une image mysql 
---

> **Note**
>
> Vous pouvez aussi installer mysql directement sur la machine hôte,
> dans ce cas, il faut sauter cette étape.

J’utilise [celle-ci](https://hub.docker.com/_/mysql/). Pour l’installer
:

    docker pull mysql:latest

Puis la lancer :

    sudo docker run --name jeedom-mysql -v /opt/jeedom/mysql:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=your-mysql-password -d mysql:latest

Avec :

-   jeedom-mysql : le nom du conteneur mysql

-   /opt/jeedom/mysql : le dossier de l’hote ou l’on doit stoker les
    données de MySql

-   your-mysql-password : le mot de passe root de l’instance MySql

Etape 3 : Installation d’une image Jeedom 
---

Installation de l’image :

    docker pull jeedom/jeedom

Puis lancez la :

    sudo docker run --name jeedom-server --link jeedom-mysql:mysql --privileged -v /your/jeedom/path:/var/www/html -e ROOT_PASSWORD=your-root-password -p 9080:80 -p 9022:22 jeedom/jeedom

Avec :

-   jeedom-server : nom du Docker jeedom voulu

-   /your/jeedom/path : répertoire où les données de Jeedom sont mises
    sur l’hôte

-   your-root-password : mot de passe root pour accéder à Jeedom en SSH

Il vous faut ensuite installer Jeedom en allant sur : IP\_DOCKER:9080 et
entrer les informations de connexion vers mysql :

![install other](../images/install_other.PNG)

Pour la suite, vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index)

> **Important**
>
> Pour le nom de l’hote MySql, il faut mettre jeedom-mysql

Synology
========

Vous trouverez ici la documentation pas à pas pour installer Jeedom sur un
Synology (DSM 5.2 minimum).

Etape 1 : Installation de Docker 
================================

Allez sur le centre des paquets :

![install synology 1](../images/install_synology_1.PNG)

Cliquez sur tous, puis installez le paquet Docker

![install synology 2](../images/install_synology_2.PNG)

Attendez jusqu’à ce que l’installation soit finie :

![install synology 3](../images/install_synology_3.PNG)

> **Important**
>
> Pour avoir accès au paquet Docker, il faut absolument avoir DSM 5.2 et
> un NAS compatible

Etape 2 : Récupération et installation des images Jeedom 
========================================================

Il faut Docker pour faire tourner Jeedom, le premier un Docker Mysql qui
contiendra la base de données et un 2ème qui contient Jeedom

Lancez l’application Docker :

![install synology 4](../images/install_synology_4.PNG)

MYSQL 
-----

Cliquez sur "Registre" :

![install synology 5](../images/install_synology_5.PNG)

Dans le champ de recherche tapez "mysql", selectionnez mysql et cliquez
sur télécharger :

![install synology 15](../images/install_synology_15.PNG)

Validez ensuite la demande de version, le mieux étant de prendre la
version latest :

![install synology 14](../images/install_synology_14.PNG)

Cliquez ensuite sur image, ici vous pouvez suivre l’avancement du
téléchargement (peut prendre plusieurs dizaines de minutes) :

![install synology 16](../images/install_synology_16.PNG)

Une fois terminé, cliquez sur l’image puis lancer :

![install synology 17](../images/install_synology_17.PNG)

Donnez un nom à votre mysql ainsi qu’un port local redirigé vers le port
3306 du conteneur, puis faites suivant :

![install synology 18](../images/install_synology_18.PNG)

Faites suivant :

![install synology 19](../images/install_synology_19.PNG)

Cliquez sur "Paramètres avancés" :

![install synology 34](../images/install_synology_34.PNG)

Puis sur "Ajouter un dossier", et là, mettez le dossier voulu côté
Synology (c’est dans ce dossier qu’il y aura tous les fichiers de la
base de données) et /var/lib/mysql côté conteneur (attention à bien
décocher "Lecture seule")

![install synology 32](../images/install_synology_32.PNG)

Cliquez sur "Environnement" puis "Ajoutez une variable" et mettant dans
"Variable" : "MYSQL\_ROOT\_PASSWORD" et dans valeur mettez le mot de
passe de BDD voulu (il servira plus tard). Puis validez :

![install synology 33](../images/install_synology_33.PNG)

Cochez "Exécuter ce conteneur lorsque l’assistant a terminé" puis
cliquez sur "Appliquer".

Jeedom 
------

Cliquez sur "Registre" :

![install synology 5](../images/install_synology_5.PNG)

Dans le champ de recherche, tapez "jeedom", sélectionnez jeedom/jeedom
et cliquez sur télécharger :

![install synology 20](../images/install_synology_20.PNG)

Validez ensuite la demande de version, le mieux étant de prendre la
dernière.

Cliquez ensuite sur image, ici vous pouvez suivre l’avancement du
téléchargement (peut prendre plusieurs dizaines de minutes) :

![install synology 21](../images/install_synology_21.PNG)

Une fois terminé, cliquez sur l’image puis lancez :

![install synology 22](../images/install_synology_22.PNG)

Donnez un nom à votre jeedom ainsi qu’un port local redirigé vers le
port 80 (ici 9080) et un vers le 22 (ici 9022) du conteneur, puis faites
suivant :

![install synology 23](../images/install_synology_23.PNG)

Faites suivant :

![install synology 24](../images/install_synology_24.PNG)

Cliquez sur "Paramètres avancés"

![install synology 25](../images/install_synology_25.PNG)

Puis sur "Ajouter un dossier"

![install synology 26](../images/install_synology_26.PNG)

Choisissez un dossier sur votre Synology (c’est dans ce dossier qu’il y
aura tous les fichiers jeedom), attention à bien décocher "Lecture
seule"

![install synology 27](../images/install_synology_27.PNG)

Dans chemin d’accès, mettez /var/www/html puis cliquez sur
"Environnement" :

![install synology 28](../images/install_synology_28.PNG)

Cochez "Exécuter le conteneur à l’aide de privilèges élevés" puis
validez le tout :

![install synology 29](../images/install_synology_29.PNG)

Cochez "Exécuter ce conteneur lorsque l’assistant a terminé" puis
cliquez sur "Appliquer".

> **Paramètre de configuration avancé**
>
> Il existe 3 paramètres optionnel de configuration, ces paramètres doivent etre passé en variable d'environement
> - APACHE_PORT : permet de changer le port par défaut (80) d'écoute du serveur web
> - SSH_PORT : permet de changer le port par défaut (22) d'écoute du ssh
> - MODE_HOST : indique que le résaux est en mode host

> **IMPORTANT**
>
> Certain plugin on besoin d'avoir le broadcast du réseaux (type plugin Xioami), pour cela il faut ABSOLUMENT passer en le réseaux en mode host (possible uniquement lors de la création), changer le port d'écoute par defaut du serveur web et ssh par des ports non utilisé (type 9080 pour le serveur web et 9022 pour le ssh), et mettre la variable MODE_HOST à 1

Etape 3 : Configuration de Jeedom 
---

Il vous faut maintenant installer Jeedom, c’est très simple, allez sur
IP\_NAS:9080

![install synology 31](../images/install_synology_31.PNG)

Remplissez les champs en fonction de votre configuration (configuration
du Docker mysql installé précédemment) et validez.

> **Important**
>
> L’addresse IP de la BDD est l’addresse IP du NAS, le port est celui
> redirigé du Docker Mysql, le mot de passe est celui mis dans le Docker
> Mysql. Le nom d’utilisateur est root et le nom de la base celui que
> vous voulez (conseillé Jeedom)

![install synology 30](../images/install_synology_30.PNG)

> **Tip**
>
> Si vous voulez un accès SSH, il vous faut dans les ports rediriger un
> port local vers le port 22 du conteneur, les identifiants SSH sont
> root/jeedom. Vous pouvez changer le mot de passe en initialisant la
> variable d’environement ROOT\_PASSWORD à la valeur du mot de passe
> voulu.

Ensuite, vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index)

Autres
======

Vous trouverez ici la documentation pour installer Jeedom sur la plupart
des systèmes linux (testée et approuvée sur la distribution Debian)

> **Important**
>
> Debian 9 (Stretch) est la distribution officiellement supportée pour
> la version 3.1.7 de Jeedom (mais Jessie reste parfaitement
> fonctionnelle). Si vous ne maîtrisez pas un minimum les environnements
> Linux, nous vous conseillons de partir sur une image officielle (OVF)
> ou l’utilisation d’une Mini+ ou Smart (disponible prochainement).

> **Important**
>
> Le script d’installation peut être dangereux, car il part du principe
> que votre système est vierge. Si ce n’est pas le cas merci de lire le
> script et de faire une installation à la main.

Connectez-vous en SSH à votre système et faites :

    wget https://raw.githubusercontent.com/jeedom/core/stable/install/install.sh
    chmod +x install.sh
    ./install.sh

Il vous suffit ensuite d’aller sur IP\_MACHINE\_JEEDOM à partir de votre
navigateur Internet.

> **Note**
>
> Les identifiants par défaut sont admin/admin

> **Note**
>
> Les arguments suivants sont utilisables : -w = dossier webserver -z =
> installation dependances z-wave -m = mot de passe root mysql désiré

    ./install.sh -w /var/www/html -z -m Jeedom

Ensuite, vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index).
