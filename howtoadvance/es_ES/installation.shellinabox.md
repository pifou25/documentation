Shellinabox es accesible desde una consola navegador.

Esto viene en la forma de un servicio de escucha en el puerto 4200
https. Vamos a describir la instalación y la configuración a continuación,
proxy inverso

Instalación Shellinabox
===========================

Este es el comando a ejecutar para instalar Shellinabox:

    sudo apt-get -y shellinabox

Apache proxy inverso
====================

Se debe crear un archivo en
/etc/apache2/sites-enabled/shellinabox.conf con el siguiente contenido
y reinicie Apache

    <Location / jeedom / shellinabox>
    Proxypass http: // localhost: 4200 /
    #ProxyPassReverse http: // localhost: 4200 /
    Dejar de todas las
    </ Location>

Nginx proxy inverso
===================

Se debe crear un archivo en /etc/nginx/sites-enabled/shellinabox.conf
con el siguiente contenido y reinicie Nginx

    Alquiler / jeedom / shellinabox / {
    PROXY_PASS http://127.0.0.1:4200;
    Anfitrión proxy_set_header $ anfitrión;
    proxy_buffering apagado;
    TCP_NODELAY uno;
    access_log apagado;
    }
