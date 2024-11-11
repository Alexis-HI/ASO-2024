#Actividad 1.2 - LDAP Account Manager e `phpLDAPAdmin` 

## 1 - Instalación de las dependencias necesarias.

### Instalamos los paquetes necesarios con el siguiente comando.

![Cap1](img/1.png)

### Para el correcto funcionamiento del programa necesitaremos activar una funcionalidad de php. Para ello verificaremos la versión del mismo e introduciremos el comando para activar el PHP-CGI. Por último reiniciamos el servicio Apache.

![Cap2](img/2.png)

## 2 - Configuración del LDAP Account Manager

### Editaremos el siguiente archivo para darle acceso remoto a todos los equipos de la red que indicamos y reiniciamos de nuevo el servicio.

![Cap3](img/3.png)

### Accedemos desde el cliente al LDAP Account Manager y entramos en la opción “LAM Configuration” > “Edit general settings” > Y escribimos “lam” en el espacio para la contraseña. Ya dentro del menú, bajaremos al fondo de la página para cambiar la contraseña del master.

![Cap4](img/4.png)
![Cap5](img/5.png)

### Ahora entraremos en la opción “Edit server profile” (lam es la contraseña por defecto) para hacer las siguientes modificaciones en los campos de List of valid users, treeview y contraseña.

![Cap6](img/6.png)

### Volveremos a “Edit server profile”, pero esta vez iremos al apartado “Account Types” y modificaremos los campos “LDAP suffix” de los usuarios y grupos de la siguiente forma.

![Cap7](img/7.png)

### Ahora solo quedaría acceder al entorno con el usuario Admin y su contraseña.


![Cap8](img/8.png)
![Cap9](img/9.png)

## 3 - Eliminar UO anterior.

### Será tan simple como entrar en el apartado Tools > OU editor y en el apartado de Delete seleccionar nuestra antigua UO.

![Cap10](img/10.png)
![Cap11](img/11.png)
![Cap12](img/12.png)

## 4 - Crear UO nueva.

### Creamos las unidades necesarias simplemente indicando el directorio padre y el nombre de la UO.

![Cap13](img/13.png)
![Cap14](img/14.png)

### Crearemos de la misma forma el resto de unidades organizativas.

![Cap15](img/15.png)

### El resultado sería algo así.

![Cap16](img/16.png)

## 5 - Crear grupos nuevos.

### La mecánica de creación de grupos será muy similar a la de crear unidades organizativas.

![Cap17](img/17.png)
![Cap18](img/18.png)

### El resultado final de la inclusión de grupos sería el siguiente.

![Cap19](img/19.png)
![Cap20](img/20.png)

## 5 - Crear usuarios nuevos.

### Crearemos un par de usuarios de ejemplo. Dentro del apartado de creación iremos a la opción Unix y ahí indicaremos los datos del usuario, su uid y su grupo.

![Cap21](img/21.png)

### Quedando el resultado de la siguiente forma.

![Cap22](img/22.png)
![Cap23](img/23.png)

## 6 - Instalación y configuración de phpLDAPadmin.

### Intalamos el programa.

![Cap24](img/24.png)

### Ahora configuramos su archivo .conf para indicarle nuestro dominio.

![Cap25](img/25.png)

### Nos conectaremos desde el cliente y le daremos clic en el botón “conectar”.

![Cap26](img/26.png)
![Cap27](img/27.png)
![Cap28](img/28.png)

## 7 - Crear una UO nueva.

### Iremos al lugar indicado en la captura y le daremos clic al botón de crear nuevo objeto y seleccionaremos la opción “Genérico: Unidad Organizativa”.

![Cap29](img/29.png)
![Cap30](img/30.png)
![Cap31](img/31.png)
