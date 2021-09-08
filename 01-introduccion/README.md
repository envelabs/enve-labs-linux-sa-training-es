# Introducción a Linux

### Sistema de Archivos
El sistema de archivos en un sistema Linux es lo que nos permite ordenar los datos que vamos a procesar, como también el software y el acceso a éste para el procesado de éstos.

##### Navegando el sistema de Archivos
Para poder navegar un sistema de archivos linux es necesario introducir comandos. Un comando, es un programa que nos permite darle una instrucción al sistema para que realice una operación puntual, como ser el desplazamiento dentro del sistema, la creación de un archivo o la ejecución de otro programa.

La información dentro de un sistema Linux se estructura de manera jerárquica y agrupa mediante directorios, los que a su vez pueden contener más directorios o archivos. En Linux, todo puede representarse mediante un archivo.

### comandos
un comando es una instrucción que le damos al sistema operativo para que nos permita interactuar con el hardware. En general el comando sigue un formato que inicia con su `nombre` y luego puede ser acompañado por opciones que modifican al comando, como también uno o varios parámetros que determinan el comportamiento de éste o definen sobre qué elemento se va a operar.

##### formato de un comando

    <nombre-comando> [-opciones] [param1|param2|param-n]


##### ayuda de comandos
todo comando presenta una ayuda mediante documentación a la que se puede acceder mediante el comando `man`, de manual

    man man

##### situándonos
el comando `pwd` nos permite identificar el lugar en el que nos encontramos dentro del sistema de Archivos

    pwd


##### listando Archivos
el comando `ls` nos permite listar el contenido de directorios como también ver propiedaes de los arhivos

    ls <archivo|dir>

##### desplazamiento
el comando `cd` nos permite desplazarnos a otro punto dentro del sistema de archivos

    cd <dest>

##### creacion de directorios
el comando `mkdir` nos permite crear un directorio que a su vez puede contener archivos o más directorios

    mkdir <nombre-directorio>

##### creacion de archivos
el comando `touch` nos permite crear un arhivo

    touch <nombre-archivo>

##### borrado de archivos
el comando `rm` nos permite borrar un arhivo

    rm <nombre-archivo>

##### borrado de directorios
el comando `rm -fr` nos permite borrar un directorio y su contenido

    rm -fr <nombre-directorio>

##### renombrar archivos
el comando `mv` nos permite renombrar un archivo o un directorio

    mv <nombre-archivo|nombre-directorio> <nuevo-nombre-archivo|nuevo-nombre-directorio>

##### renombrar archivos
el comando `mv` nos permite renombrar un archivo o un directorio

    mv <nombre-archivo|nombre-directorio> <nuevo-nombre-archivo|nuevo-nombre-directorio>

##### imprime una linea
el comando `echo` nos permite mostrar una linea a través de la salida standard

    echo <linea-a-imprimir>

##### mostrar contenido de archivos
el comando `cat` nos permite mostrar el contenido de un arhivo a través de la salida standard

    cat <nombre-archivo>

##### buscar archivos
el comando `which` nos permite buscar por nombre a través de los directorios definidos en la variable $PATH

    which <nombre-archivo>

##### localizar

    updatedb

    locate <nombre-archivo>  

##### buscar archivos o directorios

    find <nombre-archivo>
