## ¿Por donde empiezo?

No es un sistema de virtualización.

[Docker] es un sistema de contenedores ligeros y portables(independiente del sistema operativo), para evitar el problema de "en mi máquina si funciona", para tener el mismo entorno en todos los ambientes(desarrollo, qa, producción).

## ¿Qué ventajas tiene?

* **Flexible** Las aplicaciones más complejas pueden ser almacenadas en contenedores.
* **Ligero**
* **Intercambiable** Permite implementar actualizaciones sin ser tan tediosas.
* **Portatil**
* **Escalable** Se puede aumentar y distribuir las distintas réplicas de los contenedores.
* **Apilable** Se van apilando según sea necesario, tu proyecto puede que en un primer momento no necesite de un contenedor, luego puede que surja la necesidad orquestandolo con otros contenededores.

## ¿Que diferencia tiene con una máquina virtual?
El peso por lo ligero que es y esto se ve reflejado en el consumo de recursos de la máquina host, puedes tener muchos contenedores orquestados sin que se note el consumo de recuros.

## ¿Cómo funciona Docker?
* **Cliente** Es la forma como te vas a comunicar con tu *`docker-host`* (imágenes y contenedores locales), vas a poder contruir(build), descargar(pull) y ejecutarlas creando los contenedores(run).
* **Docker Host** Registry local.
* **Registry** Es un repositorio donde se encuentran las imágenes por defecto que suele ser *`Docker-hub`*.

![Arquitectura de Docker](docker-architecture-609x270.webp)

### Comandos iniciales de Docker

* `docker container run ubuntu echo hola mundo` 

    * Crear un contenedor a partir de la imagen ubuntu y muestra el mensaje `hola mundo` por consola.

* `docker ps`
* `docker conatiner ls`
    * Ambos comandos listan los contenedores activos en ese momento.

* `docker ps -a`
* `dokcer container ls -a`
    * Ambos comandos listan todos los contenedores.

## Docker CLI

Muestra por pantalla la versión con la que se está trabajando.

    docker -version
    docker -v
    docker version

Muestra el listado todos los posibles comandos.  
    
    docker --help

Muestra la info de docker en formato json

    docker info --format '{{json .}}'
    docker info -f '{{json .}}'

Envía la info de json a un archivo

    docker info --format '{{json .}}' > docker-config.json

Busca un contenedor 

    docker search
    