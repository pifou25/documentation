No es realmente un howto aquí, sino una colección de consejos y trucos
MySQL

Desactivar sistema de incentivos
================================

Editar el archivo y añadir /etc/mysql/mysql.conf.d/mysqld.cnf en:

    [Mysqld]
    performance_schema = OFF

optimizar MySQL
===============

> **Importante**
>
> Este método es a su propio riesgo. Si no se preocupe
> Soporte será posible.

-   Detener el demonio de MySQL y eliminar los archivos de registro:

<! - ->

    servicio de la parada de MySQL
    rm / var / lib / mysql / * ib_logfile

-   A continuación, hacer:

<! - ->

    tocar /etc/mysql/conf.d/jeedom_my.cnf
    echo "[mysqld]" /etc/mysql/conf.d/jeedom_my.cnf >>
    echo "key_buffer_size = 16M" /etc/mysql/conf.d/jeedom_my.cnf >>
    echo "thread_cache_size = 16" >> /etc/mysql/conf.d/jeedom_my.cnf
    echo "tmp_table_size = 48M" /etc/mysql/conf.d/jeedom_my.cnf >>
    echo "max_heap_table_size = 48M" /etc/mysql/conf.d/jeedom_my.cnf >>
    echo "query_cache_type = 1" >> /etc/mysql/conf.d/jeedom_my.cnf
    echo "query_cache_size = 16M" /etc/mysql/conf.d/jeedom_my.cnf >>
    echo "query_cache_limit = 2M" /etc/mysql/conf.d/jeedom_my.cnf >>
    echo "query_cache_min_res_unit = 3K" /etc/mysql/conf.d/jeedom_my.cnf >>
    echo "= O_DIRECT innodb_flush_method" /etc/mysql/conf.d/jeedom_my.cnf >>
    echo "innodb_flush_log_at_trx_commit = 2" >> /etc/mysql/conf.d/jeedom_my.cnf
    echo "innodb_log_file_size = 32M" /etc/mysql/conf.d/jeedom_my.cnf >>

-   Reiniciar MySQL:

<! - ->

    inicio del servicio MySQL
