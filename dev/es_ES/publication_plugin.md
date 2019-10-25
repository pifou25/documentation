# Cómo publicar el plugin en el market

## Requisitos previos

- S'etre inscrit en tant que dev, voir [ici](https://www.jeedom.com/site/fr/dev.html)
- Avoir attendu la validation du compte market comme developpeur
- Avoir mis votre plugin sur github (dépot privé ou non)

## Configuración

Une fois connecté avec votre compte dev sur le market il faut : 

- cliquer sur market puis sur ajouter
- renseigner les informations sur votre plugin : 
  - General :
    - Precio
    - Id (celui dans le fichier info.json)
    - Nombre
    - Categoría
    - Si il est privé ou non pour commencer
  - Documentación y enlaces
    - la description (bien mettre les point important, la plupart des utilisateurs ne vont pas voir la documentation avant l'achat)
    - los idiomas 
    - el material compatible
    - une note sur l'utilisation si necessaire
  - Github : c'est ici que vous aller mettre les information entre le market et Github
    - le token (a ne mettre que si votre plugin est sur un dépot privé)
    - su nombre de usuario github
    - el nombre del depósito en github
    - cocher la case pour que le market gere la traduction de votre plugin et de la documentation (attention dans ce cas à bien donner tous les droits à l'utilisateur zoic21 de github sur votre dépot github)

   Une fois sauvegardé en retournant dans l'onglet github vous aurez 3-4 champs pour indiquer les branches : 

   - beta
   - estable
   - pro (es inútil en el 99% de los casos)
   - stablev3 (pronto)

   La synchronisation se fait soit automatiquement tous les jours à 12h10 (attention vu le nombre de plugin et les restrictions d'appels api la mise à jour commence à 12h10 mais prendre plusieurs dizaine d'heure). Vous pouvez aussi lancer une synchronisation manuel d'une branche à partir de la fiche plugin
