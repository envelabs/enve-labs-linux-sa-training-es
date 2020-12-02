
### Netstat
netstat es una herramienta de línea de comandos que muestra un listado de las conexiones activas de una computadora, tanto entrantes como salientes.
LISTENING: El puerto está abierto escuchando, en espera de una conexión
ESTABLISHED: La conexión ha sido establecida
CLOSE_WAIT: La conexión está abierta, pero el otro extremo nos comunica que no se continuará enviando información
TIME_WAIT: La conexión ha sido cerrada, pero no se elimina de la tabla de conexión por si queda algo pendiente de recibir
LAST_ACK: La conexión se está cerrando
CLOSED: La conexión ha sido cerrada completamente

##### Listado de todos los puertos de escucha TCP y conexiones UDP
      netstat -a 
##### Listado de conexiones de puertos TCP  (Transmission Control Protocol) 
       netstat -at

##### Listado sólo conexiones de puerto UDP (User Datagram Protocol) 
       netstat -au

##### Listado de todas las conexiones activas de escucha de puertos 
       netstat -l

##### Listado de todos los puertos TCP de escucha activa mediante la opción
        netstat -lt 

##### Listado de todos los puertos UDP de escucha activa mediante la opción
 netstat -lu

##### Mostrando estadísticas por protocolo.  para TCP, UDP, ICMP e IP. 

         Netstat -s

###### Mostrando estadísticas de único protocolo TCP mediante la opción 

         netstat -st

##### Visualización del nombre de servicio con PID

           Netstat -tp

##### Viendo modo promiscuo, netstat imprimirá la información seleccionada o actualización de la pantalla cada cinco segundo. Actualización de la pantalla por defecto en cada segundo.

      netstat -ac 5 |grep tcp

##### Viendo enrutamiento IP del núcleo
            Netstat -r

#####  Mostrando transacciones de paquetes de interfaz de red que incluye tanto la transferencia y recepción de paquetes con un tamaño de MTU.

         netstat -l 

##### Mostrando tabla de interfaz del kernel

         netstat -ie 

##### Visualización de información de IPv4 e IPv6

         netstat -g

##### Imprimir Información Netstat continuamente

         netstat -g

##### Encontrar familias de direcciones sin configurar con alguna información útil.

         netstat --verbose
 
##### para más información 

         netstat --help 

### Ifconfig 

##### ifconfig sin argumentos nos muestra los detalles de todos los interfaces de red que se encuentren activos en nuestro sistema.
  
      ifconfig 

 #####  Para deshabilitar un adaptador de red

       ifconfig enp0s3 down
 
 #####  si quisiéramos mostrar todos los adaptadores, incluidos los deshabilitados.
      
      ifconfig -a 

 ##### Para volver a habilitar un adaptador de red deshabilitado.

      Ifconfig enp0s3 up
##### Para asignar una nueva dirección IP al adaptador de red.
   
     ifconfig enp0s3 192.168.1.10

##### Si necesitamos asignar una nueva máscara de red al adaptador, habrá que incluir la palabra netmask.
    
     ifconfig enp0s3 netmask 255.255.255.0

##### Modo promiscuo 

      ifconfig enp0s3 promisc


##### Cuando necesitemos devolver el adaptador a su configuración normal.

     ifconfig enp0s3 -promisc

##### Para mas info 
      
      ifconfig --help


### PS 
  El comando ps muestra por pantalla un listado de los procesos que se están ejecutando en el sistema.
  Si no añadimos ningún parámetro, ps mostrará los procesos del usuario con el que estamos logueados.
  
#####  Listar los procesos de todos los usuarios con información añadida
    
        ps -aux 

##### Listar los procesos de todos los usuarios.
    
        ps -a 

##### Listar información del proceso como por ejemplo el usuario que lo está corriendo, la utilización de Cpu y memoria, etc.
      
      ps -u 

##### Listar procesos de todas las terminales y usuarios.

       ps -x

##### Mostrar información que incluye el UID    
    
       ps -l

#### Mostrar el listado procesos en un formato tipo árbol que permite ver como los procesos interactuan entre si.
  
       ps -forest

###  Kill

  Este comando simplemente envía una señal para terminar uno o más identificadores de proceso (Process ID). Debe ser propietario del proceso o ser un usuario privilegiado.

      

##### Si queremos finalizar el proceso  debemos mencionar el PID del Servicio.

      kill <PID>