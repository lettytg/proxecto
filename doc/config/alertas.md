# CONFIGURACIÓN DO SERVIZO SMTP CON POSTFIX PARA RECIBIR ALERTAS DE ZABBIX

## INSTALACIÓN E CONFIGURACIÓN DO POSTFIX


- Instalamos o servidor de correo Postfix e o paquete mail-utils

`sudo apt install postfix`

`sudo apt install mail-utils`

- Seleccionamos "Sen configuración", para despois realizala manualmente.  

![raspi_1](doc/img/imaxes-alertas/alertas1.png)

- Copiamos o ficheiro de configuración **main.cf.proto**, xa que é o ficheiro plantilla.

`cp /etc/postfix/main.cf.proto main.cf`

- Unha vez copiado, configuraremos o ficheiro.

![raspi_1](doc/img/imaxes-alertas/alertas3.png)

- A continuación, reiniciaremos o servizo co seguinte comando:

`sudo service postfix restart`

- Cando teñamos o servizo reiniciado, procederemos a mandar un correo a través da terminal co seguinte comando:

`echo "CORPO DO CORREO" | mail -s "ASUNTO DO CORREO" alertasinvernao@gmail.com`

![raspi_1](doc/img/imaxes-alertas/alertas4.png)

- Unha vez enviado comprobaremos o log.

![raspi_1](doc/img/imaxes-alertas/alertas4.1.png)

- Comprobaremos na bandexa de entrada se hai algún correo.

![raspi_1](doc/img/imaxes-alertas/alertas5.png)


## CONFIGURACIÓN DO CORREO EN ZABBIX

- O seguinte paso será configurar o correo para recibir alertas do Zabbix, para iso iremos a **Administration** - **Media types**.


![raspi_1](doc/img/imaxes-alertas/alertas6.png)


- Agregaremos o correo ao cal se van enviar as alertas, en este caso "alertasinvernao@gmail.com", xunto co seu contrasinal.

- Agregaremos o porto 25, xa que é o porto que utiliza o servizo SMTP, o servidor SMTP que é o localhost (o que configuramos no Postfix).

![raspi_1](doc/img/imaxes-alertas/alertas7.png)

- Enviamos unha notificación manual a través de Zabbix para comprobar que funciona correctamente.

![raspi_1](doc/img/imaxes-alertas/alertas9.png)

![raspi_1](doc/img/imaxes-alertas/alertas10.png)


### CONFIGURACIÓN DE ALERTAS

- En **Configuration** - **Actions** - **Trigger actions** - **Report problems to Zabbix administrators**. Engadiremos "Host equals Zabbix server". Unha vez agregado en "Operations" editaremos a opción "Send message to user groups: Zabbix administrators via all media" e engadiremos o correo electrónico e a mensaxe por defecto que se vai recibir cando se xere unha alerta no servidor.


![raspi_1](doc/img/imaxes-alertas/alertas7.1.png)

![raspi_1](doc/img/imaxes-alertas/alertas8.png)







