# SWAP1718
####Javier Prieto Infante 3º GII TIC Grupo2
## **Práctica1 : Preparación de las herramientas**    
***
El objetivo de la práctica1 es configurar dos máquinas (servidores) con Ubuntu Server para trabajar en prácticas posteriores.     

Para ello lo que he hecho ha sido la instalación de dos máquinas Ubuntu Server en VirtualBox, con las opciones de servidor LAMP (Apache,MySQL,PHP) y SSH.    

Y a las cuales he llamado:    
- ubuntuserver1     
- ubuntuserver2   

A ambas máquinas desde virtual box hay que añadirle 
un nuevo adaptador de red con la configuración de red interna. Las dos máquinas virtuales creadas tienen el mismo nombre de red interna. (intnet)

Como resultado en cada máquina aparecen dos interfaces de red:
- enp0s3 -> NAT   
- enp0s8 -> RED INTERNA

Despues he asignado la IP fija a la interfaz enp0s8.   
Mediante : `sudo nano /etc/network/interfaces` 

![Configuracion de red](/practica1/imagenes/etc-network-interfaces.png)

Una vez hecho este cambio debemos reiniciar y obtendremos las siguientes interfaces de red.    
Haciendo: `ifconfig -a`

![Interfaces de red](/practica1/imagenes/ifconfig.png)

Una vez instalado los servidores y cambiadas la configuración de su red, comprobamos la versión del servidor y que apache está ejecutandose:

![Apache](/practica1/imagenes/apache.png)

Para ver que Apache está funcionando, usando un editor de texto plano, crearemos el archivo HTML llamado hola.html en el directorio /var/www/html. Y mediante curl accedemos a el.

![cURL](/practica1/imagenes/curl.png)

Como en la instalación indicamos la instalación de SSH, a continuación muestro la conexión entre máquinas mediante SSH (de una máquina a la otra):

![SSH](/practica1/imagenes/ssh.png)

