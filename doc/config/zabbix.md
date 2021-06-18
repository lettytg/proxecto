#	INSTALACIÓN E CONFIGURACIÓN DE ZABBIX.


## INSTALACIÓN DE ZABBIX.

- Antes de facer nada vamos a actualizar o equipo.


![raspi_1](doc/img/imaxes-zabbix/zabbix1.png)


- Vamos instalar o paquete ntp, xa que é moi importante manter o correcto funcionamento da fecha e hora do sistema.


`# apt-get install ntp`


![raspi_1](doc/img/imaxes-zabbix/zabbix2.png)


- Habilitamos o servizo ntp.


`# systemctl enable ntp`


![raspi_1](doc/img/imaxes-zabbix/zabbix3.png)


- Engadimos no ficheiro de configuración /etc/ntp.conf os servidores referentes a rexión de España.


`# server 0.es.pool.ntp.org`


`# server 0.europe.pool.ntp.org`


`# server 2.europe.pool.ntp.org`


![raspi_1](doc/img/imaxes-zabbix/zabbix4.png)


- Reiniciamos o servizo e verificamos o estado do mesmo.


`# service ntp restart`


`# service ntp status`


![raspi_1](doc/img/imaxes-zabbix/zabbix5.png)


- Reiniciamos a máquina e comprobamos que temos correctamente configurada a franxa horaria.


`# date`


![raspi_1](doc/img/imaxes-zabbix/zabbix6.png)


- Procedemos a instalar Zabbix dende a [páxina oficial](https://www.zabbix.com/download?os_distribution=raspberry_pi_os/)


`# wget https://repo.zabbix.com/zabbix/5.4/raspbian/pool/main/z/zabbix-release/zabbix-release_5.4-1+debian10_all.deb`

`# dpkg -i zabbix-release_5.4-1+debian10_all.deb`


![raspi_1](doc/img/imaxes-zabbix/zabbix7.png)


- A continuación vamos a instalar o servidor, a interface e o axente de Zabbix.


`# apt install zabbix-server-mysql zabbix-frontend-php zabbix-apache-conf zabbix-sql-scripts zabbix-agent`


![raspi_1](doc/img/imaxes-zabbix/zabbix8.png)


- Vamos a instalar unha base de datos, en este caso o paquete mariadb, xa que Zabbix require de un sistema de base de datos para almacenar toda a súa configuración.

`# apt install mariadb server mariadb client`


![raspi_1](doc/img/imaxes-zabbix/zabbix9.png)


- Agora accedemos a consola do servidor MySQL.

- Na consola de MySQL, realizaremos as seguintes tarefas.

        -  Crearemos unha base de datos chamada “zabbix”.

        -  Crearemos unha conta de usuario MySQL chamada “zabbix”

        -  Darémoslle permisos totais sobre a base de datos zabbix o usuario de zabbix.


![raspi_1](doc/img/imaxes-zabbix/zabbix10.png)


- O seguinte paso é importar o esquema e os datos iniciais.


![raspi_1](doc/img/imaxes-zabbix/zabbix11.png)


- Vamos a configurar o arquivo de configuración do servidor Zabbix.


`# nano /etc/zabbix/zabbix_server.conf`


- Descomentamos e completamos as seguintes liñas:


`# DBHost= localhost`

`# DBName= zabbix`

`# DBUser = zabbix`

`# DBPassword = abc123..`

`# Timeout = 4`

`# LogSlowQueries= 3000`

![raspi_1](doc/img/imaxes-zabbix/zabbix12.png)


- Iniciamos os procesos do axente e do servidor de Zabbix.

`# systemctl restart zabbix-server zabbix-agent apache2`

`# systemctl enable zabbix-server zabbix-agent apache2`


![raspi_1](doc/img/imaxes-zabbix/zabbix13.png)


- Agora procedemos a acceder a Zabbix no seguinte enlace: http://ip/zabbix/setup.php.


![raspi_1](doc/img/imaxes-zabbix/zabbix14.png)



- Verificamos que os requisitos de Zabbix se cumpriron correctamente.


![raspi_1](doc/img/imaxes-zabbix/zabbix15.png)


- Ingresamos a información de inicio de sesión de MySQL requirida para conectarse a base de datos de Zabbix.


![raspi_1](doc/img/imaxes-zabbix/zabbix16.png)


- Dámoslle a seguinte.


![raspi_1](doc/img/imaxes-zabbix/zabbix17.png)


- Configuramos a zona horaria e o tema de Zabbix.


![raspi_1](doc/img/imaxes-zabbix/zabbix18.png)


- Comprobamos que está correctamente a configuración.


![raspi_1](doc/img/imaxes-zabbix/zabbix19.png)


- Unha vez xa configurado.

- O usuario para iniciar en Zabbix é “Admin”, e o seu contrasinal é “zabbix”.


![raspi_1](doc/img/imaxes-zabbix/zabbix20.png)



