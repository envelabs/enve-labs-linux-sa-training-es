# Edición de Archivos

### redireccionamiento

#### comando `echo`
    echo "hola amigos"

#### redireccionamiento de standard output
    echo "hola amigos" > texto.txt

#### inspeccionando el contenido de un archivo
    cat texto.txt

#### redireccionando el standard input
    wc -m < texto.txt

#### redireccionando el standard error
    ls testo.txt 2> error.txt

#### concatenando o `piping`
    cat error.txt | wc -m

    cat error.txt | wc -m > count.txt
