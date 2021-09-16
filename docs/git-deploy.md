---
title: Git deploy
slug: /git-deploy
---

## Introducción
Esta guia esta diseñada para la configuración de git en el servidor para para el proceso de despliegue ``(deployment)``

## Requisitos mínimos:

La versión minima de git en la que debe estar el servidor es `2.33.0`

```shell
$ git --version
```

## Estructura de ramas

El proyecto de aviatur contempla una estructura de ramas como en este ejemplo:

```shell
aviatur-project/
  |--pruebas
  |
  |--release
  |
  |--hotfix
  |
  |--master
  |
  |--development
  |  |--other-branches
  |

```
## Configración inicial de repositorio remoto de Git
Para configurar inicialmente cualquier servidor Git, debe exportar un repositorio existente a un nuevo repositorio desnudo, un repositorio que no contiene un directorio de trabajo. Por lo general, esto es sencillo de hacer. Para clonar su repositorio para crear un nuevo repositorio desnudo, ejecute el comando clone con la opción --bare. Por convención, los nombres de directorios de repositorios simples terminan con el sufijo .git, así:
```
git clone --bare my_project my_project.git
Cloning into bare repository 'my_project.git'...
done.
```
o en el git aviatur

```
$ git clone http://tikan01:8080/tfs/DefaultCollection/Aviatur_COM/_git/aviatur.com
```
Ahora debería tener una copia de los datos del directorio Git en su directorio my_project.git.

## Repositorio de estación de trabajo local

En este punto, otros usuarios que tienen acceso de lectura basado en SSH al directorio / srv / git en ese servidor pueden clonar su repositorio ejecutando:

```
$ git clone http://tikan01:8080/tfs/DefaultCollection/Aviatur_COM/_git/aviatur.com
```

Git agregará automáticamente permisos de escritura de grupo a un repositorio correctamente si ejecuta el comando git init con la opción --shared. Tenga en cuenta que al ejecutar este comando, no destruirá ninguna confirmación, referencia, etc. en el proceso.

## Subir cambios

Luego, John, Josie o Jessica pueden enviar la primera versión de su proyecto a ese repositorio agregándola como control remoto y subiendo una rama. Tenga en cuenta que alguien debe ingresar a la máquina y crear un repositorio simple cada vez que desee agregar un proyecto. Usemos gitserver como el nombre de host del servidor en el que configuró su usuario y repositorio de git. Si lo está ejecutando internamente y configura DNS para que gitserver apunte a ese servidor, entonces puede usar los comandos prácticamente tal como están (asumiendo que myproject es un proyecto existente con archivos):
```
# on John's computer
$ cd myproject
$ git init
$ git add .
$ git commit -m 'Initial commit'
$ git remote add origin git@gitserver:/srv/git/project.git
$ git push origin master
```

## Referencias

Todas las practicas de uso de git para proceso de despliegue en servidores fueron consultadas desde la documentación de git
- https://git-scm.com/book/en/v2/Git-on-the-Server-The-Protocols
- https://git-scm.com/book/en/v2/Git-on-the-Server-Getting-Git-on-a-Server
- https://git-scm.com/book/en/v2/Git-on-the-Server-Generating-Your-SSH-Public-Key
- https://gist.github.com/cjsteel/5bdab49c97ecacb67904056ccdcb956d
