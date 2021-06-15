# INSTALACIÓN E CONFIGURACIÓN DE ARDUINO UNO.

- Instalamos o software de Arduino no equipo de traballo dende a [páxina oficial.](https://www.arduino.cc/en/software/)


![raspi_1](doc/img/imaxes-arduino/ardu1.png)
![raspi_1](doc/img/imaxes-arduino/ardu2.png)
![raspi_1](doc/img/imaxes-arduino/ardu3.png)
![raspi_1](doc/img/imaxes-arduino/ardu4.png)


- Abrimos o programa de Arduino e en **Ferramentas** seleccionamos **Porto: COM 4** que é donde está conectado o Arduino.


![raspi_1](doc/img/imaxes-arduino/ardu5.png)


- Para representar isto necesitaremos, unha placa Arduino UNO, un par de cables e un dispositivo de refrixeración, en este caso un ventilador.


![raspi_1](doc/img/imaxes-arduino/ardu7.png)


- Para realizar esta tarefa precisase enviar instruccións a Arduino para que haxa unha comunicación entre a placa, os sensores e o ventilador.



```
//Incluimos biblioteca para poder utilizar o DHT11
#include <DHT.h>
#include <DHT_U.h>

//Asignamos nome dos pins de Arduino a utilizar
const int ventilador=3;
const int sensorDHT=A2;

//Declaramos 2 variables tipo para almacenar os datos lidos do sensor
int temp, humidade;

//Asignamoslle un nome ao noso obxecto
DHT dht (sensorDHT,DHT11);

//Configuaraciòn inicial da Tarxeta Arduino
void setup(){
  Serial.begin(9600); //Iniciamos comunicaciòn co PC a 9600 Batios
  pinMode(ventilador,OUTPUT); //Indicamoslle que o ventilador (pin 8) será de saída
  dht.begin(); //Iniciamos o sensor DHT11
  }

void loop(){
      humidade= dht.readHumidity(); //Funcion incluida na libreria. Permite leer a humidade
      temp= dht.readTemperature(); //Permite leer a temperatura


      //Imprime por pantalla os datos leidos
      Serial.print("Temperatura: ");
      Serial.print(temp);
      Serial.println("ºC"); //Tempertura: 27ºC
      Serial.print("Humidade: ");
      Serial.print(humidade);
      Serial.print("%");
      Serial.println(" ");
      Serial.println(" ");

      //Pausa de 1 segundo para ver os datos.
      delay(1000);

      if (temp>=27){ //Temperatura maior a 27.
        Serial.println("Ventiladores encendidos");
        digitalWrite(ventilador,HIGH); //Encendemos o ventilador
        temp= dht.readTemperature(); //Volvemos a leer a temperatura
        delay(10000);
        }

        digitalWrite(ventilador,LOW);

  }

  
```

- Para que isto funcione, necesitamos unhas librerías do propio sensor, en este caso descarguei a librería da seguinte [páxina](https://codeload.github.com/adafruit/Adafruit_Sensor/zip/refs/heads/master)


![raspi_1](doc/img/imaxes-arduino/ardu12.png)


- Unha vez realizado o código, procedemos a compilar o programa para así entregarlle a información necesaria.


![raspi_1](doc/img/imaxes-arduino/ardu10.png)


- Seleccionamos "**Subir**" e comprobamos que se está subindo o código a placa.

![raspi_1](doc/img/imaxes-arduino/ardu11.png)


- Unha vez subido comprobaremos no propio terminal da aplicación que está a funcionar o sensor e o ventilador.


![raspi_1](doc/img/imaxes-arduino/ardux.PNG)







