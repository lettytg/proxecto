## CERTIFICADO E ACTIVACIÓN DO SSL.

- **SSL** é un estándar de seguridade global que permite a transferencia de datos cifrados entre un navegador e un servidor web.

- Para establecer esta conexión segura, instalase no servidor web un certificado SSL que cumpre estas dúas funcións:

    - Autenticar a identidade do sitio web, garantizando aos visitantes que no están nun sitio falso.
    - Cifrar a información transmitida.


- Procederemos a ir a nosa máquina e habilitaremos o módulo **rewrite** e **SSL** de Apache2.


![raspi_1](doc/img/imaxes-certi/certi1.png)


- Unha vez feito o anterior, instalaremos Certbot (que é un cliente ACME automático e fácil de utilizar, que obten certificados SSL/TLS gratis provistos por Let´s Encrypt).


![raspi_1](doc/img/imaxes-certi/certi7.png)


### CREACIÓN DO NOME DO DOMÍNIO.


- Agora procederemos a crear o novo nome do domínio en este caso **Invernao**, faremolo en FreeNom, xa que é un software que utilizamos anteriormente no módulo de Redes. 

- Para crear o nome teremonos que rexistrar na [páxina oficial](https://my.freenom.com/).


![raspi_1](doc/img/imaxes-certi/certi9.png)


- En este caso elexiremos o .ga e seleccionaremolo xa que é o único que está dispoñible.


![raspi_1](doc/img/imaxes-certi/certi8.png)


- Unha vez seleccionado, poderemos elexir, ata cando queremos ter o nome do domínio vixente, en este caso eu elexin 12 meses. 


![raspi_1](doc/img/imaxes-certi/certi10.png)


- Agora ca conta poderemos administrar o noso domínio. Engadiremos a IP pública do noso router para redireccionar o tráfico.


![raspi_1](doc/img/imaxes-certi/certi11.png)


- Unha vez realizados os pasos anteriores executaremos o seguinte comando:


![raspi_1](doc/img/imaxes-certi/certi12.png)




