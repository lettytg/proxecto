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


- Unha vez creada a plantilla, procederemos a crear o **Item**, que é un elemento que nos permite adquirir datos do sistema. Cada elemento ven co seu propio conxunto de chaves e parámetros requeridos.

- En este caso o tipo será Zabbix agent (active), xa que o axente debe tomar o rol de activo, é dicir, vai tomar a iniciativa de comunicar o valor. Para saber que o que ten que comunicar, previamente lle preguntará ao servidor e identificará co seu hostname.

- Como vamos a monitorizar un txt onde estarán gardados os valores, elexiremos como chave **log** e agregaremos a ruta onde está gardado o txt.

- No apartado de tipo de información, elexiremos text, xa que leva números e letras.


![raspi_1](doc/img/imaxes-monitorizacion/moni2.PNG)


- Agora comprobaremos no **Monitoring** - *Latest Data*. Aquí poderemos ver todos os valores recopilados dos distintos elementos.


![raspi_1](doc/img/imaxes-monitorizacion/moni3.PNG)

![raspi_1](doc/img/imaxes-monitorizacion/moni4.PNG)


- Unha vez feito isto, modificaremos o **Dashboard** para que nos apareza a táboa cos valores monitorizados.


![raspi_1](doc/img/imaxes-monitorizacion/moni5.PNG)




