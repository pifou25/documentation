Nodered está escrito en NodeJS herramienta para gestionar la IO orientado o un arroyo
domótica. Ofrece una interfaz gráfica para editar flujos. la
tutorial describe su instalación, configuración y un proxy inverso
La puesta en marcha

Instalación Nodered
=======================

Estos son los comandos para ejecutar la instalación nodered tener un nodejs
funcional:

    sudo apt-get -y install libavahi-compat-libdnssd-dev libusb-1.0-0-dev build-essential
    sudo NPM instalar -g nodo-roja

Para NodeJS puede instalar un plugin que en jeedom
carga.

Inicio automático Nodered
================================

Es posible declarar Nodered como un servicio para que
inicie automáticamente en el arranque de la caja. Un ejemplo aquí:

<Https://gist.github.com/bigmonkeyboy/9962293>

Configuración de Apache
======================

Aquí es un archivo de ejemplo para acceder a través de un Nodered inversa
proxy.

    <Location / jeedom / nodered>
    ws ProxyPass: // localhost: 1880 / jeedom / nodered /
    ProxyPass http: // localhost: 1880 / jeedom / nodered /
    ws #ProxyPassReverse: // localhost: 1880 / jeedom / nodered /
    #ProxyPassReverse http: // localhost: 1880 / jeedom / nodered /
    </ Location>

Configuración de Nginx
======================

Aquí es un archivo de ejemplo para acceder a través de un Nodered inversa
proxy.

    Alquiler / jeedom / nodered / {
      PROXY_PASS http://127.0.0.1:1880;
      Anfitrión proxy_set_header $ anfitrión;
      proxy_buffering apagado;
      TCP_NODELAY uno;
      access_log apagado;
      proxy_http_version 1,1;
      Asciende proxy_set_header $ http_upgrade;
      proxy_set_header Conexión 'Upgrade';
      proxy_redirect apagado;
      proxy_read_timeout 6000;
    }

módulos existentes para Nodered
==============================

Ejemplos de extensiones disponibles para Nodered.

Avahi / Bonjour Discovery Module
==============================

sudo NPM instalar nodo-red-nodo-descubrimiento -g \ # sudo Google Módulo NPM
instalar node-rojo-nodo Google--g \ # eventos solares Módulo sudo NPM instalan
nodo-rojo-contrib-sunevents -g \ # JSON ruta sudo NPM instalar
nodo-rojo-contrib-jsonpath -g \ # módulo geocerca, comprobar si la ubicación
es en la zona de la NGP sudo instalar nodo-red-nodo-geocerca -g \ # geohas, decodificar
latitud longitud de cadena de NPM sudo instalar nodo-red-nodo-geohash -g
\ # Recomendación Cuadrangular de la ubicación NPM sudo instalar
nodo-red-nodo en cuadro -g \ # Ping sudo NPM instalar
nodo-rojo-contrib-avanzada de ping-sudo NPM instalar -g -g nodo-red-nodo-ping
\ # WOL sudo NPM instalar nodo-red-nodo-wol -g \ # sudo NPM instalar SNMP
nodo-red-nodo-SNMP -g \ # sudo NPM instalar Tiempo
nodo-red-nodo-forecastio sudo NPM instalar -g
nodo-red-nodo-OpenWeatherMap sudo NPM instalar -g
nodo-red-nodo-tiempo-subterránea -g \ # sudo general GPIO NPM instalar
nodo-rojo-contrib-GPIO -g \ # de Electirc Imp sudo NPM instalar -g imp-io \ #
Spark Core sudo NPM instalar chispa io -g \ # Arduino / Firmata sudo NPM
firmata instalar -g \ # Pushover sudo NPM instalar nodo-red-nodo-presa fácil
-g \ # notificar a mi Android sudo NPM instalar nodo-red-nodo-nes -g \ #
Pushbullet sudo NPM instalar nodo-red-nodo-pushbullet -g \ vagabundeo # sudo
NPM instalar nodo-red-nodo-acecho -g \ # XMPP sudo NPM instalar
nodo-red-nodo en XMPP -g \ # IRC sudo NPM instalar nodo-red-nodo-irc -g \ #
Holgura sudo NPM instalar nodo-rojo-contrib-holgura -g \ # Pusher sudo NPM
install nodo-red-nodo-empujador -g \ # sudo NPM instalación de almacenamiento
nodo-red-nodo-dropbox sudo NPM instalar -g nodo-red-nodo-flickr sudo -g
NPM instalar nodo-red-nodo-AWS sudo NPM instalar -g -g nodo-rojo-caja-nodo
\ Música # sudo instalar NPM nodo-rojo-contrib-mpd sudo NPM instalar -g
nodo-rojo-contrib-mopidy -g \ # sudo Actividades NPM instalar
nodo-red-nodo-Fitbit sudo NPM instalar -g nodo-red-nodo-jawboneup sudo -g
NPM instalar nodo-red-nodo-strava -g \ # KNX / EIBD sudo NPM instalar
nodo-rojo-contrib-EIBD -g \ # OpenZwave sudo NPM instalar
nodo-rojo-contrib-openzwave -g \ # RFXCOM sudo NPM instalar
nodo-rojo-contrib-RFXCOM -g \ # OWFS sudo NPM instalar
nodo-rojo-contrib-owfs -g \ Nido # sudo instalar NPM nodo-rojo-contrib-nido
-g \ # Hue sudo NPM instalar nodo-rojo-contrib-hue -g \ # Spark-Core sudo
NPM instalar nodo-rojo-contrib-sparkcore -g \ # Wemo sudo NPM instalar
nodo-red-nodo-WEMO -g \ # ZiBASE sudo NPM instalar nodo-rojo-contrib-ZiBASE
-g \ # SensorTag sudo NPM instalar nodo-red-nodo-sensortag -g \ #
Blinkstick sudo NPM instalar nodo-red-nodo-blinkstick -g \ # sudo Blink1
NPM instalar nodo-red-nodo-blink1 -g \ # Tellstick * sudo NPM instalar
nodo-rojo-contrib-tellstick -g \ # PiTFT \ NPM instalar #sudo
nodo-rojo-contrib-pitft toque -g \ # Pibrella \ NPM instalar #sudo
nodo-red-nodo-pibrella -g \ #sudo apt-get -y install python-rpi.gpio \ #
PiBord \ #sudo NPM instalar nodo-red-nodo-ledborg -g \ # Sensores \ #sudo NPER
install nodo-rojo-contrib-BMP085 -g \ NPM instalar #sudo
nodo-rojo-contrib-DS18B20 sensor -g \ NPM instalar #sudo
nodo-rojo-contrib-DHT-sensor -g \ # GPIO \ # HummingBoard \ #sudo NPER
instalar nodo-red-nodo-hbgpio -g \ #sudo PC
nodo \ _modules / nodo-red-node-hbgpio / gpiohb / usr / local / bin / \ #sudo chmod
4755 / usr / lcoal / bin / gpiohb \ # Frambuesa Pi \ #sudo NPM instalar Raspi-io
-g \ # * BEAGLEBONE Negro \ #sudo NPM instalar -g BEAGLEBONE-io \ #
Galileo / Edison \ #sudo NPER instalar Galileo-io -g \ # Blend Micro \ #sudo
NPM instalar micro-mezcla-io -g \ # LightBlue frijol \ NPM instalar #sudo
frijol-io -g
