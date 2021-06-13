#NOTIFICACIÓNS DE ALERTAS POR CORREO


- Vamos a instalar un servidor de correo para integrar G-mail en Zabbix.


![raspi_1](doc/img/imaxes-correo/correo1.PNG)


- Configuramos o arquivo de configuración so smtp.

```
# nano /etc/ssmtp/ssmtp.conf
# root=alertaszabixx@gmail.com
# mailhub=smtp.gmail.com
# FromLineOverride=YES
# AuthUser=alertaszabixx@gmail.com
# AuthPass=Abc123..
# UseTLS=Yes
# AuthMethod=LOGIN
```
