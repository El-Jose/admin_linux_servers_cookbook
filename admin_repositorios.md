#Añadir y administrar repositorios en Linux

Un repositorio es una listado de paquetes oficiales para una distribucion.
Para distribuciones basadas en Debian como Ubuntu server el listado de repositorios se encuentra en:*/etc/apt/source.list*.

#Añadiendo el repo de Mongodb
##Agregando la llave publica
APT posee una herramienta llamada apt-key que nos ayuda a manejar con facilidad las llaves de seguridad de nuestros repositorios. vamos a agregar la llaver para Ubuntu 16.04:

'''
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 9DA31620334BD75D9DCB4NF368818C72E52529D4
'''

