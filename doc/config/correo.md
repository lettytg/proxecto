#NOTIFICACIÓNS DE ALERTAS POR CORREO


- Vamos a instalar un servidor de correo para integrar G-mail en Zabbix.


![raspi_1](doc/img/imaxes-correo/correo1.PNG)


- Configuramos o arquivo de configuración so smtp.

```
# nano /etc/ssmtp/ssmtp.conf
# root=alertasinvernao@gmail.com
# mailhub=smtp.gmail.com
# FromLineOverride=YES
# AuthUser=alertasinvernao@gmail.com
# AuthPass=+Qwerty-
# UseTLS=Yes
# AuthMethod=LOGIN
```
![raspi_1](doc/img/imaxes-correo/correo2.PNG)
