Hardware
========

Jeedom can be installed on different hardware components:

-   a Raspberry pi 2 or 3

-   a Synology NAS

-   any Debian-based Linux system

You can also buy a ready made box with Jeedom preinstalled
which also contains a service pack (more support and services) and
Plugins offered:

-   [Jeedom Smart
    Z-Wave +](https://www.domadoo.fr/fr/box-domotique/3959-jeedom-controleur-domotique-jeedom-smart-z-wave.html)

-   [Jeedom Smart Z-Wave + and
    RFXCOM](https://www.domadoo.fr/fr/box-domotique/4043-jeedom-controleur-domotique-jeedom-smart-z-wave-et-interface-rfxcom.html)

-   [Jeedom Smart
    EnOcean](https://www.domadoo.fr/fr/box-domotique/4041-jeedom-controleur-domotique-jeedom-smart-enocean.html)

-   [Jeedom Smart EnOcean and
    RFXCOM](https://www.domadoo.fr/fr/box-domotique/4044-jeedom-controleur-domotique-jeedom-smart-enocean-et-interface-rfxcom.html)

Here is a configuration "type" to start well with Jeedom Z-Wave:

1.  Raspberry pi 3:

    -   Un raspberry+boitier \~ 50 €

    -   Une clef Aeon Gen 5 \~ 60 €

    -   Une micro carte SD \~ 7 €

    -   Une alimentation USB \~ 8 €

That's a total of 125 € for an open source home automation box with a
complete control of his installation.

> **Tip**
>
> It is possible to add or change via an Rfxcom antenna, or a
> key inOcean.

> **Tip**
>
> Jeedom is software that is and will remain open source, its use
> is completely free and does not depend on a cloud or a
> subscription. However, some plugins that allow to increase the
> Jeedom's capabilities or usage may be subject to pay ** and
> may need an internet connection **. You can find
> the list of plugins
> [here](http://market.jeedom.fr/index.php?v=d&p=market&type=plugin).

> **Tip**
>
> Service pack? Quezako? You can see
> [here](https://blog.jeedom.fr/?p=1215) the benefits of service packs.


Jeedomboard
===========

You will find here the documentation step by step to install Jeedom on
the Jeedomboard (or Hummingboard).

> **Tip**
>
> The name of the Jeedom image may be different from that of the captures
> made in this documentation

Step 1: Install Etcher
---

You must download the Etcher software [here] (https://etcher.io/) then
install it on your pc

Step 2: Retrieving the Jeedom image
---

You have to go
[Here](https://www.amazon.fr/clouddrive/share/OwYXPEKiIMdsGhkFeI3eUQ0VcvTEBq0qxQevlXPvPIy/folder/IT3WZ3N0RqGzaLBnBo0qog)
then in the images folder get the image jeedom-jeeboard - \ *. rar or
Jeedomboard \ _ \ _ Debian \ _Jessie \ *. Rar

![install humming 1](../images/install_humming_1.PNG)

Step 3: Decompression of the Jeedom image
---

Decompress the image of Jeedom (if you have nothing to decompress it
you can install
[winrar](http://www.clubic.com/telecharger-fiche9632-winrar.html)), you
must obtain:

![install humming 2](../images/install_humming_2.PNG)

![install humming 8](../images/install_humming_8.PNG)

Step 4: Burn the image on the SD card
---

Insert your SD card into your computer and launch the software
Ether, give him the path of the image, the path of the SD card and
click on "flash". The software will burn the SD card and check the
engraving

All you have to do is put the SD card in the Jeedomboard (or
Hummingboard), to connect the network and the power supply, your Jeedom goes
start (5 min) and you should see it on the network.

> **Tip**
>
> The SSH credentials are jeedom / Mjeedom96

For the continuation you can follow the documentation [First step with
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index.html)

Miniplus / Hummingboard
=====================

You will find here the documentation step by step to install Jeedom on
the mini plus (Hummingboard Solid-Run card).

![jeedom](../images/jeedom.jpg)

Step 1: Install Etcher
---

You must download the Etcher software [here](https://etcher.io/) then
install it on your pc

2nd step :
---

Jessie image recovery. Attention humingboard is not not
a raspberry. ** You must recover this specific iso
which is a jessie for IMX6. **

You have to go
[Here](https://images.solid-build.xyz/IMX6/Debian/sr-imx6-debian-jessie-cli-20171108.img.xz)
and save this image on your PC.

Step 3: Decompression of the image
---

Decompress the image of Jeedom (if you have nothing to decompress it
you can install
[Winrar](http://www.clubic.com/telecharger-fiche9632-winrar.html)).

Step 4: Burn the image on the SD card
---

Insert your SD card into your computer and launch the software
Ether, give him the path of the image, the path of the SD card and
click on "flash". The software will burn the SD card and check the
engraving

You just have to put the SD card in the Mini + to connect the
network and power, your Jeedom will start.

Step 5: Jeedom installation - Launching the script
---

Open an SSH console with putty for exemmple.

> **Tip**
>
> login debian / debian password

> **Tip**
>
> the root password is debian

1 / Configuration of the swap on the Mini + because it is inactive by default with this
distribution.

Log in SSH to your system and do:

    sudo imx6-config

Enter the root password ("debian")

Click OK (your local IP appears - note it to connect to
the end)

Press Enter

Choose the topic 4 swap with the arrows on the keyboard, then intall
Swap (a Swap of 512 is recommended, you can change it at the end of
creating the default swap). Follow the procedure.

**Reboot** and check Swap activation with the command

    sudo reboot

    free - m

2 / Finally run the official script with these 3 commands:

    wget https://raw.githubusercontent.com/jeedom/core/stable/install/install.sh

    chmod + x install.sh

    sudo ./install.sh

**Installation time varies from 60 to 120 minutes**. You must not
interrupt this procedure. If not, we must start all over again. It is
strongly advise to reboot at the end of the installation.

The following arguments are usable:

-w = webserver folder

-z = installation dependencies z-wave

-m = desired mysql root password

    ./install.sh -w / var / www / html -z -m Jeedom

It is advisable to do a reboot of the mini +

    sudo reboot

Then you just have to go to IP \ _MACHINE \ _JEEDOM in your
Navigator.

> **Note**
>
> The default credentials are admin / admin

> **Important**
>
> If you need to re-inject a backup, you must wait between 5 and 10
> minutes to get everything back in order (your admin user /
> admin does not exist anymore ...). You must not turn off
> electrically your mini-plus.

For the continuation you can follow the documentation [First step with
Jeedom] (https://www.jeedom.fr/doc/documentation/premiers-pas/fr_FR/doc-premiers-pas.html)

Raspberry Pi
===========

You will find here the documentation to install Jeedom on a
raspberry PI **with an SD card.**

> **Important**
>
> Debian 9 (Strecht) is the officially supported distribution for
> version 3.1.5 of jeedom (but jessie remains perfectly
> functional).

**1 / Download the latest image "lite", ie without interface
graphic**
[HERE](https://downloads.raspberrypi.org/raspbian_lite/images/raspbian_lite-2017-12-01/2017-11-29-raspbian-stretch-lite.zip)

**2 / Decompress the image with winrar** [Here](http://www.win-rar.com)

**3 / Burn this image on an SD with etcher for example**
[Here](https://etcher.io/)

> **Note**
>
> If you use Etcher to burn your image, the step of
> decompression is useless (Zip format recognized directly in the
> selection of the image file).

**4 / Enable SSH Access**

> **Warning**
>
> For security reasons, SSH access is no longer enabled by default
> on this distribution. It must therefore be activated.

You have to create on the boot partition (the only one accessible under windows)
an empty ssh file.

Just right click: new / text document and the
rename to "ssh" **without extension**

> **Important**
>
> In windows, in the explorer, you have to check your
> setting in display / options / change options of
> records and research /

![ExtensionFichier](../images/ExtensionFichier.PNG)

**5 / Start the PI**

Insert your SD card, connect the network cable, connect
food.

**6 / Login in SSH**

Identify your Pi on the network

You need to know the IP address of your IP. Many solutions :

-   View the DHCP configuration in your router

-   Use a port scanner type "angyipscanner"
    [right here](http://angryip.org/download/#windows)

Establish the connection

Then use for example putty to establish your connection
[Here](http://www.putty.org/)

Enter the IP address of your IP (here 192.168.0.10) and click on
open. Accept the default message about security when
first connection.

Sign in with the **pi / raspberry** credentials

> **Important**
>
> For security reasons, it is imperative to modify the word
> passes by default. Cases of piracy based on the exploitation of
> default login / password of the Raspberry are
> particularly widespread. (passwd and sudo passwd command)

**7 / Run the jeedom installation script**

    wget -O- https://raw.githubusercontent.com/jeedom/core/stable/install/install.sh | sudo bash

**The sudo password is also raspberry**

> **Note**
>
> Depending on your internet speed, the installation may take 45
> 90 minutes. You should not interrupt the process before
> the end. Otherwise, it will be necessary to resume the entire procedure.

Then you just have to go to IP \ _MACHINE \ _JEEDOM

> **Note**
>
> The default credentials are admin / admin

> **Note**
>
> The following arguments are usable: -w = webserver folder -z =
> installation dependencies z-wave -m = desired mysql root password

    ./install.sh -w / var / www / html -z -m Jeedom

**8/ Optimisation système

Si vous utiliser votre Raspberry pour Jeedom sans écran connecté, il est recommandé d'effectuer le minimum de RAM à la partie vidéo.

Il suffit de se connecter en **SSH** et de modifier le fichier config : `sudo nano /boot/config.txt`

Ajoutez **et/ou**De-commentez (en supprimant le #)**et/ou** Modifiez les lignes : 

`gpu_mem=16`

`disable_l2cache=0`

`gpu_freq=250`

Quitter en sauvegardant : `CTRL+X` puis `O `puis `ENTREE`

Rebooter votre RPI

Ensuite vous pouvez suivre la documentation [Premier pas avec
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

Télécharger une image minimaliste debian 9 Strecht
[Ici](https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-9.3.0-amd64-netinst.iso)

Télécharger le pack d’extensions, et installez-le.
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

-   Sélectionner stockage

-   Ajouter un lecteur optique

-   Choisir un disque

![VirtualBox2](../images/VirtualBox2.PNG)

-   Indiquez l’image précédemment téléchargée

-   Sélectionner ensuite réseau et choisir "accès par pont" dans le mode
    d’accès réseau.

![VirtualBox3](../images/VirtualBox3.PNG)

-   Cliquez sur OK \*Cliquez sur démarrer

Etape 5 : Installation de debian 9 
---

C’est du classique …​

![VirtualBox4](../images/VirtualBox4.PNG)

-   Choisir Graphical install

-   Installer la debian de préférence sans interface graphique
    car inutile. Le nom d’utilisateur n’a aucune importance. Dans la
    plupart des écrans il suffit de valider le choix par défaut. Vous
    pouvez laissez des champs vides ce n’est pas bloquant.

-   Pour la sélection des logiciels :

![VirtualBox5](../images/VirtualBox5.PNG)

-   Pour Grub, pas d’inquiétude, le secteur de démarrage est celui de la
    VM, pas celui de votre PC. Aucun risque de casser quoi que ce soit.

Etape 6 : Installation de jeedom 
---

-   Lancez votre VM

-   Identifiez-vous avec l’utilisateur et le mot de passe choisis
    pendant l’installation

-   Passer en root

<! - ->

    su

-   Saisissez le mot de passe root défini pendant l’installation

-   Récupérer le script jeedom, le rendre exécutable, le lancer

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
> Si cela ne fonctionne pas, vous n’avez pas configurer votre carte
> réseau en Pont réseau comme indiquée au départ.

Ensuite vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index)

Docker
======

> **Important**
>
> Attention nous partons ici du principe que vous maitrisez déjà docker

Pour découvrir Jeedom vous pouvez aussi le faire tourner dans un
conteneur Docker :

> **Important**
>
> Prérequis : Avoir une machine ou une VM tournant sous Linux

Etape 1 : Installation de docker 
---

docker est maintenant disponible sur toutes les distributions récentes.
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
> dans ce cas il faut sauter cette étape.

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

-   jeedom-server : nom du docker jeedom voulu

-   /your/jeedom/path : répertoire où les données de Jeedom sont mise
    sur l’hôte

-   your-root-password : mot de passe root pour accéder à Jeedom en SSH

Il vous faut ensuite installer Jeedom en allant sur : IP\_DOCKER:9080 et
entrer les informations de connexion vers mysql :

![install other](../images/install_other.PNG)

Pour la suite vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index)

> **Important**
>
> Pour le nom de l’hote MySql il faut mettre jeedom-mysql

Synology
========

Vous trouverez ici la documentation pas à pas pour installer Jeedom un
Synology (DSM 5.2 minimum).

Etape 1 : Installation de Docker 
================================

Aller sur le centre des paquets :

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

Il faut Docker pour faire tourner Jeedom, le premier un docker Mysql qui
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

Une fois terminé, cliquez sur l’image puis lancer :

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

Etape 3 : Configuration de Jeedom 
---

Il vous faut maintenant installer Jeedom, c’est très simple, allez sur
IP\_NAS:9080

![install synology 31](../images/install_synology_31.PNG)

Remplissez les champs en fonction de votre configuration (configuration
du docker mysql installé précédemment) et validez.

> **Important**
>
> L’addresse IP de la BDD est l’addresse IP du NAS, le port est celui
> redirigé du docker Mysql, le mot de passe est celui mis dans le docker
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
> fonctionnelle). Si vous ne maîtriser pas un minimum les environnements
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

Ensuite vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://jeedom.github.io/documentation/premiers-pas/fr_FR/index).
