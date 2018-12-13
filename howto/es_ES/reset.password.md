Veremos cómo cambiar su contraseña si Jeedom
han olvidado, directamente mediante la modificación en la base de datos
datos.

Lo primero que debe hacer es SSH en Jeedom (con
software como masilla o gatito).

Una vez conectado, es necesario recuperar los identificadores de la base
datos:

``` {.bash}
cat /var/www/html/core/config/common.config.php
```

Aquí se puede encontrar la contraseña para acceder a la base de datos
jeedom que hacer a continuación:

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

>**IMPORTANTE**
>
>No olvide que una vez finalizado el proceso, borre del usuario adminTmp, dejarlo  se convierte en una potencial vulnerabilidad de seguridad.

>**IMPORTANTE**
>
> Si ha activado la autenticación AD/LDAP, este método de reinicio no funcionará a menos que desactive el modo AD/LDAP. Puede hacerlo haciendo: 
>``` {.bash}
>use jeedom;
>REPLACE INTO `config` SET `value`='0',`key`='ldap:enable',`plugin`='core';
>```
