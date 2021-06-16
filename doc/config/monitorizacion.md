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


- Agora comprobaremos no **Monitoring** - **Latest Data**. Aquí poderemos ver todos os valores recopilados dos distintos elementos.


![raspi_1](doc/img/imaxes-monitorizacion/moni3.PNG)

![raspi_1](doc/img/imaxes-monitorizacion/moni4.PNG)


- Unha vez feito isto, modificaremos o **Dashboard** para que nos apareza a táboa cos valores monitorizados.


![raspi_1](doc/img/imaxes-monitorizacion/moni5.PNG)


##	CREACIÓN DO USUARIO ESTÁNDAR INVERNADOIRO.


- Como ben sabemos, o usuario do invernadoiro necesitará un usuario para poder acceder ao Zabbix e ver os resultados da monitorizacion do sensor. O usuario ten que ser un usuario estándar, e dicir, un usuario que teña uns permisos determinados, para que non poida modificar ningunha configuración.  
- Para levar isto acabo, crearemos un usuario no apartado **Administration** - **Users**. 


![raspi_1](doc/img/imaxes-monitorizacion/moni6.PNG)


- Crearemos o usuario, agregando ao grupo **Guest** que sería o invitado.

    - **Nome:** invernadoiro.
    - **Contrasinal:** abc123..

![raspi_1](doc/img/imaxes-monitorizacion/moni7.PNG)


- Agora procederemos a crear un rol, no cal elexiremos os privilexios que vai ter o usuario "invernadoiro". Para crear o rol seleccionaremos **Administration** - **User roles**


![raspi_1](doc/img/imaxes-monitorizacion/moni8.PNG)

![raspi_1](doc/img/imaxes-monitorizacion/moni9.PNG)

- Unha vez creado o rol, iremos ao usuario e na pestana de **Permissions** e agregaremolo.


![raspi_1](doc/img/imaxes-monitorizacion/moni10.PNG)


- Agora entraremos co usuario invernadoio e comprobaremos que funciona correctamente e que ten os permisos necesarios.


![raspi_1](doc/img/imaxes-monitorizacion/moni11.PNG)

