# REQUIRIMENTOS DO SISTEMA

Este documento describe os requirimentos para Invernao especificando que funcionalidade ofrecerá e de que xeito.

## Descrición Xeral


O proxecto consiste en crear un invernadoiro automatizado, xa que nos da un nivel de independencia moi grande, porque poden operar, de forma autónama, sen necesidade da presenza do productor de forma permanente no sitio. Aforrase tempo de traballo, xa que é o encargado de realizar algunhas de esas tarefas que se requiren para o seu bo funcionamento. 

O invernadoiro sería controlado por un sistema de monitorización o cal nos avisaría vía e-mail se se xera algunha alerta no noso sistema.


## Funcionalidades


Exemplo:
 1. A aplicación web debe permitir controlar o acceso ao sistema a través do usuario e password.
 2. O sistema debe permitir monitorizar o estado dos sensores, en este caso de temperatura e humidade.
 3. O sistema debe permitir visualizar a través da páxina de Zabbix unha gráfica cas diferentes lecturas rexistradas polo sensor de temperatura.
 
## Requerimentos non funcionais

  1. O sistema debe procesar os datos en liña e de forma rápida.
  2. O sistema debe mostrar mensaxes de erros de unha forma clara, que permita ao usuario comprendelos fácilemente.
  3. O sistema debe ter unha interface amigable para o usuario.

## Tipos de usuarios


Tipos de usuario que poderán acceder ó noso sistema. Poderán diferenciarse polos permisos sobre os datos, pantallas que se lles amosan, operacións que poden levar a cabo, etc.

Usuarios do sistema Raspbian:

- **Usuario administrador:** responsable da administración e configuración de todo o sistema, é o único que ten permisos para engadir novos usuarios, instalar aplicacións, etc.
- **Usuario estándar:** só poderá acceder a certas carpetas e arquivos.

Usuario do sistema de monitorización Zabbix:

- **Usuario administrador:** é o usuario que ten todos os permisos da aplicación.
- **Usuario estándar:** é o usuario que tería permisos para a visualización do contido da aplicación pero non para a súa moddificación, é dicir, sería o usuario que tería o cliente para ter acceso e poder visualizar a monitorización.

## Avaliación da viabilidade técnica do proxecto


### Hardware requerido


- **RASPBERRY PI 3B +** 


![raspi_1](doc/img/imaxes-analise/analise1.png)


- CARACTERÍSTICAS:

  - CPU + GPU: Broadcom BCM2837B0, Cortex-A53 (ARMv8) 64-bit SoC @ 1.4GHz.
  - RAM: 1GB LPDDR2 SDRAM.
  - Wi-Fi + Bluetooth.
  - Ethernet: Gigabit Ethernet sobre USB 2.0 (300 Mbps).
  - HDMI.
  - 4 portos USB 2.0.
  - Puerto CSI para conectar unHa cámara.
  - Puerto DSI para conectar unHa pantalla táctil.
  - Saída de audio estéreo e vídeo composto.
  - Micro-SD.
  - Power-over-Ethernet (PoE).


- Imaxes da Raspberry PI que estou a utilizar:


  - Parte de arriba da Raspberry:


![raspi_1](doc/img/imaxes-analise/analise2.png)


  - Parte inferior da Raspberry:


![raspi_1](doc/img/imaxes-analise/analise3.png)


  - Parte lateral, onde se encontran os portos USB e o cable de rede conectado ao porto Ethernet.


 ![raspi_1](doc/img/imaxes-analise/analise4.png)
 

  - Parte lateral, onde se encontra o cable de alimentación e a saída de vídeo conectada ao porto HDMI.


![raspi_1](doc/img/imaxes-analise/analise5.png)


- **ARDUINO UNO**


![raspi_1](doc/img/imaxes-analise/analise8.png)


- CARACTERÍSTICAS:

  - Microcontrolador: ATmega328
  - Voltaxe Operativo: 5v
  - Voltaxe de Entrada (Recomendado): 7 – 12 v
  - Pines de Entradas/Saídas Dixital: 14.
  - Pines de Entradas Análogas: 6
  - Memoria Flash: 32 KB (ATmega328).
  - SRAM: 2 KB (ATmega328)
  - EEPROM: 1 KB (ATmega328)
  - Velocidade de Reloxo: 16 MHZ.


- Imaxes do Arduino UNO que estou a utilizar:


![raspi_1](doc/img/imaxes-analise/analise6.png)


![raspi_1](doc/img/imaxes-analise/analise7.png)


### Software

Analizar as opcións software existentes e xustificar a idoneidade dos compoñentes seleccionados.

#### RASPBERRY PI OS 


**Raspberry Pi OS** é unha distribución do sistema operativo GNU/Linux basado en Debian, e polo tanto libre para a SBC Raspberry Pi, orientado a enseñanza de informática. É o sistema operativo por excelencia e case por defecto para a Raspberry Pi. Detrás do sistema están os mesmos creadores da placa de desarrollo. O lanzamento inicial foi en Xuño do 2012, e a última versión estable foi liberada o 3 de Abril.
Podemos obter a imaxe dende a súa [páxina oficial](https://www.raspberrypi.org/software/operating-systems/)

![raspi_1](doc/img/imaxes-analise/analise9.png)


#### ZABBIX 5.4


**Zabbix 5.4** é un Sistema de Monitorización de Redes. Está deseñado para monitorizar e rexistrar o estado de varios servizos de rede, servidores e hardware de rede. Usa MySQL, PostgreSQL, SQLite, Oracle ou IBM DB" como base de datos. O seu backend está escrito en C e o frontend web está en PHP. Etos sistemas de monitoreo principalmente usanse para poder visualizar de maneira gráfica e rápida nunha liña de tempo o seu desempeño. Os sistema de monitoreo rexistran diferente información, como límites, parámetros e eventos importnates, utilizando contadores virtuais. De esta maneira podese chegar a ráìdas conclusión que axudan a identificar condicións críticas, moderas ou lixeria que requiren de atención oportuna pola parte da persoas que o están utilizando.

Elixo Zabbix xa que a parte de ser unha ferramenta de software libre, ofrece un gran rendemento para a recopilación de datos e podese escalar a entornos moitp máis grandes.


![raspi_1](doc/img/imaxes-analise/analise10.jpg)



## Análise de riscos e interesados





## Actividades

Definir, de forma xeral, os pasos que se han seguir para levar a cabo o proxecto, de forma que na fase de planificación nos sirvan como referencia para detallar as tarefas, recursos e temporalización necesaria para cada fase.

1. Análise do entorno no que imos imprantar o sistema.
2. Recollida de información sobre o sistema que queremos despregar.
3. Escolla dos produtos que imos a empregar.
4. Instalación e configuración de Raspberry Pi OS.
5. Securización da Raspberry Pi.
6. Instalación e configuración de Arduino UNO.
7. Instalación e configuración de Zabbix 5.4.
8. Monitorización do sensor de temperatura en Zabbix.
9. Nome do dominio e reenvío de portos.


## Melloras futuras

Este proxecto está centrado en cubrir unha necesidade que a meirande parte da xente que se adica a isto non se pode permitir. Nun futuro gustaríame engadir máis funcionalidades, como por exemplo:

- Integrar un sistema automático de rego, para complementar o sistema de refrixeración que temos (ventilador)
- Creación de unha aplicación móbil que xestione de forma manual todos os compoñentes do invernadoiro.
