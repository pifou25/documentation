Vous trouverez ici la documentation pour installer Jeedom sur un
raspberry PI **avec une carte SD.**

> **Important**
>
> Debian 9 (Strecht) est la distribution officiellement supportée pour
> la version 3.1.5 de jeedom (mais jessie reste parfaitement
> fonctionnelle).

**1/ Télécharger le dernière image "lite", c’est à dire sans interface
graphique**
[ICI](https://downloads.raspberrypi.org/raspbian_lite/images/raspbian_lite-2017-12-01/2017-11-29-raspbian-stretch-lite.zip)

**2/ Décompresser l’image avec winrar** [Ici](http://www.win-rar.com)

**3/ Graver cette image sur une SD avec etcher par exemple**
[ici](https://etcher.io/)

> **Note**
>
> Si vous utilisez Etcher pour graver votre image, l’étape de
> décompression est inutile (format Zip reconnu directement dans la
> sélection du fichier image).

**4/ Activer un accès SSH**

> **Warning**
>
> Pour des raisons de sécurité, l’accès SSH n’est plus activé par défaut
> sur cette distribution. Il faut donc l’activer.

Il faut créer sur la partition boot (la seule accessible sous windows)
un fichier ssh vide.

Il suffit de faire un clic droit : nouveau / document texte et le
renommer en "ssh" **sans extension**

> **Important**
>
> Sous windows, dans l’explorateur il faut donc vérifier votre
> paramétrage dans affichage / options / modifier les options de
> dossiers et de recherche /

![ExtensionFichier](../images/ExtensionFichier.PNG)

**5/ Démarrer le PI**

Insérer votre carte SD, brancher le cable réseau, brancher
l’alimentation.

**6/ Se connecter en SSH**

Identifier votre Pi sur le réseau

Il faut connaitre l’adresse Ip de votre PI. Plusieurs solutions :

-   Consulter la configuration DHCP dans votre routeur

-   Utiliser un scanner de port type "angyipscanner"
    [ici](http://angryip.org/download/#windows)

Etablir la connexion

Ensuite utiliser par exemple putty pour établir votre connexion
[Ici](http://www.putty.org/)

Rentrer l’adresse de Ip de votre PI (ici 192.168.0.10) et cliquez sur
open. Accepter le message par défaut relatif à la sécurité lors de la
première connexion.

Connectez-vous avec les identifiants **pi / raspberry**

> **Important**
>
> Pour des raisons de sécurité, il est impératif de modifier le mot de
> passe par défaut. Les cas de piratages basés sur l’exploitation du
> couple login/mot de passe par défaut du Raspberry sont
> particulièrement répandus. (commande passwd et sudo passwd)

**7/ Lancer le script d’installation jeedom**

    wget -O- https://raw.githubusercontent.com/jeedom/core/stable/install/install.sh | sudo bash

**Le mot de passe sudo est également raspberry**

> **Note**
>
> En fonction de votre débit internet, l’installation peut prendre de 45
> à 90 minutes. Vous ne devez surtout pas interrompre le processus avant
> la fin. A défaut, il faudra reprendre la totalité de la procédure.

Il vous suffit ensuite d’aller sur IP\_MACHINE\_JEEDOM

> **Note**
>
> Les identifiants par défaut sont admin/admin

> **Note**
>
> Les arguments suivants sont utilisables : -w = dossier webserver -z =
> installation dependances z-wave -m = mot de passe root mysql désiré

    ./install.sh -w /var/www/html -z -m Jeedom

Ensuite vous pouvez suivre la documentation [Premier pas avec
Jeedom](https://github.com/jeedom/documentation/blob/master/premiers-pas/fr_FR/index.asciidoc)
