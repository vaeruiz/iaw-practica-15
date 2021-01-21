# Instalación de Wordpress a través de contenedores Docker

Creando un sitio Wordpress utilizando el sistema de contenedores de Docker.

## Instalando docker y docker-compose

Para instalar ambas utilidades tenemos que ejecutar el siguiente comando:

>apt install docker docker-compose

Cuando se descargue, cada vez que las queramos utilizar deberá de ser con el comando sudo, para evitar esto, tenemos que meter al usuario en el grupo de usuarios de Docker, esto se hace con la siguiente instrucción:

>sudo usermod -aG docker $USER

Después de esto, tenemos que habilitar el servicio docker para que se arranque cada vez que iniciemos el sistema, para ello ejecutamos este comando:

>sudo systemctl enable docker

Ahora reiniciamos la máquina haciendo un reboot y podremos empezar a utilizar docker con total normalidad.

## Utilizando docker-compose

Con docker-compose podemos crear un archivo de configuración en el que podemos reflejar los contenedores que queremos utilizar y sus parámetros necesarios (puertos, volúmenes que tenemos que utilizar, redes, etc).

De esta forma cuando queramos poner en funcionamiento toda nuestra infraestructura, solo tendremos que llamar al archivo de configuración que hemos creado, en el repositorio se encuentra el archivo que he utilizado.

El comando para llamar al archivo de configuración y ponerlo todo en marcha es el siguiente:

>docker-compose up -d

Después de ejecutarlo, el sistema se encarga de obtener las imágenes y aplicar las configuraciones correspondientes a los contenedores de docker.

## Demostración

Aquí se ven unas capturas de la infraestructura en marcha:

