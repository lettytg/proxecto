# APERTURA DE PORTOS EN ROUTER E FIREWALL


- Antes de abrir os portos, configuraremos o firewall UFW da Raspberry PI, para permitir a conexión por http.
- Executar este comando é equivalente a habilitar o porto 80.


![raspi_1](doc/img/imaxes-portos/porto2.png)


- Agora procederemos a abrir os portos do noso router, en este caso o operador é Movistar. 
- Poderemos acceder dende o navegador utilizando a IP do noso router. Unha vez accedidos, haberá que agregar o nome do usuario e contrasinal para poder administrar o router.


![raspi_1](doc/img/imaxes-portos/porto0.png)


- Unha vez feito isto, seleccionaremos "Configurar aplicacións e portos".

- Aquí abriremos os portos correspondentes para HTTP (80) e HTTPS (443). 


![raspi_1](doc/img/imaxes-portos/porto1.png)


- Comprobamos que podemos acceder co nome do dominio por HTTPS.


![raspi_1](doc/img/imaxes-portos/porto11.png)



