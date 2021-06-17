# Monitorización de invernadoiro con Zabbix.

## Descripción

O proxecto consiste en crear un mecanismo de monitorización e control de temperatura e humidade para os cultivos do invernadoiro.

A idea sería crear unha infraestrutura na cal poidamos mellorar a calidade dos nosos cultivos, de unha maneira automática e desatendida para o usuario encargado, para iso teríamos que levar un control da temperatura e humidade do invernadoiro. 
Para controlar isto necesitaríamos un microordenador como por exemplo unha Raspberry Pi, un sensor que leve o control ambiental e un dispositivo hardware para a súa ventilación.

Para abarcar todo o mencionado, necesitaremos un sistema de tempo real que controle a cantidade de temperatura e humidade do invernadoiro, en este utilizaríamos Zabbix.

Zabbix permitiranos recompilar información dos sensores que irán conectados a placa que enviarán ordes aos dispositivos de ventilación.

## Instalación / Puesta en marcha

> Ver [Implantación]((doc/templates/6_implantacion.md))

## Uso

> *TODO*: Es este apartado describe brevemente cómo se usará el software que proyectas. Si tiene una interfaz de terminal, describe aquí su sintaxis. Si tiene una interfaz gráfica de usuario, describe aquí **sólo el uso** (a modo de sumario) **de los aspectos más relevantes de su funcionamiento** (máxima brevedad, como si fuese un anuncio reclamo o comercial).
> Si tu proyecto es documental, realiza una especificación de cómo planteas estas interfaces, con ejemplos incluso o esquemas de diseño. En otras palabras, realiza este apartado independientemente que no haya implementación.

## Sobre o autor

O meu nome é Leticia Tuñas García, son Técnico en Sistemas Microinformáticos e Redes (SMR), actualmente estudo Administración de Sistemas Informáticos en Rede, 
estou desarrollando este mesmo proxecto e traballando na empresa na que estou realizando as prácticas. Ao mesmo tempo tamén estou estudando o primeiro ano de Desenrolo de Aplicacións Multiplataforma.

Este proxecto é unha oportunidade para poder ver un sistema de monitorización implantado nunha infraestrutura pouco común, como é un invernadoiro.

Todo isto xurde como unha inquietude, xa que durante os anos cursados, nunca nos adentramos no mundo da monitorización, por iso, con este proxecto espero levar unha gran aprendizaxe.


## Licenza

En termos de licenza, autorizase a distribución, copia e modificación do documento baixo os termos da Licenza de Documentación libre GNU, versión 1.3, 
ou calquera outra que posteriormente publique a Fundación para o Software Libre, sen seccións invariantes, textos de portada, nin texto de contraportada.

## Índice

> *TODO*: Simplemente indexa ordenadamente todo tu proyecto.

1. Anteproxecto
    * 1.1. [Idea](doc/templates/1_idea.md)
    * 1.2. [Necesidades](doc/templates/2_necesidades.md)
2. [Análises](doc/templates/3_analise.md)
3. [Planificación](doc/templates/4_planificacion.md)
4. [Deseño](doc/templates/5_deseño.md)
5. Implantación

    5.1. [INSTALACIÓN E CONFIGURACIÓN DE RASPBERRY PI OS](doc/config/raspbian.md)

    5.2. [INSTALACIÓN E CONFIGURACIÓN DE ZABBIX PARA RASPBERRY PI OS](doc/config/zabbix.md)

    5.3. [NOTIFICACIÓNS DE ALERTAS POR CORREO](doc/config/correo.md)

    5.4. [CERTIFICADO E ACTIVACIÓN DO SSL](doc/config/certi.md)

    5.5. [APERTURAS DE PORTOS DO ROUTER E FIREWALL](doc/config/portos.md)

    5.6. [INSTALACIÓN E CONFIGURACIÓN DE ARDUINO UNO](doc/config/arduino.md)

    5.7. [INSTALACIÓN DO IDE ARDUINO EN RASPBERRY PI](doc/config/arduino1.md)

    5.8. [EXTRACIÓN DOS VALORES DO SENSOR A RASPBERRY PI](doc/config/valores.md)

    5.9. [MONITORIZACIÓN DO SENSOR DE TEMPERATURA CON ZABBIX](doc/config/monitorizacion.md)

## Guía de contribución

Todas as ferramentas software que son empregadas en este proxecto son de software libre e de código aberto, con isto teremos a liberdade de executar os programas cando desexemos, con calquera proposito, a liberdade de estudar como é o funcionamento de cada un de eles 

## Enlaces 

** Enlaces de descarga


