## **Tema 5: Medir prestaciones**    

**1. Buscar información sobre cómo calcular el número de conexiones por segundo.**

En el caso de nginx esto es muy fácil de hacer ya que trae un módulo que se encarga de realizar estadísticas sobre las conexiones a nuestra máquina.

Para ello, tendremos que añadir a nuestro fichero de configuración `nginx.conf` lo siguiente:

    location /nginx_status {
    	# Turn on stats
    	stub_status on;
    	access_log   off;
      	# only allow access from 192.168.1.5 #
     	allow 192.168.1.5;
	deny all;
    }

Tras esto, reiniciamos el servicio:
`service nginx reload`

Y accedemos a la siguiente url: `http://direccion_ip/nginx_status` y nos indicará el número de conexiones abiertas, el número de conexiones aceptadas, las que ha manejado y las conexiones que está manejando.

*** 

**3. Buscar información sobre características, disponibilidad para diversos SO, etc de herramientas para monitorizar las prestaciones de un servidor. Para empezar, podemos comenzar utilizando las clásicas de Linux:**

- **top**
- **vmstat**
- **netstat**


- `top:` esta herramienta nos ofrece un monitor en tiempo real sobre las características del sistema. La pantalla que muestra por defecto al ejecutar la orden es un monitor general del estado de nuestra máquina. En función de los parámetros que introduzcamos, podemos cambiar la pantalla de monitorización de top. Estos comandos los podemos ver ejecutando man top o bien acceder a [https://linux.die.net/man/1/top](https://linux.die.net/man/1/top)

- `vmstat:` vmstat (virtual memory statistics) nos ofrece información sobre los procesos en ejecución, del estado de la memoria, paginación, etc, dependiendo de la opción que introduzcamos. Estas opciones, al igual que antes están disponibles en el man o en [https://linux.die.net/man/8/vmstat](https://linux.die.net/man/8/vmstat)

- `netstat:` netstat imprime información sobre conexiones de red, tablas de enrutamiento, estadísticas sobre interfaces de red, etc. El problema es que este programa está obsoleto y ha sido reemplado por `ss`. 


En **Windows** tenemos dos herramientas características de monitorización:

- **Task Manager:** muestra las aplicaciones y procesos que se están ejecutando en el sistema con información tal como el proceso padre o la cantidad de memoria que consumen.

- **Network Monitor Agent:** monitoriza el tráfico de red.






