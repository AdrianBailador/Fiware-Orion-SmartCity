Fiware-Orion

1. vamos a actualizar la base de datos de paquetes:

sudo apt-get update

2. Ahora vamos a instalar Docker. Agregue la clave GPG para el repositorio oficial de Docker al sistema:

sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D

3. Agregue el repositorio Docker a fuentes APT:

sudo apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'

4. Actualice la base de datos de paquetes, con los paquetes Docker desde el repositorio recién agregado:

sudo apt-get update

5. Asegúrese de que está a punto de instalar desde el repositorio de Docker en lugar del repositorio predeterminado de Ubuntu 16.04:

apt-cache policy docker-engine

6. Por último, instale Docker:

sudo apt-get install -y docker-engine

7. Docker ahora debe estar instalado, el daemon iniciado, y el proceso habilitado para iniciar en el arranque. Compruebe que se está ejecutando:

sudo systemctl status docker

8. Para comprobar si puede acceder y descargar imágenes de Docker Hub, escriba:

docker run hello-world
