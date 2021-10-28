# FastAPI-MySQL

**Proyecto de prueba de un API server con FastAPI y MySQL**


En esta prueba, uso el SO Linux CentOS 7, con Apache y MySQL instalado y Python 3.6.7. Entonces: 

1. Instalar los modulos: FastAPI, pymysql, uvicorn, gunicorn entre otros, ya veremos
```
# Pip3 install fastapi pymysql uvicorn gunicorn
```

2. Crear un virtual environment. Yo lo hice en `/opt/fastapi-mysql`
```
# Cd /opt
# Mkdir fastapi-mysql
```
2.1. Con el comando Python3 –m venv [nombre subdir del venv], por ejemplo:
```
# python3 –m venv env
```
Esto crea una estructura de subdirectorios dentro de la carpeta

2.2. Activo el ambiente de desarrollo virtual o virtual environment
```
# . env/bin/actívate
```
Me aparecerá `(env)` en la línea de comandos, haciéndonos saber que estamos en el virtual environment. Para salir, usaremos el comando `deactivate`

2.3 Instalo las dependencias:
```
(env) # pip install pymysql
(env) # pip install uvicorn
(env) # pip install gunicorn
```
Adv! Puede ser que le pida actualizar pip a la última versión. Para esto, ejecutaremos:
```
(env) # pip install –upgrade –pip
```
Para mi proyecto de prueba, también tuve que instalar otros módulos como: `sqlalchemy, cryptography, uvloops, httptools`

**Puesta en marcha - Producción**

Mas allá de que es un proyecto, es importante saber cómo hacer para que realmente se ejecute al iniciar el servidor. En este caso CentOS 7

Se debe crear un archivo en la carpeta /etc/systemd/system
En este caso lo llamo `fastapi-mysql.service`

El archivo es el que figuro en la raíz del repositorio