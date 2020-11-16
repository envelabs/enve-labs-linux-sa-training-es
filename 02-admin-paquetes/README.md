# Administración de Paquetes de Software

La administracion de paquetes es un conjunto de tareas de instalacion, actualizacion, y desinstalacion de recursos de software
en nuestro sistema.

### dpkg

dpkg es el programa base para manejar paquetes Debian en el sistema. Dicha herramienta sirve para instalar un paquete Debian ya disponible ya que no descarga nada. 


##### Instalacion de un paquete
 
Para realizar una insatlacion hemos de utilizar el pametro -i. Por ejemplo si queremos instalar el paquete vagrant_2.2.10_86_64.deb que nos hemos descargado de la web de Vagrant, lo hariamos de esta forma:

    sudo dpkg -i vagrant_2.2.10_86_64.deb

##### Listar los paquetes instalados
 
Si queremos listar los paquetes instalados usaremos el parametro -l.

    dpkg -l

##### Desinstalar un paquete
 
Si queremos desintalar un paquete que ya no necesitamos, debemos utilizar el parametro -r, asi:
    
    sudo dpkg -r vagrant

##### Eliminar todo lo que este asociado al paquete

Para eliminar completamente todo lo asociado con un paquete, utilizamos la opcion --purge seguida del nombre del paquete.

     sudo dpkg --purge vagrant
 
##### Para ver el contenido de un paquete 

Para ver el contenido de un paquete usamos -c, como parametro. 

    sudo dpkg -c vagrant_2.2.10_x86_64.deb

##### Buscar la localizacion de un paquete
 
Con dpkg tambien podemos saber la documentacion del binario y la documentacion del paquete, utilizando -L, como parametro 

    sudo dpkg -L vagrant

##### Ayuda de dpkg  
 Si queremos obtener ayuda para saber como utilizar la herramienta, podemos consultar la pagina de man o el parametro --help
   
    sudo dpkg --help




### apt-get / apt-cache

apt-get nos permite descargar, actualizar e instalar paquetes, apt-cache por otro lado permite lanzar consultas y buscar paquetes contra la base de datos de los repositorios.

##### Instalar un paquete:
 
    sudo apt-get install <paquete> 

##### Desinstalar unn paquete:
    
     sudo apt-get remove <paquete>

##### Eliminar un paquete incluidos sus ficheros de configuracion:

    sudo apt-get purge <paquete> 

##### Eliminar de forma automática aquellos paquetes que no se estén utilizando: 

     sudo apt-get autoremove <paquete> 

##### Actualizar un paquete a la ultima version disponible en el repositorio:

     sudo apt-get update <paquete>

##### Actualizar el sistema. Actualizará todos los paquetes que dispongan de una versión superior dentro de la rama instalada de la distribución:

     sudo apt-get dist-upgrade

##### Descargar únicamente las fuentes de un paquete para manipularlas de forma manual:

    sudo  apt-get dist-upgrade

##### Limpiar cachés, paquetes descargados:

     sudo apt-get autoclean

##### Verificar que no tenemos ninguna dependencia incumplida:

      sudo apt-get check


### apt-cache

#####Buscar un paquete en los repositorios, se puede especificar un patrón, expresión regular, el nombre exacto del paquete, etc:

    sudo apt-cache search <paquete> 

##### Mostrar información sobre un paquete específico:

     apt-cache showpkg <paquete>

##### Mostrar información del paquete incluyendo la descripción, información del paquete como su sitio web, página de bugs:
     
    sudo apt-cache show <paquete>

##### Mostrar dependencias de un paquete:
   
     sudo apt-cache depends <paquete>

##### Mostrar los nombres de todos los paquetes instalados en el sistema:

     sudo apt-cache pkgnames
##### Si necesitamos ayuda 

     apt-get --help 


### systemctl
El comando systemctl es una herramienta que sirve para poder controlar el sistema y sus servicios. 

#####Para iniciar servicios 

    sudo systemctl start apache2.service

##### Para detener servicios

    sudo systemctl stop apache2.service

##### Para reiniciar el servicio 

    sudo systemctl restart apache2.service

##### Para recargar el servicio 

    sudo systemctl reload apache2.service

##### Para habilitar el servicio 

    sudo systemctl enable application.service

##### Para desahabilitar 

    sudo systemctl disable application.service

##### Para verificar el estado del servicios

    sudo systemctl status apache2

##### Para listar los servicios
 
     systemctl list-units --all --type=service --no-pager

##### Para mostrar todos los servicios activos
 
    systemctl list-units --all --state=active

##### Para mostrar los servicios inactivos 

    systemctl list-units –all –state=active


