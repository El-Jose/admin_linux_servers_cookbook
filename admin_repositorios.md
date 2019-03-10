# Añadir y administrar repositorios en Linux

Un repositorio es una listado de paquetes oficiales para una distribucion.
Para distribuciones basadas en Debian como Ubuntu server el listado de repositorios se encuentra en:*/etc/apt/source.list*

# Añadiendo el repo de Mongodb
## Agregando la llave publica
APT posee una herramienta llamada apt-key que nos ayuda a manejar con facilidad las llaves de seguridad de nuestros repositorios. vamos a agregar la llaver para Ubuntu 16.04:

```
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB4NF368818C72E52529D4
```
## Creando un list file para Mongodb
```
echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu xenial/mongodb-org/4.0 multiverse"  | sudo tee /etc/apt/sources.list.d/mongodb-org-4.0.list
```
## Recargar base de datos local de paquetes
Una vez creado el fichero se actualiza la base de datos de APT
```
sudo apt-get update
```
Ya con esos pasos podemos instalar libremente el paquete de Mongodb en nuestro local
