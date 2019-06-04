# Asistentes vocales cloud

## Descripción

C'est un service Jeedom SAS, gratuit le temps des tests en beta, qui deviendra payant par la suite une fois celui-ci stabilisé. Il prends en compte les assistants vocaux de Google et d'Amazon.

## Pourquoi est-ce payant ?

Ce service nous oblige a mettre en place une infrastructure de serveur entre vos Jeedom et les serveurs de Google ou Amazon. Cela à donc un coup récurrent pour Jeedom SAS.
De plus ces 2 services nous demandes beaucoup de temps de maintient/developpement et nous impose une grosse charge de travail pour la partie validation avec Amazon ou Google.

## Comment l'utiliser 

Il faut : 

- avoir du crédit (voir [ici](https://www.jeedom.com/market/index.php?v=d&p=profils#services) pour l'abonnement)
- avoir le plugin Dialogflow, [documentation](https://jeedom.github.io/plugin-dialogflow/fr_FR/)
- ou le plugin Google Smarthome, [documentation](https://jeedom.github.io/plugin-gsh/fr_FR/)
- ou le plugin Alexa, [documentation](https://jeedom.github.io/plugin-ash//fr_FR/)

Vous trouverez dans la documentation respective des plugins leurs différences.

Ensuite une fois l'abonnement pris il faut attendre la synchronisation (voir chapitre suivant). Vous pouvez faire la configuration en suivant la documentation du plugin

## Synchronisation et délai

Il y a des délai de synchronisation lors des actions suivantes :

- Activation du compte
- Achat d'année sur le service Assistant Vocaux
- Changement de clef api du plugin Google smarthome
- Changement de l'url du jeedom
- Changement de mot de passe market

La synchronisation se fait toute les 6h (à 00h10,6h10,12h10,18h10). Cette synchronisation est du a notre volonté de rendre le serveur tierce qui fait le pont entre votre Jeedom et l'infrastructure Google/Amazon independant et autonome (ca évite lors d'un soucis sur le market par exemple de perdre aussi les service Assistant vocaux). Lors de la synchronisation il y a un redemarrage du service (coupure de moins de 1s), ce qui explique la limitation à une fois toute les 6h.
