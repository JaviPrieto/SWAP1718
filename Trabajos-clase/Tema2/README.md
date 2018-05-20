## **Tema 2: Alta disponibilidad y escalabilidad**    

**1. Calcular la disponibilidad del sistema si tenemos dos réplicas de cada elemento (en total 3 elementos en cada subsistema):**


| Component 	| Availability 1 | Availability 2 | Availability 3 | 
|---------------|----------------|----------------|----------------|
| Web     	| 0.85000000     | 0.97750000	  | 0.99660000	   | 
| Application   | 0.90000000     | 0.99000000     | 0.99900000     |
| Database      | 0.99900000     | 0.99999000	  | 0.99999999     |
| DNS           | 0.98000000     | 0.99960000	  | 0.99992000     |
| Firewall      | 0.85000000     | 0.97750000	  | 0.99660000     |
| Switch        | 0.99000000     | 0.99990000	  | 0.99999000     |
| Datacenter    | 0.99990000     | 0.99990000	  | 0.99990000     |
| ISP           | 0.95000000     | 0.99750000	  | 0.99987000     |


***

**2. Buscar frameworks y librerías para diferentes lenguajes que permitan hacer aplicaciones altamente disponibles con relativa facilidad.**

- **Forever**: forever es una utilidad de Node.js para línea de comandos que asegura que una aplicación se ejecute de manera continua. También permite monitorizar la aplicación usando forever-monitor. Tiene una funcionalidad mucho más reducida que pm2 y, por tanto, es menos popular.

- **Pacemaker**: al igual que pm2, pacemaker es un CRM que nos da alta disponibilidad y escalabilidad. En DigitalOcean hay documentación disponible para crear, usándolo junto a corosync, una aplicación con alta disponibilidad.

- **Keepalived**: software de enrutamiento. Su principal objetivo es proporcionar un sistema robusto y simple para balanceo de carga y alta disponibilidad a sistemas Linux. Al igual que con pacemaker, DigitalOcean tiene documentación sobre cómo configurar un servicio con alta disponibilidad usando keepalived.


