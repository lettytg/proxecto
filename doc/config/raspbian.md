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

`# ip a` (En este caso: 192.168.1.37/24 aínda que máis adiante quedaría a 192.168.1.33/24).

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


- Vamos a cambiar o idioma que por defecto ven en Inglés. Para iso iremos a **Preferencias > Configuración Raspberry Pi > Localización**.


![raspi_1](doc/img/imaxes-raspbian/rasp17.png)


### INSTALACIÓN DO VNC NO EQUIPO DE TRABALLO.


- Descargamos o VNC dende a súa [páxina oficial](https://www.realvnc.com/es/connect/download/viewer/).

- Unha vez descargado e instalado, abrimos o aplicativo.


![raspi_1](doc/img/imaxes-raspbian/rasp13.png)


- Para crear unha conexión iremos a **Arquivo > Nova conexión**:

` VNC SERVER: A ip da Raspberry Pi `

` NOME: O nome co que queremos que se garde a conexión `


![raspi_1](doc/img/imaxes-raspbian/rasp14.png)


- Seleccionamos aceptar e sairanos unha ventá que nos solicitará o nome do usuario e o contrasinal para autenticarnos na Raspberry Pi.

` NOME DO USUARIO: Pi `

` CONTRASINAL: raspberryletty `


![raspi_1](doc/img/imaxes-raspbian/rasp15.png)


- Unha vez agregado, comprobamos que efectivamente nos conectamos remotamente dende o noso equipo de traballo a Raspberry Pi.


![raspi_1](doc/img/imaxes-raspbian/rasp16.png)


## SECURIZACIÓN DO SISTEMA RASPBERRY PI OS.

- A securización nos sistemas é algo primordial para evitar riscos que poidan facer peligrar a estabilidade da rede e do noso equipo.

- Para facer que a Raspberry Pi sexa máis segura, cambiaremos o usuario, xa que todas as Raspberry veñen co nome
do usuraio predeterminado **pi**, realizando isto conseguirase que a nosa Raspberry sexa menos vulnerable a ataques.

- Engadiremos o usuario co seguinte comando:

`# adduser raspiad`

![raspi_1](doc/img/imaxes-raspbian/rasp18.png)


- Engadimos o usarios anteriormente creado a todos os grupos do sistema.


`# usermod -a -G adm,dialout,cdrom,sudo,audio,video,plugdev,games,users,input,netdev,gpio,i2c,spi raspiad`


- Comprobamos que se agregou correctamente nos ficheiros /etc/passwd e /etc/groups.


![raspi_1](doc/img/imaxes-raspbian/rasp19.png)


- Unha vez comprobado o anterior, cerraremos sesión co usuario **pi** e iniciaremos co usuario novo creado **raspiad**.

`# su - raspiad `


![raspi_1](doc/img/imaxes-raspbian/rasp20.png)


- Para eliminar o usuario **pi** primeiro teremos que eliminar todos os procesos que estean vinculados con este usuario.

`# sudo pkill -eu pi `


- A continuación eliminaremos o usuario:


`# sudo deluser --remove-home pi`


- Comprobamos que xa non hai resto do usuario pi no noso sistema.


`# cat /etc/passwd | grep ^pi `


![raspi_1](doc/img/imaxes-raspbian/rasp21.png)


- Instalaremos e configuraremos un cortafogos, en este caso UFW, sen un cortafogos activo, a nosa Raspberry Pi está exposta a recibir posibles 
ataques dende Internet (ou incluso dende outro ordenadores da rede local). O cortafogos permitenos vixiar os portos de comunicacións e controlar
todo o que entra na nosa máquina dende o exterior e tamén todo o que sae de ela hacia o exterior. En este caso elixo UFW, porque é máis fácil de configurar, de aí o seu nome "**uncomplicated firewall**".


`# apt install ufw  `


![raspi_1](doc/img/imaxes-raspbian/rasp22.png)


- Engadimos a seguinte regra, para abrir o porto 3426 para o servizo SSH.

- Activamos e verificamos o estado do cortafogos.


![raspi_1](doc/img/imaxes-raspbian/rasp23.png)


- Engadimos tamén a seguinte regra, para abrir o servizo en este caso non empregaremos porto senon o propio nome.

- Comprobamos o estado.


![raspi_1](doc/img/imaxes-raspbian/rasp24.png)


## ASEGURAR O SERVIDOR SSH.


- Se accedemos a Raspberry mediante SSH a través de Internet, deberíanos asegurar o servidor, xa que os intentos de acceso non 
autorizado aos servidores SSH son moi frecuentes. Vemos a continuación algúns parámetros que podemos modificar ou engadir para que o noso 
servidor SSH esté máis seguro.


- O primeiro que imos facer é entrar no ficheiro de configuración para realizar os cambios.


`# sudo nano /etc/ssh/sshd_config  `


- Unha das primeiras opcións que nos atopamos é a que indica o porto de acceso ao servidor, que por defecto é 22. Se o cambiamos por 3426,
dificultaremos que intenten acceder a nosa máquina.


`# Port 3426  `


- Outra opción que podemos modificar é a que indica a cantidade de minutos que a pantalla de **login** estará dispoñible para que o usuarios
se identifiquen. Pasado ese tempo, se non nos identificamos, a conexión cerrarase.


`# LoginGraceTime 1m `


- Para dificultar os ataques de forza bruta. A primeira opción indica o número máximo de erros permitidos a facer **login**. Se o 
sobrepasamos ese número, mostrarasenos unha mensaxe de erro e haberá que volver a empezar de novo. A segunda opción refirese ao número máximo
de conexións simultáneas por IP que permite o servidor.


`# MaxAuthTries 3 `

`# MaxSessions 3 `


- Tamén aseguraremonos de que non se acepten contrasinais vacíos ou en branco.


`# PasswordAuthentication yes `

`# PermitEmptyPasswords no `


- Se hai varios usuarios no sistema, podemos engadir tamén ao final do ficheiro de configuración unha opción para que só os usuarios especificados teñan acceso ao mesmo. 


`# AllowUsers raspiad `


- En esta opción poderemos denegar o acceso ao usuario root.


`# DenyUsers root `


![raspi_1](doc/img/imaxes-raspbian/rasp25.png)


- Comprobamos que podemos acceder dende o noso equipo a Raspberry por SSH a través do porto 3426.


![raspi_1](doc/img/imaxes-raspbian/rasp26.png)


![raspi_1](doc/img/imaxes-raspbian/rasp27.png)


![raspi_1](doc/img/imaxes-raspbian/rasp28.png)

