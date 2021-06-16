#	MONITORIZACIÓN DO SENSOR DE TEMPERATURA CON ZABBIX.

- Para a monitorización dos valores xerados polo sensor de temperatura necesitaremos configurar o axente de Zabbix.

`nano /etc/zabbix/zabbix_agentd.conf`

- Comprobamos no ficheiro de configuración do axente de Zabbix, que están as seguintes opcións ben configuradas.

`Server=127.0.0.1` 

`ServerActive=127.0.0.1`

`Hostname= Zabbix server`

![raspi_1](doc/img/imaxes-monitorizacion/moni0.png)


- Unha vez configurado o anterior, procederemos a reiniciar o servizo do axente de Zabbix e a comprobar o seu estado.

![raspi_1](doc/img/imaxes-monitorizacion/moni01.PNG)


- Agora procederemos a ir ao noso Zabbix, no panel do Menú, seleccionaremos **Configuration** - **Templates**.
- Un **Template** ou **Plantilla** é un conxunto de (items, triggers, graphs, screens..) preparados para ser aplicados a un ou varios hosts. O traballo das plantillas é acelerar a imprantación das tarefas de supervisión no host, tamén para facilitar a aplicación de cambios masicos nas tarefas de supervisión.

- En este caso chamaremos a plantilla **aplicacionMonitorizar** e agregaremos os grupos aos que vai pertencer dita plantlla.


![raspi_1](doc/img/imaxes-monitorizacion/moni1.PNG)

![raspi_1](doc/img/imaxes-monitorizacion/moni1.1.PNG)


- Unha vez creada a plantilla, procederemos a crear o seu **Item**, que son  

