#Actividad 1.1– OpenLDAP desde la terminal

## 0. Instalación, apt update, apt upgrade y configurar en red interna.

![Cap1](img/1.png)
![Cap2](img/2.png)
![Cap3](img/3.png)
![Cap4](img/4.png)
![Cap5](img/5.png)

###Después de los APT, en ambas máquinas, configuraremos la red de Virtual Box en modo “Red Interna” en las dos máquinas. Por ahora mantendremos la “red NAT”. Cambiaremos a “Red Interna” únicamente después de que todos los servicios necesarios estén instalados. Esta captura solo es para ubicar donde cambiar el modo del adaptador de red.

![Cap6](img/6.png)

## 1. Descarga e instalación del DHCP y del LDAP.

### Descargamos e instalamos ambos servicios con los siguientes comandos.

![Cap7](img/7.png)
![Cap8](img/8.png)

### Ahora podremos pasar ambas máquinas a red interna.

## 2. Configuración de una IP fija.

### Crearemos un archivo .yaml y aplicaremos los cambios.

![Cap9](img/9.png)
![Cap10](img/10.png)

## 3. Configuración del DHCP.

### Ahora configuraremos el dhcp, para ello accederemos al archivo .conf, iremos al fondo del mismo y lo modificaremos de la siguiente manera.

![Cap11](img/11.png)
![Cap12](img/12.png)

### Luego de aplicar las modificaciones verificaremos que la configuración es correcta con el siguiente comando.

![Cap13](img/13.png)

### Ahora iremos al siguiente archivo de configuración para especificar la tarjeta de red que usará el DHCP.

![Cap14](img/14.png)
![Cap15](img/15.png)

### Ahora reiniciamos el servicio para aplicar los cambios y comprobaremos el estado del mismo.

![Cap16](img/16.png)

### En este punto solo quedaría poner ambas máquinas en red interna para que se vean y verificar el correcto funcionamiento del DHCP mirando si el cliente ha conseguido ip.

![Cap17](img/17.png)

## 4. Configurar Linux como Router.

### Primero verificaremos si se permite el paso de paquetes a través del servidor con el siguiente comando.

![Cap18](img/18.png)

### Al estar a 0 quiere decir que no se permite el paso de los paquetes. Para cambiar eso, descomentamos la línea de net.ipv4.ip_forward=1.

![Cap19](img/19.png)
![Cap20](img/20.png)

### Aplicamos los cambios y comprobamos si han dado resultado.

![Cap21](img/21.png)

### Ahora haremos el enmascaramiento para que los paquetes sepan por dónde ir.

![Cap22](img/22.png)

## 5. Configuración del LDAP.

### Para la configuración inicial seguiremos los siguientes pasos.

![Cap23](img/23.png)
![Cap24](img/24.png)
![Cap25](img/25.png)
![Cap26](img/26.png)
![Cap27](img/27.png)
![Cap28](img/28.png)
![Cap29](img/29.png)
![Cap30](img/30.png)

### Visualizamos la información de nuestro dominio.

![Cap31](img/31.png)

## 6. Creación de la unidad organizativa.

### Creamos el archivo de creación de la unidad organizativa.

![Cap32](img/32.png)
![Cap33](img/33.png)

### Importamos el archivo al servidor ldap.

![Cap34](img/34.png)
![Cap35](img/35.png)

## 7. Creación de grupos.

### Copiamos el archivo del active directory y lo editamos para configurar el grupo.

![Cap36](img/36.png)
![Cap37](img/37.png)

### Ya con el archivo editado, lo subiremos al ldap y repetiremos la operación con el resto de grupos que debamos crear.

![Cap38](img/38.png)
![Cap39](img/39.png)

## 8. Creación de usuarios.

###  Para la creación de los usuario será exactamente igual que los grupos. Únicamente cambiará la sintaxis del archivo.

![Cap39](img/39.png)

### Lo subimos de la misma forma que los grupos.

![Cap40](img/40.png)

