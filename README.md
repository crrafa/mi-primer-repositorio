<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/e/e0/Git-logo.svg/1024px-Git-logo.svg.png" alt="Git" width="200"/>

## Practica No. 1
## Flujo basico de Git
## Tema no. 2 - Fundamentos de control de versiones
## Ingeniería en Tecnologías de la Información y Comunicación
## Software para el Control de Versiones

---

Desarrollar la siguiente practica, recuerda que deberas presentar evidencias del desarrollo de esta, en forma de un repote de practica.

### 1. Comprobar version de Git.


```C#
git version
```

    git version 2.37.1.windows.1



> la versión de git instalada puede variar.

### 2. Crear un nuevo directorio.
Nuevo directorio de trabajo para el desarrollo de la presente practica.

### 3. Inicializa un nuevo repositorio.

Ingresar el comando `git init` para crear un nuevo repositorio de Git. Git ahora es consciente de los archivos en el proyecto. 


```C#
git init
```

    Initialized empty Git repository in D:/Usuarios/Escritorio/Practicas Jupyter/Tema#1/practica#1/.git/



> La ejecución de git init crea un subdirectorio `.git` en el directorio de trabajo actual, que contiene todos los metadatos de Git necesarios para el nuevo repositorio.

### 4. Creación de archivo README.
Crear un archivo de texto llamado README.md


```C#
code README.md
```

Ingresar el siguiente mensaje:

```
# Este es mi primer repositorio [nombre_completo].
```

> Guardar archivo README.md

### 5. Revisar el estado de los archivos.
Ingresar `git status` para comprobar el estado.
Este comando muestra el estado del working tree. También muestra los cambios que se han preparado para commit(staged), los cambios que no se han preparado (no staged) y los archivos que Git no realiza un seguimiento.


```C#
git status
```

    On branch master

    

    No commits yet

    

    Untracked files:

      (use "git add <file>..." to include in what will be committed)

    	README.md

    

    nothing added to commit but untracked files present (use "git add" to track)



> README.md aparece en la sección Archivos sin seguimiento. Git aún no está rastreando los archivos. Para realizar un seguimiento de los archivos, tenemos que confirmar (commit) estos archivos agregándolos al área de preparación (staging area).

### 6. Rastrear nuevo archivo en especifico.
Ingresar `git add [archivo]`. El archivo se agregara al área de preparación (staging area).


```C#
git add README.md
```

> README.md se encuentra preparado para commit.

### 7. Revisar el estado de los archivos.
Ingresar `git status`, muestra el estado del working tree. Aparecera README.md en verde, el archivo ahora está en el área de preparación (staging area) y aún no se ha confirmado.


```C#
git status
```

    On branch master

    

    No commits yet

    

    Changes to be committed:

      (use "git rm --cached <file>..." to unstage)

    	new file:   README.md

    



> Sin embargo hay que recordar que `git add [archivo]` no afecta al repositorio de manera permanente porque los cambios no se registran realmente hasta que los confirmen (commit).

### 8. Commit de los cambios de los archivos.
Ingresar `git commit`, se abrira el editor de condigo default, escribe el mensaje de confirmación ***"Hola mundo soy [nombre_completo], este es mi primer commit."***
Ahora confirmamos (commit) los cambios, el equivalente a "Guardar" en Git. 


```C#
git commit
```

    [master (root-commit) 77d2cca] Hola mundo soy nombre_completo, este es mi primer commit.

     1 file changed, 1 insertion(+)

     create mode 100644 README.md



>  Cada commit tiene un mensaje de confirmación asociado. Un mensaje de confirmación es un mensaje de registro del usuario que describe los cambios.

### 9. Subir como evidencia el repositorio en el GitHub proporcionado.

Se generara un repositorio para la entrega de esta actividad
[Repositorio GitHub Classroom](https://classroom.github.com/a/pEFJ147b). 

Siga las instrucciones:

```
git remote add origin https://github.com/ITIC-ITESME/mi-primer-repositorio-[tu-usuario].git
git branch -M main
git push -u origin main
```
