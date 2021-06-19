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

`echo "PROBA" | mail -s "PROBA CORREO DENDE TERMINAL" alertasinvernao@gmail.com`

![raspi_1](doc/img/imaxes-alertas/alertas4.png)

- Unha vez enviado comprobaremos o log.

![raspi_1](doc/img/imaxes-alertas/alertas4.1.png)

- Comprobaremos na bandexa de entrada se hai algún correo.

![raspi_1](doc/img/imaxes-alertas/alertas5.png)


## CONFIGURACIÓN DO CORREO EN ZABBIX

- O seguinte paso será configurar o correo para recibir alertas do Zabbix, para iso iremos a **Administration** - **Media Types**.

![raspi_1](doc/img/imaxes-alertas/alertas6.png)

- Agregaremos o correo ao cal se van enviar as alertas, en este caso "alertasinvernao@gmail.com", xunto co seu contrasinal.

- Agregaremos o porto 25, xa que é o porto que utiliza o servizo SMTP, o servidor SMTP que é o localhost (o que configuramos no Postfix).

![raspi_1](doc/img/imaxes-alertas/alertas7.png)

- Enviamos unha notificación manual a través de Zabbix para comprobar que funciona correctamente.

![raspi_1](doc/img/imaxes-alertas/alertas9.png)

![raspi_1](doc/img/imaxes-alertas/alertas10.png)


### CONFIGURACIÓN DE ALERTAS

- Vamos configurar o disparador/trigger que se executará cando non reciba valores do archivo a monitorizar.

![raspi_1](doc/img/imaxes-alertas/alertas11.png)

- Imos a paralizar a monitorización do archivo para simular a alerta.

![raspi_1](doc/img/imaxes-alertas/alertas13.png)

- A continuación, iremos a "Administration" - "Users" - "Admin" - "Media" e configuraremos o correo electrónico para ese usuario.

![raspi_1](doc/img/imaxes-alertas/alertas16.png)

- Unha vez feito o trigger, en “Actions” - ”Trigger actions” crearemos unha acción chamada "Monitorización de archivo", cas seguintes condicións:

    - Que a gravedade do trigger sexa: "Average" (Moderada).
    - Que o trigger sexa igual ao Item que contén o trigger do arquivo a monitorizar.

![raspi_1](doc/img/imaxes-alertas/alertas12.png)
   
- Unha vez agregadas as condicións editaremos a opción "Send message to user groups: Zabbix administrators via all media" e engadiremos o correo electrónico e a mensaxe personalizada que se vai recibir cando todas as condicións sexan verdadeiras.

![raspi_1](doc/img/imaxes-alertas/alertas14.png)

- Agora comprobaremos no correo electrónico se recibimos o correo da alerta.

![raspi_1](doc/img/imaxes-alertas/alertas15.png)


