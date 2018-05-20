## **Tema 3: La red de una granja web**    

**1. Buscar con qué órdenes de terminal o herramientas gráficas podemos configurar bajo Windows y bajo Linux el enrutamiento del tráfico de un servidor para pasar el tráfico desde una subred a otra.**


**Windows**

Windows Server proporciona una herramienta gráfica capaz de añadir a nuestro servidor la funcionalidad para realizar un NAT y poder enrutar el tráfico de una subred a otra. En la documentación oficial se explica de forma muy breve cómo crear paso a paso una configuración NAT en nuestro servidor, y enrutar el tráfico a una máquina u otra gracias a la herramienta Server Manager de Windows Server.

**Linux**

Para enrutar el tráfico en Linux, podemos usar route para crear nuestra NAT y poder redirigir el tráfico en nuestra máquina. 
Algunos comandos route podrían ser:

Para ver la tabla principal de direcciones:
`% route -n`

Para ver la tabla local de enrutamiento:
`% ip route show table local`

Para añadir una dirección a la tabla de direccionamiento:
`% ip route add 10.20.0.0/16 via 192.168.1.1`

Para añadir una dirección de direccionamiento por defecto:
`% ip route add 10.20.0.0/16 via 192.168.1.1`

Para crear una NAT para una red entera:
`% ip route add nat 205.206.207.32/29 via 192.168.1.32`
