# EXTRACIÓN DOS VALORES DO SENSOR A RASPBERRY PI


- Agora vamos a proceder a extraer os valores do noso sensor que está conectado no Arduino. Para iso necesitaremos crear un script no cal recolla a información do porto onde está conectado o Arduino, é dicir, **/dev/ttyACM0**. 

- Crearemos un script en Python, para poder realizar isto necesitaremos unhas librerías de Python chamadas **Python-Serial** que é a que nos permitirá comunicarse ao porto serial e permitiranos extraer estos valores.

`sudo apt-get install python-serial`

```
import serial

serial_port = '/dev/ttyACM0'; //Establecese o porto da conexión.
baud_rate = 9600; /Establece a velocidad de datos en bits por segundo (baudios) para a transmisión de datos en serial.
write_to_file_path = "/home/raspiad/Documentos/info3.txt"; //Crea o arquivo info3.txt

output_file = open(write_to_file_path, "w+"); 
ser = serial.Serial(serial_port, baud_rate)
while True:
    line = ser.readline();
    line = line.decode('utf-8');
    print(line);
    output_file.write(line);
```



