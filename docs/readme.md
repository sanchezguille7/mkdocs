# Docker Web 2
Es la misma dinámica que [Docker-web](https://github.com/sanchezguille7/docker-web) pero con **Ubuntu 23.04**
Este proyecto consiste en crear un contenedor **Docker** que ejecuta una aplicación del juego **2048** en un servidor **Apache**. Utiliza un archivo Dockerfile para construir la imagen del contenedor y un archivo docker-compose.yml para definir y configurar el entorno de ejecución.

  

## Archivos:

**Dockerfile**: Este archivo define cómo se construirá la imagen del contenedor **Docker**. Utiliza una imagen base de **Ubuntu 23.04**, instala **Git** y **Apache2**, clona el repositorio de la aplicación **2048** desde **GitHub**, mueve los archivos al directorio de documentos raíz de **Apache** y expone el puerto **80** para que la aplicación sea accesible desde el exterior. Además, define el comando para iniciar **Apache2** en primer plano.

  ![2048](images/docker.gif)

**docker-compose.yml:** Este archivo describe los servicios para el entorno **Docker** utilizando **Docker Compose**. Define el servicio de **nginx** que construye la imagen a partir del directorio *./app* mapea el puerto **80** del contenedor al puerto **80** del host, y establece que el servicio se reinicie automáticamente en caso de fallo.

  

### Instrucciones de Uso:
1. Clona este repositorio en tu máquina local.
2. Asegúrate de tener **Docker** y **Docker Compose** instalados en tu sistema.
3. En la terminal, navega hasta el directorio del proyecto clonado.
4. Ejecuta el siguiente comando para construir y ejecutar los contenedores:
    docker-compose up --build
    
5. Una vez que los contenedores estén en ejecución, abre un navegador web y visita http://localhost para jugar al juego **2048**.

![2048](images/2048.gif)
