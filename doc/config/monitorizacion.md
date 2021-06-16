#	MONITORIZACIÓN DO SENSOR DE TEMPERATURA CON ZABBIX.

- Para a monitorización dos valores xerados polo sensor de temperatura necesitaremos configurar o axente de Zabbix.

`nano /etc/zabbix/zabbix_agentd.conf`

- Comprobamos no ficheiro de configuración do axente de Zabbix, que están as seguintes opcións ben configuradas.

`Server=127.0.0.1` 

`ServerActive=127.0.0.1`

`Hostname= Zabbix server`

![raspi_1](doc/img/imaxes-monitorizacion/moni0.png)


- Unha vez configurado o anterior, procederemos a reiniciar o servizo do axente de Zabbix e a comprobar o seu estado.

![raspi_1](doc/img/imaxes-monitorizacion/moni01.png)


