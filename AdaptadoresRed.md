# Adaptadores de Red de VirtualBox

Virtual Box tiene un total de **7 adaptadores de red**. En este documento se explicará la función principal de cada uno de los adaptadores, una ventaja del mismo y algún escenario en el que sería util su uso.


## NAT
Este adaptador es el más usado por todos los usuarios por su simpleza a la hora de configurar y su función principal es la de acceder a internet y redes exteriores utilizando la dirección IP del host, manteniendo la máquina virtual aislada del resto de la red.

  - **Ventaja Principal** = Gran simpleza en su configuración y aplicación.
  - **Escenario de Uso** = En el desarrollo de aplicaciones web necesitaremos probar el funcionamiento de la página, por lo que configurando una NAT, podremos salir al exterior para probar la página de manera segura.


## Adaptador Puente
El adaptador puente conecta a la máquina virtual directamente a la red física de nuestro host, provocando que la mv trabaje y actue como un dispositivo más de la red local, permitiendo que se comunique con otros dispositivos de su misma red.

  - **Ventaja Principal** = Adaptador que ofrece una gran facilidad para integrar máquinas a redes existentes.
  - **Escenario de Uso** = Se puede configurar un servidor de archivos dentro de una máquina virtual y usar el adaptador puente para que la mv obtenga una dirección IP válida en la red física, facilitando así la conexión y transferencias entre equipos.


## Red Interna
La función principal de la red interna es ofrecerle a una serie de equipos comunicación total entre ellos estando aislados de la red externa para no recibir interferencias.

  - **Ventaja Principal** = Muy bueno para operar en un entorno seguro de atacantes del exterior.
  - **Escenario de Uso** = Se puede usar este adaptador para simular ataques de hacking entre máquinas y para crear entornos de empresas, como dominios, de prueba sin que haya interferencias del exterior.


## Adaptador solo Anfitrión
Este adaptador permite que una máquina virtual se comunique únicamente con la máquina física y con otras mv que estén configuradas en la misma red solo anfitrión.

  - **Ventaja Principal** = No se tiene acceso a internet por lo que la red será segura en todo momento.
  - **Escenario de Uso** = Se pueden hacer pruebas con un servidor Apache de forma segura.


## Controlador Genérico
El controlador genérico permite a las máquinas virtuales utilizar controladores personalizados para simular diferentes tipos de conexiones de red.

  - **Ventaja Principal** = Es un adaptador que permite una gran personalización en el entorno de red permitiendo integrar protocolos o configuraciones de red no convencionales.
  - **Escenario de Uso** = Puede resultar útil cuando se quiere integrar al entorno de red un protocolo el cual no es soportado por ningún otro adaptador de red.


## Red NAT
Este adaptador es extremadamente similar al NAT. La única diferencia entre ellos es que la red Nat permite la comunicación entre máquinas virtuales.

  - **Ventaja Principal** = Permite la comunicación directa entre máquinas virtuales.
  - **Escenario de Uso** = En el desarrollo de aplicaciones web necesitaremos probar el funcionamiento de la página, por lo que configurando una NAT, podremos salir al exterior para probar la página de manera segura.
