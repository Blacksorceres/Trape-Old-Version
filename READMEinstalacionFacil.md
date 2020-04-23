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

ingrese a la carpeta trape e instale :

pip -r requirements.txt

inmediatamente :

pip install flask
pip install flask_socketio
pip install eventlet

(o use todo en una sola linea luego de pip install)

Nota: 
requiere nrgok ;
abra una cuenta en la opagina ngrok y use su tokken como explica ahi,luego haga ngrok global desde su carpeta de descragas:
sudo cp ngrok /usr/bin/ngrok && chmod a+x ngrok 

ejemplo:
nrgok http 8080 

y en trape use :

python trape.py -u https://www.youtube.com/watch?v=4L_yCwFD6Jo -p 8080 

(donde el mismo puerto dirija a localhost :recordemos que nrgok sera el tunel a este, y donde url youtube use su favorita)

listo ya esta pip para python 2 ... que es lo que usa trape ... y muchas herramientas mas,
suerte...

