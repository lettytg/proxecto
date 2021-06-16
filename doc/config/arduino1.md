#	INSTALACIÓN DO IDE ARDUINO EN RASPBERRY PI.

- Para usar a interface en serie de Raspberry Pi, debe estar habilitada no menú de configuración. Para iso, introducimos o seguinte comando.

`sudo raspi-config`

![raspi_1](doc/img/imaxes-arduino/ardu13.png)


- Seleccionamos "**Opcións da interface**" - "**P6 Serial Port**".


![raspi_1](doc/img/imaxes-arduino/ardu14.png)


- Unha vez realizada a conexión, podemos comprobar os dispositivos conectados ao porto serie co seguinte comando.
- En este caso  o nome do porto é ttyACM0.

`lsusb`


![raspi_1](doc/img/imaxes-arduino/ardu15.png)


- Para instaar o IDE de Arduino na Raspberry Pi, o mellor é facelo dende a terminal. Para iso procedemos a descargar o seguinte:


![raspi_1](doc/img/imaxes-arduino/ardu16.png)

![raspi_1](doc/img/imaxes-arduino/ardu17.png)


- Agora no menú de **Programación** poderemos ver que foi instalado o IDE correctamente.


![raspi_1](doc/img/imaxes-arduino/ardu18.png)


- Comprobamos que efectivamente se ve o porto.


![raspi_1](doc/img/imaxes-arduino/ardu19.png)




