## **Tema 7: Almacenamiento de datos**    

**1. ¿Qué tamaño de unidad RAID se obtendrá al configurar un RAID 0 a partir de dos discos de 100 GB y 100 GB?**
**¿Qué tamaño de unidad RAID se obtendrá al configurar un RAID 0 a partir de tres discos de 200 GB cada uno?**

Al configurar un RAID 0 con dos discos de igual capacidad, el tamaño total será la suma de la capacidad de ambos. 

- **Caso1** : 200GB
- **Caso2** : 600GB 

Ahora bien, si hacemos un RAID 0 con discos de diferente tamaño, el tamaño total del RAID será el tamaño del disco más pequeño multiplicado por el número de discos.

***

**2. ¿Qué tamaño de unidad RAID se obtendrá al configurar un RAID 1 a partir de dos discos de 100GB y 100GB?**
**¿Qué tamaño de unidad RAID se obtendrá al configurar un RAID 1 a partir de tres discos de 200GB cada uno?**

En el caso del RAID 1, como su objetivo es clonar archivos en ambos discos duros de forma que si uno deja de funcionar los datos seguirán ahí, si hacemos un RAID 1 a partir de dos o más discos del mismo tamaño, el tamaño del RAID será igual al tamaño de los discos. 

- **Caso1** : 100GB
- **Caso2** : 200GB 
