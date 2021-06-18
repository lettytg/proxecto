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
 
- Configuración do Zabbix, para que poida monitorizar os valores recollidos polo sensor de temperatura e humidade DHT11, e monitorizar o propio servidor e ver o estado no que se encontra.
 
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

    - Recursos hardware: Servomotor + Aspas do ventilador.


### Diagrama de Gantt

- O diagrama de Gantt é unha metodoloxía de representación de actividades ou tarefas que pretende dar unha visión xeneralizada sobre o tempo dedicado a cada actividade contemplada de forma independente dentro de un proceso. 
- En este caso utilizaremos o aplicativo de GanttProject.

![raspi_1](doc/img/imaxes-planificacion/diagramadeGantt.png)


## Orzamento do proxecto.

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

### Orzamento da creción da empresa.

#### Trámites necesarios

En este caso crearemos unha Sociedade Limitada Unipersoal que é unha forma xurídica que cada vez elixen máis os emprendedores.

Funciona igual que unha Sociedade Limita Unipersoal, coa única diferencia de que todas as responsabilidades e os beneficios recaen sobre ti.

- **Características da Socieade Limitada Unipersoal**:

    - O capital mínimo é de 3000 euros, ao igual que en unha SL.
    - Aínda que sexas socio único, terá que deixar constancia das xuntas xerais nunha acta ca túa firma ou a do teu respresentante.
    - Terás que presentar os seguintes libros: a diario, o balance, o PyG, as actas e o rexistro de contratos da SLU para contigo mesmo.
    
Os pasos para constituir a SLU son os mesmos que na SL pero con lixeiras variacións.

- **Pasos para constituir unha Sociedade Limitada Unipersonal**:

1.** Rexistrar o nome da SLU**.

A denominación social da empresa é un dos papeis que che exesirá o notario para constituir a sociedade.

A denominación social teñen eficacia xurídica e é por tanto o nome "oficial" da sociedade. Este nome non ten por qué ser o mesmo que o nome comercial.

2.** Determinar o Capital Social**.

O capital social é a aportación que deberás facer para constituir a sociedade.

    - Canto capital social aporto?

        A aportación debe ter un valor mínimo de 3000 euros para poder crear a SLU, pero se temos unha estrutura de gastos importante recomendase por máis de 3000 euros para iniciar a túa actividade.

        Hai que ter en conta que os 3000 euros van a ser os que soporten os gastos ata que consigamos as ventas suficientes para cubrilos.


3. **Definir o Obxeto Social**.

O obxeto social é a definición da actividade que vai a desenrrolar na SLU. O obxeto social deberemos indicalo posteriormente nos estatutos sociais.

Ao redactar a actividade que vamos a desenrrolar teremos que indicar tamén o CNAE (Código Nacional de Actividades Económicas) ao que fai referencia a túa actividade.


4. **Establecer o Dominio Social**.

O dominio social que vaiamos a indicar para a SLU pode ser calquera de estos dous:

    - O lugar onde se desenrrole a actividade principal.
    - O lugar onde se desenrole a dirección e administración da mesma.

5. **Establece os estatutos sociais**.

O estatuto social comprende as normas que van a regular o funcionamento da sociedade.

Deberemos indicar o estatuto os seguintes puntos:

    - O obxeto social.
    - A denominación da sociedade.
    - O dominio social.
    - O capital social.
    - A capacidade, dereitos e deberes dos socios (en este caso só eu).
    - A regulación do órgano de administración.
    - A relación da sociedade cos socios (en este caso eu)

6. **Abrir unha conta bancaria e conseguir o certificado das aportacións**.

Elixir un banco, abrir unha conta e ingresa o capital social.

O certificado de aportacións darao o banco no que ingreses o capital social.

Pode ser que o banco tarde en emitir este certificado se o diñeiro se ingresa mediante transferencia.


7. **Solicitar o CIF Provisional do SLU**.

De ese paso encargarase no 99% das veces o notario, pero é importante que se sepa da súa existencia para fixarte se o teu notario o solicitou ou non.

O CIF Provisional é o número de identificación que se ofrecerá e que poderás convertir nun CIF Definitivo unha vez teñamos a escritura rexistrada no Rexistro Mercantil.

8. **Realizar a escritura da constitución**.

En este paso só temos que preocuparnos de ir ao notario e él realizará o trámite.

Os documentos que serán necesarios para construir a SLU son:

    - Estatuos sociais.
    - Certificado do Rexistro Mercantil de reserva de denominación social.
    - Certificado de aportacións do Banco.

9. **Inscribir a escritura no Rexistro Mercantil**.

Na maioría dos casos tamén encargarase o notario de remitir telemáticamente a escritura ao Rexistro Mercantil. Para validar a escritura o rexistro deberá marcala con un selo. Por tatno, aseguremonos de que a escritura que se garde sexa a que teña selo xa que as outras non teñen efectos.

10. Obter a acta de titularidade real da SLU.

A acta 























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





