###netstat
netstat (estadísticas de red) es una herramienta de la línea de comandos para controlar las conexiones de red entrantes y salientes, así como la visualización de las tablas de enrutamiento, las estadísticas de la interfaz. Es muy útil en términos de resolución de problemas de red y la medición del desempeño. Netstat es una de las herramientas de depuración de servicios de red más básicas, que le dice qué puertos están abiertos y si los programas escuchan en tales puertos.

##### Listado de todos los puertos (tanto TCP como UDP).

     netstat -a | more

##### Listado solo de las conexiones de puerto TCP ( Protocolo de control de transmisión).

    netstat -at

##### Listado solo de las conexiones de puerto UDP ( Protocolo de datagramas de usuario).

     netstat -au

##### Listado de todas las conexiones de puertos de escucha activas.

     netstat -l

##### Listado de todos los puertos TCP de escucha activos.

     netstat -lt

##### Listado de todos los puertos UDP de escucha activos.

     netstat -lu

##### Listado de todos los puertos de escucha activos de UNIX.

     netstat -lx

##### Mostrando estadísticas por protocolo
     
     netstat -s

##### Mostrando estadísticas por protocolo TCP

      netstat -st

##### Desplegar estadísticas del protocolo UDP 
      
      netstat -su

##### Al mostrar el nombre del servicio con su número de PID, con la opción netstat -tp se mostrará "PID/Nombre del programa".

      netstat -tp

##### Mostrando el modo Promiscuo con el interruptor -ac, netstat imprime la información seleccionada o actualiza la pantalla cada cinco segundos. Actualización de pantalla predeterminada en cada segundo.

       netstat -ac 5 | grep tcp

##### Mostrar la tabla de enrutamiento IP del kernel con netstat y comando de ruta.

       netstat -r


##### Mostrar las transacciones de paquetes de interfaz de red que incluyen tanto la transferencia como la recepción de paquetes con el tamaño de MTU.

       netstat -i

##### Muestra información de pertenencia a grupos de multidifusión tanto para IPv4 como para IPv6.

       netstat -g

##### Averiguar  cuántos programas de escucha se ejecutan en un puerto.

       netstat -ap | grep http

##### Para mas infomacion 
     
     netstat --help



### ifconfig
 
La orden ifconfig se utiliza para configurar correctamente los interfaces de red de nuestro sistema Unix, se utiliza para  inicializar la interfaz de red y para habilitar o deshabilitar dichas interfaces.

##### Para obtener información de interfaces de red activas:
    
      ifconfig

##### Ver la configuración de red de un adaptador Ethernet 
    
     ifconfig eth0

##### Mostrar detalles de todas las interfaces, incluidas las interfaces deshabilitadas
  
    ifconfig -a

##### Deshabilitar una interfaz

      ifconfig eth0 down
    

##### Habilitar una interfaz
 
     ifconfig eth0 up

##### Asignar dirección IP a una interfaz
   
    ifconfig eth0 192.168.2.2

##### Modo promiscuo

    ifconfig eth0 promisc

##### Salir del modo promiscuo el interfaz

     ifconfig eth0 -promisc   

##### Establecer el valor de MTU del interface

      ifconfig eth0 mtu 1500    

##### Establecer la máscara para el interfaz eth0

     ifconfig eth0 netmask 255.255.255.0 

##### Para mas informacion

     ifconfig --help
