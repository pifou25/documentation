Nous allons voir ici comment changer le mot de passe Jeedom directement
en modifiant celui-ci dans la base de données, dans le cas où vous l’auriez oublié 

Lo primero que debe hacer es SSH en Jeedom (con
software como masilla o gatito).

Una vez que haya iniciado sesión, debe recuperar los identificadores de la base de
datos :

``` {.bash}
cat /var/www/html/core/config/common.config.php
```

Ici, vous trouverez le mot de passe pour accéder à la base de données
Jeedom, il faut ensuite faire :

``` {.bash}
mysql -ujeedom -p
```

Allí se le pide la contraseña recuperada por encima (la contraseña
no aparece: esto es normal). A continuación, introduzca (o mejor,
copiar pegar. Necesitamos "botón derecho del ratón" en la masilla para "pegar"):

``` {.bash}
use jeedom;
REPLACE INTO user SET `login`='adminTmp',password='c7ad44cbad762a5da0a452f9e854fdc1e0e7a52a38015f23f3eab1d80b931dd472634dfac71cd34ebc35d16ab7fb8a90c81f975113d6c7538dc69dd8de9077ec',profils='admin', enable='1';
```

Ahí lo tienes. Puede desconectarse/reconectarse a su Jeedom con la
identificación adminTmp/admin que le permitirán modificar la contraseña
de otras cuentas también.

>**IMPORTANT**
>
>N'oubliez pas une fois vos accès récupéré de bien supprimer l'utilisateur adminTmp, le laisser pourrait être une potentielle
faille de sécurité dont vous seriez seul responsable.

>**IMPORTANT**
>
> Si vous avez activé l'authentification AD/LDAP cette méthode de remise à zéro ne marchera pas à moins de désactiver le mode AD/LDAP. Vous pouvez le faire en faisant : 
>``` {.bash}
>use jeedom;
>REPLACE INTO `config` SET `value`='0',`key`='ldap:enable',`plugin`='core';
>```
