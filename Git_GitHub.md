# Git/GitHub

## ¿Qué es Git?

Es un **Sistema de Control de Versiones** (VCS) para seguir los cambios en los archivos.

* Control de version distribuido
* Coordina el trabajo entre multiples desarrolladores
* Monitoreo de quien y cuando hizo cambios
* Opción a revertir cambios
* Repositorios locales y remotos

## Comandos Básicos

* `git init` *crea un archivo oculto git en el directorio elegido*
* `git add nomarchivo` *asigna un archivo del working directory al staging area*
* `git status` *verifica el estado de los archivos del directorio elegido*
* `git commit -m "Descripción de Cambios Realizados"` *crea un snapshot/instantanea del staging area*
* `git remote add origin direccionrepo` *declaración de ruta del repositorio*
* `git push -u origin master` *sube archivos al repositorio remoto*
* `git pull` *recupera los cambios de multiples desarrolladores*
* `git clone direccionrepo` *crea una copia local de un repositorio remoto*
* `git log` *permite la visualizacion de cambios con datos de persona y fecha*
* `git checkout -- nomarchivo` *revierte los cambios realizados hasta antes de ejecutar commit*
* `git diff nomarchivo` *muestra explicitamente los cambios realizados*
* `git branch nomrama` *crea una rama nueva/version*
* `git checkout nomrama` *cambia a la rama seleccionada*



## Estructura 

Git se compone por tres bloques o estados *working directory, staging area y repository*.

* **Working Directory.** Es donde se localizan los archivos de prototipado.
* **Staging Area.** Es donde se asignan los archivos previos a subir al repositorio.
* **Repository.** Es donde se alojan finalmente los archivos elegidos para la versión de control.

## Entorno de Trabajo

Para empezar a trabajar con Git es necesario instalar los componentes Git https://git-scm.com , así como crear una cuenta en GitHub https://github.com

[![Git/GitHub, Curso Páctico](http://img.youtube.com/vi/HiXLkL42tMU/0.jpg)](https://www.youtube.com/watch?v=HiXLkL42tMU "Tutorial Markdown")



