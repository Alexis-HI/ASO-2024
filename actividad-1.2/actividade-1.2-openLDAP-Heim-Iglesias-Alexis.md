# Actividad 1.2 - LDAP Account Manager y `phpLDAPAdmin` 

## 1 - Instalación de las dependencias necesarias.

### Instalamos los paquetes necesarios con el siguiente comando.

![Cap1](img/1.PNG)

### Para el correcto funcionamiento del programa necesitaremos activar una funcionalidad de php. Para ello verificaremos la versión del mismo e introduciremos el comando para activar el PHP-CGI. Por último reiniciamos el servicio Apache.

![Cap2](img/2.PNG)

## 2 - Configuración del LDAP Account Manager

### Editaremos el siguiente archivo para darle acceso remoto a todos los equipos de la red que indicamos y reiniciamos de nuevo el servicio.

![Cap3](img/3.PNG)

### Accedemos desde el cliente al LDAP Account Manager y entramos en la opción “LAM Configuration” > “Edit general settings” > Y escribimos “lam” en el espacio para la contraseña. Ya dentro del menú, bajaremos al fondo de la página para cambiar la contraseña del master.

![Cap4](img/4.PNG)
![Cap5](img/5.PNG)

### Ahora entraremos en la opción “Edit server profile” (lam es la contraseña por defecto) para hacer las siguientes modificaciones en los campos de List of valid users, treeview y contraseña.

![Cap6](img/6.PNG)

### Volveremos a “Edit server profile”, pero esta vez iremos al apartado “Account Types” y modificaremos los campos “LDAP suffix” de los usuarios y grupos de la siguiente forma.

![Cap7](img/7.PNG)

### Ahora solo quedaría acceder al entorno con el usuario Admin y su contraseña.


![Cap8](img/8.PNG)
![Cap9](img/9.PNG)

## 3 - Eliminar UO anterior.

### Será tan simple como entrar en el apartado Tools > OU editor y en el apartado de Delete seleccionar nuestra antigua UO.

![Cap10](img/10.PNG)
![Cap11](img/11.PNG)

## 4 - Crear UO nueva.

### Creamos las unidades necesarias simplemente indicando el directorio padre y el nombre de la UO.

![Cap12](img/12.png)
![Cap13](img/13.PNG)

### Crearemos de la misma forma el resto de unidades organizativas.

![Cap14](img/14.PNG)

### El resultado sería algo así.

![Cap15](img/15.PNG)

## 5 - Crear grupos nuevos.

### La mecánica de creación de grupos será muy similar a la de crear unidades organizativas.

![Cap16](img/16.PNG)
![Cap17](img/17.PNG)

### El resultado final de la inclusión de grupos sería el siguiente.

![Cap18](img/18.PNG)
![Cap19](img/19.PNG)

## 5 - Crear usuarios nuevos.

### Crearemos un par de usuarios de ejemplo. Dentro del apartado de creación iremos a la opción Unix y ahí indicaremos los datos del usuario, su uid y su grupo.

![Cap20](img/20.PNG)

### Quedando el resultado de la siguiente forma.

![Cap21](img/21.PNG)
![Cap22](img/22.PNG)

## 6 - Instalación y configuración de phpLDAPadmin.

### Intalamos el programa.

![Cap23](img/23.PNG)

### Ahora configuramos su archivo .conf para indicarle nuestro dominio.

![Cap24](img/24.PNG)

### Nos conectaremos desde el cliente y le daremos clic en el botón “conectar”.

![Cap25](img/25.PNG)
![Cap26](img/26.PNG)
![Cap27](img/27.PNG)

## 7 - Crear una UO nueva.

### Iremos al lugar indicado en la captura y le daremos clic al botón de crear nuevo objeto y seleccionaremos la opción “Genérico: Unidad Organizativa”.

![Cap28](img/28.PNG)
![Cap29](img/29.PNG)
![Cap30](img/30.PNG)
