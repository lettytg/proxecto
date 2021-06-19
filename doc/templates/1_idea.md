# Idea

Este proxecto xurde como unha necesidade que me gustaría imprantar no invernadoiro que teño na casa, xa que me gustaría automatizar máis os labores que leva manter un invernadoiro. Como ben sabemos, un invernadoiro necesita persoal que estea pendente todos os días de que a produción non se vexa danada polos cambios de tempo durante o día. Con esta imprantación teríamos moitas vantaxes, xa que teríamos un mallor control da producción e un liberamento de carga de traballo para o persoal que se dedica ao mantemento do invernadoiro. 

Existen moitas empresas que ofrecen unha solución para que esta idea que prantexo, só que o custe é moi elevado, e a meirande parte da xente non dispon de medios para pagar estes servizos.

Por iso propoño crear un sistema que contará con unha serie de sensores e actuadores que irán conectados en Arduino, para que se poida facer efectivo a manipulación do medio ambiente da pranta para o seu cultivo e finalmente o seu consumo. Para iso teríamos unha serie de sensores, en este caso de temperatura e humidade e unha serie de actuadores en este caso un ventilador para baixar a temperatura e tamén airear o interior.

No proxecto utilizaremos un sistema de monitorización (Zabbix) que irá imprantado na Raspberry Pi, decidín facelo nunha Raspberry Pi xa que sempre quixen invertigar o funcionamento da mesma pero nunca tiven oportunidade, igualmente a instalación do sistema de monitorización tamén se podería realizar nunha máquina virtual en calquera dos sistemas de (GNU/Linux).

En este caso utilizarase unha Raspberry Pi 3 B+, un Arduino UNO, un sensor de temperatura e ventilador. Isto poderíase ampliar, agregando un sistema de rego automatizado, un panel de leds para a iluminación, un humidifacador para a humidade relativa do entorno e un sensor de humidade para controlar a humidade do terreno onde se encontran as prantas.


O software que se utilizaría sería:

- Sistema Operativo: Raspberry PI OS. 
- Software de monitorización: Zabbix para Raspberry PI OS.
- Aplicación de Arduino Uno: Arduino Software IDE.
- Securización da rede: Firewall UFW e Fail2ban. 
