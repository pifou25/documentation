OpenGarage is a DIY object but also available mounted on
order and who serves in the garage.

It proposes the activation of a relay (to open the garage) and a
distance sensor to check the presence of the car.

<Http://opengarage.io/>

Reading the states of OpenGarage
===============================

In order to recover the state of the relay and the distance sensor, the url to
use is:

    http: // addropengarage / jc

The result is a json. It is therefore necessary to use a type of equipment
Script and an info command of type json

For relay status the property name of the json: door

For the distance sensor: dist

Action on OpenGarage
========================

The address for relay activation is:

    http: // addropengarage / DC dkey = xxxx click = 1?

dkey is the key of the API, by default it is opendoor

More informations
============

The complete documentation of the API is available on github:

<Https://github.com/OpenGarage/OpenGarage-Firmware/tree/master/docs>
