Curso de GIT y GITHUB Desde Cero - MoureDev

# Comandos principales de Git

# Saber si tenemos git instalado
    git

# Consultar la versión instalada de git
    git -v
    git --version

# Consultar la ayuda de git
    git -h
    git --help

# Listar directorios 
    ls

# Cambiar de directorio
    cd "Hello Git"

# Conocer la ruta en la que estoy ubicado
	pwd	

# Crear un directorio
    mkdir "Hello Git"	
    
# Eliminar un directorio
    rmdir "Hello Git"

# Abrir editor de código 
    code .	

# Limpiar la consola
    clear

# Configuración a nivel global para todo lo que se realice en git desde la máquina 
    git config --global user.name "sarismejiasanchez"
    git config --global user.email "sarismejiasanchez@gmail.com"	

# Crear archivo en el directorio
    touch hellogit.py

# Inicializar git en un directorio
# Tras hacer esto nos refleja el nombre de la rama principal de nuestro proyecto (main) 
    git init

# Consultar estado del repositorio
    git status

# Añadir fichero al repositorio (stage)
    git add hellogit.py

# Añadir todos los ficheros pendientes al repositorio
    git add .

# Realizar commit de los cambios, esto nos henera un hash (Ej. 686d47d)
    git commit -m "Este es mi primer commit"

# Consultar log del repositorio (las fotografias de mi repositorio)
    git log

# Consultar cambios en ficheros
    git status

# Volver atrás a un fichero
    Git checkout hellogit.py	

# Volver para atras a la última fotografia
    git reset

# Muestra los cambios de la rama de manera grafica
    git log --graph	

# Muestra cada cambio en una línea para ver rápidamente lo que ha pasado en cada uno
# Refleja la llave hash completa
    git log --graph --pretty=oneline	

# Decoramos todos los cambios
# Muestra cada cambio en una línea para ver rápidamente lo que ha pasado en cada uno
# Refleja el hash reducido
    git log --graph --decorate --all --oneline	

# Crear alias
    git config --global alias.tree "log --graph --decorate --all --oneline"

# Usar alias
    git tree

# Crear .gitignore
# Dentro del .gitignore agregamos **/ + nombre del fichero (Ej. **/.DS_Store) 
# Los **/ le indica a git que no importa la ubicación del fichero dentro del directorio, 
# siempre debe ignorar los archivos con ese nombre
    touch .gitignore

# Conocer los cambios vs la última fotografia
    git diff

# Volver atrás a una fotografia especifica haciendo uso del hash
    git checkout 686d47d64da297908967465292ef9128664c547c

# El siguiente mensaje de error, nos indica que tenemos cambios locales sin fotografia que pueden perderse
# si realizamos el checkout al hash definido
    error: Your local changes to the following files would be overwritten by checkout:
    hellogit.py
    Please commit your changes or stash them before you switch branches.

# Debemos entonces realizar checkout a la última fotografía del archivo 
# y posteriormente reintentar el checkout al hash
    # $ git tree
    # * 401635f (main) Se añade el .gitignore
    # * 82ee4cf Se actualiza el texto del print
    # * 4dcdad1 Este es mi segundo commit
    # * 686d47d (HEAD) Este es mi primer commit

# Cambiar el HEAD del proyecto usando la parte final del hash
    git checkout 401635f

    # Previous HEAD position was 686d47d Este es mi primer commit
    # HEAD is now at 401635f Se añade el .gitignore

    # $ git tree
    # * 401635f (HEAD, main) Se añade el .gitignore
    # * 82ee4cf Se actualiza el texto del print
    # * 4dcdad1 Este es mi segundo commit
    # * 686d47d Este es mi primer commit

# Desaparecer todo lo que hemos hecho en adelante de un commit seleccionado
    git reset --hard 4dcdad1

# Log completo
    git reflog
    
# Deshacer git reset --hard
    git reset --hard 4dcdad1

# Crear rama
    git branch login

# Cambiar de rama
    git switch login

# Combinar los cambios entre ramas
    git merge main

# Hacer commit en local, no afecta al arbol
    git stash

# Listar stash
    git stash list

# Traer lo que tengo en stash para continuar trabajando en ello
    git stash pop

# Eliminar stash
    git stash drop