# FASE DE DESEÑO

## ARDUINO UNO

- Diagrama de compoñentes de Arduino UNO.


![raspi_1](doc/img/imaxes-deseno/dese1.png)


En este digrama podemos contemplar que estarán conectados un sensor de temperatura DHT11 e un ventilador a nosa placa Arduino (que é unha placa con todos os elementos necesarios para conectar periféricos nas entradas e saídas de un microcontrolador, e que pode ser programada tanto en Windows como macOS e GNU/Linux)

- Compoñentes conectados a Arduino UNO:

    1. SENSOR DHT11

        - Sensor digital de temperatura e humidade relativa. Integra un sensor de humidade e un termistor para medir o aire circundante, e os datos mediante o pin de datos.

    ![raspi_1](doc/img/imaxes-deseno/dese2.png)

        - PIN 1: O pin 1 irá conectado a entrada GND da placa Arduino, que é a toma terra.
        - PIN 2: O pin 2 irá conectado a entrada 5V da placa Arduino, que será a alimentación do noso sensor.
        - PIN 3: O pin 3 irá conectado a entrada analóxica (A2), que será a entrada de datos.

    2. VENTILADOR

    ![raspi_1](doc/img/imaxes-deseno/dese3.png)

        - PIN 1: O pin 1 irá conectado a GND (toma terra.)
        - PIN 2: O pin 2 irá conectado a (-3) que será alimentación.

## RASPBERRY PI 3 MODEL B


- Diagrama de compoñentes da Raspberry PI.


 ![raspi_1](doc/img/imaxes-deseno/dese4.png)


A Raspberry Pi consiste nunha placa base que soporta distintos compoñentes de un ordenador como un procesador ARM de hasta 1500 MHz, un chip gráfico e unha memoria RAM de ata 8 GB.

Ademáis, ten moitas máis cualidade por exemplo:

    1. Permite conectar dispositivos periféricos grazas aos seus portos (HDMI, USB). Por exemplo, unha pantalla, teclado, rato.

    2. Conten un procesador gráfico VideoCoreIV, co que permite a reproducción de vídeo -incluso en alta definición-.

    3. Permite a conexión a rede a través do porto de Ethernet, e permite conexión Wifi e Bluetooth. Consta de una ranura SD que permite instalar, a través de una tarjeta microSD, sistemas operativos libres.


En este caso, na nosa Raspberry Pi, teremos conectado o cable de rede ao porto Ethernet, unha saída de son e vídio no porto HDMI, a nosa MicroSD de 64GB co sistema Raspbian e finalmente a nosa placa de Arduino mediante o porto USB.


## DIAGRAMA DE COMPOÑENTES DO SISTEMA ZABBIX 5.4.


- Na seguinte imaxe poderemos ver os compoñentes de Zabbix 5.4:

 ![raspi_1](doc/img/imaxes-deseno/dese6.png)




## DIAGRAMA DA REDE 

- En este diagrama poderemos ver como está montada a rede do proxecto.


 ![raspi_1](doc/img/imaxes-deseno/dese5.png)


Como podemos ver, temos a nosa Raspberry Pi actuando de servidor, xa que en el vai estar o sistema de monitorización, o cal poderemos acceder dende Internet, xa que se fixo un reenvío de portos para acceder a mesma.

Conectado a Raspberry irá o Arduino, o cal estará programada para recoller a información do sensor e mandar instrucción ao ventilador que se ubicarán no invernadorio, que posteriormente monitorizaremos co Zabbix.





















## Modelo conceptual do dominio da aplicación e/ou Diagrama de clases [usando UML, ConML, ou linguaxe semellante].

## Casos de uso [descritos en fichas e/ou mediante esquemas; deben incluír os actores (tipos de usuarios) implicados en cada caso de uso].

## Deseño de interface de usuarios [mockups ou diagramas...].

## Diseño de interfaxes software e hardware (se aplica)

## Diagrama de Base de Datos.

## Diagrama de compoñentes software que constitúen o produto e de despregue.

## Diagrama de despregamento

## Outros diagramas, esquemas ou documentacion (seguridade, redundancia, expliacións, configuracións...)

