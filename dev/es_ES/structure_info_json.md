**Documentation fichier info.json**

Intégré depuis la version 3.0 de Jeedom, le fichier **info.json** est obligatoire pour le bon fonctionnement des plugins, et leur bon déploiement sur le Market Jeedom.

Le fichier info.json est enregistré dans le dossier /plugin_info/ de votre plugin.

Liste des variables du fichier info.json

Les champs marqués d’un * sont des champs obligatoires.

Campos                   | Valores                                                                                                                   |
------------------------ | ------------------------------------------------------------------------------------------------------------------------- |
id *                     | Identifiant unique du plugin sur le Market Jeedom. Doit debuter par une lettre. Sans accents.                             |
nombre *                   | Nombre del plugin.                                                                                                            |
descripción *            | Description du plugin, tel qu'il s’affichera sur le Market Jeedom Minimum 80 caractères. (`<br/>` pour le retour à la ligne.)                                  |                                                                                     |
uso                    | Informations complémentaires à la documentation sur l’usage du plugin.                                                    |
licencia *                | Tipo de licencia.                                                                                                          |
autor *                 | Nom de l’auteur du plugin, tel qu’il sera affiché une fois le plugin installé, dans les informations de celui-ci.         |
requiere *                | Versión mínima de Jeedom.                                                                                                |
categoría *               | Catégorie de classement du plugin sur le Market jeedom. **Respecter impérativement la nomenclature du tableau ci-dessous** |
móvil                   | Si le plugin utilise un panel dédié sur la webApp Jeedom, il s’agit du nom du fichier principal de ce panel.   |
changelog *              | Lien Html vers le Changelog.                                                                                              |
documentación *          | Lien Html vers la documentation du plugin.                                                                                |
enlace -> video               | Lien Html vers une vidéo de présentation.                                                                                 |
enlace -> foro               | Lien Html vers le forum sur le sujet officiel du plugin.                                                                  |
lenguajes                | Liste des langues disponibles pour le plugin : french, english, german, italian, spanish , russian, indonesian            |
compatibilidad            | Compatibilité du plugin : miniplus, smart, docker, rpi, diy, mobileapp.                                                   |
hasDependency            | «true» si le plugin doit installer des dépendances, sinon «false» ou absent.                                              |
hasOwnDeamon             | «true» si le plugin doit exécuter des deamons, sinon «false» ou absent.                                                   |
maxDependancyInstallTime | Temps maximum imparti pour l’installation des dépendances, exprimé en minutes.                                            |
resultado                    | URL vers le bugtracker si externe (si non remplis alors vous receverez un mail)

**Exemple** :

[Fichier plugin-template/plugin_info/info.json](https://github.com/jeedom/plugin-template/blob/master/plugin_info/info.json)




**NOMENCLATURE CATEGORIES**

Market Jeedom         | info.json               |
--------------------- | ----------------------- |
Comunicación         | comunicación           |
Confort               | wellness                |
Energía               | energía                  |
Tiempo                 | tiempo                 |
Monitoreo            | monitoreo              |
Multimedia            | multimedia              |
Naturaleza                | naturaleza                  |
Objetos conectados      | devicecommunication     |
Organización          | organización            |
Pasarela domótica  | home automation protocol|
Programación         | programación             |
Protocolo domótico   | protocolo de automatización     |
Salud                 | salud                  |
Seguridad              | seguridad                |
Automatismo           | automatisation          |











  









