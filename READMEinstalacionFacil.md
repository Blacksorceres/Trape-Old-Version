# Trape-Old-Version
Este es Trape original de @jofpin , esta es la version 1.0 esta no requiere (api"s)
--------------------------------------------------------------------------------------------------------------
Si usted esta en kali linux o tenga problemas con "pip" talvez necesite hacer esto :

(como root)
nano /etc/apt/sources.list.d/inestables.list
(inestables.list es un archivo que crearemos para los sources pero dejando los originales en sources.list sin tocar )
dentro :de /etc/apt/sources.list.d/inestables.list

#debian

deb https://deb.debian.org/debian buster main

deb-src https://deb.debian.org/debian buster main

deb https://deb.debian.org/debian buster-updates main

deb-src https://deb.debian.org/debian buster-updates main
-------------------------------------------------------------------
ya sabes : 
apt update -y
sudo apt install python-all-dev python-setuptools python-wheel -y

si hay conflictos : descargue el .deb de la version que ese pip necesita...

https://packages.debian.org/buster/all/python-pip-whl/download

dpkg -i elarchivo.deb

luego de esto ahora si :
sudo apt -y install python-pip

listo ya esta pip para python 2 ... que es lo que usa trape ... y muchas herramientas mas,
suerte...

