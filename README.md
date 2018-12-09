# Practica 11

## Instalación de WordPress con Bitnami.

La preparación de la maquina en el aws es igual que en la anterior practica.

Crear una máquina virtual en Amazon EC2.

La Amazon Machine Image (AMI) que vamos a seleccionar para esta práctica será la última versión de Ubuntu Server.

Cuando esté creando la instancia deberá configurar los puertos que estarán abiertos para poder conectarnos por SSH y para poder acceder por HTTP/HTTPS.

SSH (TCP)
HTTP (TCP)
HTTPS (TCP)
Crear un par de claves (pública y privada) para conectar por SSH con su instancia.

Realizar la instalación del módulo de WordPress de Bitnami sobre la máquina.


## Instalación del modulo de wordpress con bitnami.

Primero accedemos a la máquina por ssh.
```
ssh -i "123456.pem" ubuntu@ec2-52-91-32-81.compute-1.amazonaws.com
```
Vamos a meternos en la página de bitnami y vamos a buscar el wordpress acuerdo con la máquina que vamos a emplear,
cuando ya lo tengamos vamos a copiar la url y en el terminal ponemos el comando wget con la url:
```
wget https://bitnami.com/redirect/to/375342/bitnami-wordpress-5.0-1-linux-x64-installer.run
```
Al presionar enter se descargara el paquete de instalacion de wordpres por bitnami.
Tendremos que modificar los permisos del instalador con el comando:
```
chmod 755 bitnami-wordpress-5.0-1-linux-x64-installer.run
```
Y por ultimo lo ejecutamos:
```
sudo ./bitnami-wordpress-5.0-1-linux-x64-installer.run
```
En la instalación nos pedira varias cosas:
```
1º Seleccionar un idioma para el instalador.
2º Si queremos instalar varnish que le daremos un no.
3º Si queremos instalar phpmyadmin que le daremos a que si.
4º Confirmara si las opciones que hemos elegido son las correctas y le daremos a que si.
5º Confirmar directorio en el que se guardara nosotros cogeremos el pordefecto.
6º Nombre de usuario : el que queramos.
7º Direccion de e-mail : el que queramos.
8º Acceso: el que queramos.
9º Contraseña: la que queramos.Y confirmar contraseña.
10º Nombre del blog: el que queramos.
11º Si queremos configurar un soporte por correo que nosotros le daremos a que no.
12º Confirmar y continuar con la instalación.
13º Nos pedira lanzar Bitnami WordPress Stack: si.
```
Y ya hemos finalizado la instalacion.





