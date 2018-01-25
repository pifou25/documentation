EmonCMS es una energía de supervisión de aplicaciones PHP (Emon:
Monitor de energía)

En cuanto al intercambio de datos entre Jeedom y EmonCMS (en
de un modo u otro), se encuentra en este medio de documentación
del implemento.

Una breve nota para instalar emoncms también está disponible (esto
la instalación no está disponible de forma nativa en Jeedom)

EmonCMS se pueden instalar junto a Jeedom o en otro lugar. Puede
incluso utilizar el emoncms.org instancia

Correo electrónico pena Jeedom a EmonCMS
=========================================

Para enviar un valor a Jeedom EmonCMS, la solución más sencilla
porque es nativa disponible es utilizar la URL de un pulsador
información

En Jeedom una configuración avanzada puede acceder haciendo clic en el
rueda dentada de la derecha.

A continuación, en "Configuración avanzada", no es el último parámetro
Empuje URL, llenarlo con dirección de API EmonCMS para la alimentación
queremos llenar

La url de empuje es de la forma:

[https: //serveur/emoncms/input/post.json json = {potencia: \ # valor \} & # apikey = xxx](https://serveur/emoncms/input/post.json?json={power:#value#}&apikey=xxx)

Con los parámetros:

-   Identificación: el id de la alimentación que se encuentra en emoncms

-   apikey: clave de API para leer y escribir a emoncms

-   Valor: usted tiene que dejar una buena relación calidad * * para Jeedom envía
    valor de la información

-   Potencia: se está cambiando para

Notificación a Jeedom o la recuperación de Jeedom
================================================== ====

Para tomar una emoncms de datos en Jeedom, hay dos posibilidades
:

-   La primera es crear un script de información a través de plug-in en Jeedom
    y utilizar la URL de la API de la alimentación. Este método requiere para recuperar
    valorar regularmente o vía la escritura con el ejemplo y normalmente
    no es útil debido a que las fuentes de datos dentro de jeedom \ _setting

        https: //serveur/emoncms/feed/value.json ID = 1 & apikey = xxx?

-   La segunda posibilidad es utilizar el evento Plugin de emoncms
    para desencadenar una acción en ciertas condiciones. este método
    podría ser útil si se trataba de un dado que se calcula o
    directamente recuperado por emoncms (por ejemplo OpenBEM) Con
    la ventaja de que no se dio cuenta de que, en caso necesario, contra el plugin
    evento no hacer flexiones y que pasará por MQTT
    para la conexión de Jeedom

Memo para instalar EmonCMS
================================

La instalación se describe en la página de GitHub:

<Https://github.com/emoncms/emoncms/blob/master/docs/LinuxInstall.md>

Tenga en cuenta que algunos plugins parecen obsoletos con la versión más reciente
EmonCMS (v9 al final de 2015)

Si se instala hay problemas con los menús. De todas formas,
priori sólo tenemos:

git clone <https://github.com/emoncms/event.git> (Es él quien lo hará
permitirá crear eventos sobre las reacciones a emoncms
notificar a Jeedom)

clon git <https://github.com/emoncms/openbem.git> (Este es un plugin para
para controlar el consumo energético de la casa)

clon git <https://github.com/emoncms/energy.git>

clon git <https://github.com/emoncms/report.git>

clon git <https://github.com/elyobelyob/mqtt.git>

configuración Nginx
===================

Aquí está un ejemplo de configuración para Nginx. Para Apache sin
conf especial necesita un repertorio clásico

    alquiler / emoncms {
           Conocido / var / www / emoncms /;
           índice index.php;
            try_files = $ $ uri uri / @missing;

       Alquiler ~ [^ /] \ php (/ | $) {.
               fastcgi_split_path_info ^ (/.*) $ (+ \ php.?.);
               fastcgi_pass UNIX: /var/run/php5-fpm.sock;
               index.php fastcgi_index;
               incluir fastcgi_params;
               fastcgi_param REMOTE_USER $ usuario_remoto;
               fastcgi_param PATH_INFO $ fastcgi_path_info;
               fastcgi_param SCRIPT_FILENAME /var/www/emoncms/index.php;
           }

    }

    Alquiler @missing {
            reescribir ^ / emoncms /(.*)$ /emoncms/index.php?q=$1&$args última;
    }
