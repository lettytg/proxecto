# FASE DE PLANIFICACIÓN DO PROXECTO

## Obxectivos do proxecto

## Guía de planificación do proxecto

### Metodoloxía

### Fases planificadas

Descríbense as fases en que se divide o proxecto e as tarefas que se han levar a cabo en cada unha destas fases.
Pódense indicar os recursos materiais e humanos asociados a cada tarefa ou, se son os mesmos, de maneira máis xeral.

#### Fase 1: Análise do entorno de imprantación.

##### Tarefa 1: Desprazamentos as dependencias do cliente. 

- Desprazaremonos ao lugar onde se ubica o invernadoiro do cliente.
- Recursos necesarios: Medio de transporte.

##### Tarefa 2: Análise do marco de traballo.

- Avaliaremos as necesidades do cliente. Unha vez recopilada a información procedemos á planificación do proxecto.

#### Fase 2: Configuración do núcleo do proxecto.

##### Tarefa 1: (se se da o caso): Montaxe do invernadoiro.

- No caso de que o cliente non dispoña do invernadoiro, ofreceremoslle a posibilidade de realizar a montaxe da infraestrutura

##### Tarefa 2: Instalación e configuración da Raspberry PI.

- Instalaremos o SO na MiscroSD da Raspberry PI e realizarase unha configuración básica da mesma.

- Recursos hardware/software necesarios:

    - Raspberry Pi 3 B+.
    - Carcasa para a praca Raspberry Pi.
    - Arduino UNO.
    - Carcasa para o Urduino UNO.
    - Ferramentas para a montaxe de ambas pracas.
    - Imaxe do sistema operativo (Raspberry Pi OS)

#### Fase 3: Instalación do software para a monitorización: Zabbix.

##### Tarefa 1: Instalación de Zabbix.

- Instalación do Zabbix, executando os pasos no [punto 5.2](doc/config/zabbix.md).

- Recursos hardware/software:

    - Hardware: Raspberry PI.
    - Software: Zabbix.

##### Tarefa 2: Configuración do Zabbix.
 
Configuración do Zabbix, para que poida monitorizar os valores recollidos polo sensor de temperatura e humidade DHT11, e monitorizar o propio servidor e ver o estado no que se encontra.
 
#### Fase 4: Configuración do Arduino UNO.

##### Tarefa 1: Instalación de IDE de Arduino.

- Realizar a instalación do IDE para poder controlar mediante código o Arduino.

- Recursos hardware/software:

    - Hardware: Arduino UNO.
    - Sofware: Arduino IDE.

##### Tarefa 2: Instalación do sensor de temperatura e humidade.
 
- Realizar a instalación do sensor de temperatura e humidade DHT11.

- Recursos hardware/software:

    -  Recursos hardware: Sensor DHT11.

##### Tarefa 3: Instalación do sistema de refrixeración.
 
- Realizar a instalación do ventilador.

- Recursos hardware/software:

    - Recursos hardware: Servomotor + Aspas de ventilador


### Diagrama de Gantt

- O diagrama de Gantt é unha metodoloxía de representación de actividades ou tarefas que pretende dar unha visión xeneralizada sobre o tempo dedicado a cada actividade contemplada de forma independente dentro de un proceso. 
- En este caso utilizaremos o aplicativo de GanttProject.

![raspi_1](doc/img/imaxes-planificacion/diagramadeGantt.png)


## Orzamento

| MATERIAL| IMPORTE|
|--|--|
| Raspberry Pi 3 B+ | 36,95 € 
| Arduino UNO | 22,90 € 
| Tarxeta MicroSD | 9,00 €
| Carcasa para Raspberry Pi | 12,00 €
| Kit de sensor de temperatura e humidade, cables e servomotor | 15,00 € 

| TOTAL | PROXECTO | 
|--|--|
| -- | 95,85 € |

### Orzamento por actividade

| ACTIVIDADE | DURACIÓN | CUSTO (EUROS) | | CUSTO TOTAL ACTIVIDADE |
|--|--|--|--|--|
|            |          | PERSOAS|RECURSOS MATERIAIS|
|||||
|||||
|||||
|||||

| TOTAL | PROXECTO | 
| -- | -- |

### Orzamento por partidas de inversión / gasto:

| CONCEPTO | IMPORTE|
|--|--|
|**A) INVERSIONS**
|Gastos de establecemento e gastos de constitución
|Total inmobilizacións inmateriais
|Terreos
|Construcións
|Instalacións técnicas
|Maquinaria
|Ferramentas
|Mobiliario e instalacións
|Equipos informáticos
|Elementos de transporte
|Outro inmobilizado material
|Total inmobilizacións materiais
|Outros gastos a distribuír en varios exercicios
|**TOTAL INVERSIÓNS:**
|**B) GASTOS**
|Compras de materiais
|Arrendamentos
|Publicidade, propaganda e relacións públicas
|Persoal
|Reparacións e conservación
|Servizos de profesionais independentes
|Outros gastos xerais
|Gastos financeiros
|Amortizacións
|Gastos de xestión e administración
|**TOTAL GASTOS:**

|TOTAL ORZAMENTO:
|--|

### WEBGRAFÍA
Guía para a elaboración de proyectos. Gobierno Vasco.
https://www.pluralismoyconvivencia.es/upload/19/71/guia_elaboracion_proyectos_c.pdf  (páxina 49 e seguintes)



