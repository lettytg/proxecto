#	INSTALACIÓN E CONFIGURACIÓN BÁSICA DE RASPBERRY PI OS


## AGREGACIÓN DA IMAXE RASPBIAN NA MICROSD A TRAVÉS DE RASPBERRY PI IMAGER.

- Para poder utilizar este sistema operativo necesitaremos agregar a imaxe nunha MicroSD, que será incorporada na Raspberry Pi para iso descargaremola dende a súa [páxina oficial](https://www.raspberrypi.org/software/). O software que se vai utilizar chámase Raspberry Pi Imager.


![raspi_1](doc/img/imaxes-raspbian/rasp1.png)


- Escollemos a imaxe que desexamos agregar na MicroSD:


![raspi_1](doc/img/imaxes-raspbian/rasp2.png)


- Unha vez seleccionada a imaxe, escolleremos o dispostivo na cal agregará a mesma e seleccionaremos **write** para que escriba:


![raspi_1](doc/img/imaxes-raspbian/rasp3.png)


- Aquí podemos ver que está preparando o dispostivo para grabar:


![raspi_1](doc/img/imaxes-raspbian/rasp4.png)


- Agora esperamos a que se complete:


![raspi_1](doc/img/imaxes-raspbian/rasp5.png)



## INSTALACIÓN DE RASPBERRY Pi OS


- Unha vez rematada a grabación, insertaremos a MircoSD na Raspberry PI, conectaremos o cable de rede para que lle asigne unha ip tamén agregaremos o cable HDMI para a saída de vídio e os dispostivos correspondentes para o manexo óptimo (teclado e rato).


![raspi_1](doc/img/imaxes-raspbian/rasp6.png)


- Unha vez manexado o sistema, abriremos unha consola para ver que ip se lle asignou:

`# ip a` (En este caso: 192.168.1.37/24)

![raspi_1](doc/img/imaxes-raspbian/rasp7.png)


- O seguinte paso será habilitar os servizos SSH e VNC. Para iso, iremos a **Preferencias > Configuración Raspberry Pi**. Isto permitiranos conectarnos remotamente dende o noso equipo de traballo.


![raspi_1](doc/img/imaxes-raspbian/rasp8.png)


![raspi_1](doc/img/imaxes-raspbian/rasp9.png)


- Agora veremos que na parte superior da barra encontraremos unha icona de cor azul indicando que o VNC está activado.


![raspi_1](doc/img/imaxes-raspbian/rasp10.png)


- Unha vez feito isto logueamonos como root e deixamos actualizando o sistema:

`# apt update `

![raspi_1](doc/img/imaxes-raspbian/rasp11.png)

`# apt upgrade `

![raspi_1](doc/img/imaxes-raspbian/rasp12.png)


## INSTALACIÓN DO VNC NO EQUIPO DE TRABALLO.


- Descargamos o VNC dende a súa [páxina oficial](https://www.realvnc.com/es/connect/download/viewer/).

- Unha vez descargado e instalado, abrimos o aplicativo.


![raspi_1](doc/img/imaxes-raspbian/rasp13.png)


- Para crear unha conexión iremos a Arquivo > Nova conexión:

` VNC SERVER: A ip da Raspberry Pi `

` NOME: O nome co que queremos que se garde a conexión `


![raspi_1](doc/img/imaxes-raspbian/rasp14.png)


- Seleccionamos aceptar e sairanos unha ventá que nos solicitará o nome do usuario e o contrasinal para autenticarnos na Raspberry Pi.

` NOME DO USUARIO: Pi `

` CONTRASINAL: raspberryletty `


![raspi_1](doc/img/imaxes-raspbian/rasp15.png)


- Unha vez agregado, comprobamos que efectivamente nos conectamos remotamente dende o noso equipo de traballo a Raspberry Pi.


![raspi_1](doc/img/imaxes-raspbian/rasp16.png)








