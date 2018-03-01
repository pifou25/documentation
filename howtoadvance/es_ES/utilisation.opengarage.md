OpenGarage es un tipo de bricolaje del objeto, sino también disponible montado en
control y que sirve en el garaje.

Ofrece la activación de un relé (para abrir el garaje) y una
sensor de distancia para verificar la presencia del coche.

<Http://opengarage.io/>

La lectura de las declaraciones OpenGarage
===============================

Para recuperar el estado del relé y el sensor de distancia para la url
su uso es:

    http: // addropengarage / jc

El resultado es un JSON. Así que utilice un tipo de equipo
Guión y control de la información de tipo JSON

Para el relé de estado el nombre de la propiedad de JSON: Puerta

Para el sensor de distancia: dist

Acción sobre OpenGarage
========================

La dirección para la activación del relé es:

    http: // addropengarage / DC tecla d = xxxx clic = 1?

tecla d es la clave de la API, el valor predeterminado es OpenDoor

Mas información
============

La documentación completa del API está disponible en GitHub:

<Https://github.com/OpenGarage/OpenGarage-Firmware/tree/master/docs>
