Monit es un servicio de monitoreo de servicio. este cargo
verificar que un servicio aún está en marcha.

Para ello, los criterios de evaluación y las acciones se cuenta
tomar.

Instalación de Monit
=====================

Estos son los comandos a ejecutar para instalar monit:

    sudo apt-get -y Monit

Ejemplos de conf
================

Ejemplos de configuración con Jeedom Monit.

la supervisión de Apache
==================

    # Apache (conexión de prueba 80)
    comprobar proceso apache2 con pidfile /var/run/apache2/apache2.pid
        Programa de Inicio = "/etc/init.d/apache2 start"
        Detener el programa = "/etc/init.d/apache2 stop"
           si no el puerto 80 para 2 ciclos a continuación, reinicie

Supervisión Nginx (incluyendo php-fpm)
=====================================

    # Php-FPM
    comprobar proceso php5-FPM con pidfile /var/run/php5-fpm.pid
       Programa de Inicio = "/etc/init.d/php5-fpm empezar"
       Detener el programa = "parada /etc/init.d/php5-fpm"
       si no /var/run/php5-fpm.sock unixsocket
              durante 2 ciclos
              A continuación, reinicie

    # Nginx (conexión de prueba 80)
    comprobar proceso nginx con pidfile /var/run/nginx.pid
       Programa de Inicio = "/etc/init.d/nginx empezar"
       Detener el programa = "/etc/init.d/nginx parar"
          si no el puerto 80 para 2 ciclos a continuación, reinicie

Monitoreo MySQL
=================

    # MySQL (conexión)
    comprobar mysqld proceso con /var/run/mysqld/mysqld.pid pidfile
       Programa de Inicio = "/etc/init.d/mysql start"
       Detener el programa = "/etc/init.d/mysql parar"
           si hay un error
           /var/run/mysqld/mysqld.sock unixsocket
           luego a la alerta

supervisión apcupsd
===================

    # Apcups (si tiene un SAI con este servicio, de lo contrario borrar / adaptación)
    comprobar proceso apcupsd con pidfile /var/run/apcupsd.pid
       Programa de Inicio = "/etc/init.d/apcupsd empezar"
       Detener el programa = "parada /etc/init.d/apcupsd"
          si hay un error 3551 Puerto durante 2 ciclos luego a la alerta
