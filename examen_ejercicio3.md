# Examen DAW 1ºtrimestre
## Ejercicio 2

1. **sudo ufw allow 'Apache'** --- Abro el puerto 80 para poder trabajar con el tráfico no cifrado
2. **sudo ufw status** --- Verifico que este abierto el puerto
3. **sudo systemctl start apache2** --- Activo el servidor apache
4. **joseluis@usuario-OptiPlex-380:~$ sudo mkdir /var/www/miWeb** --- Creo la carpeta miWeb
5. **joseluis@usuario-OptiPlex-380:~$ sudo chown -R $joseluis:$joseluis /var/www/miWeb** --- Otorgo la propiedad de la carpeta al usuario joseluis
6. **root@usuario-OptiPlex-380:/home/joseluis# ls /var/www/miWeb
index.html** --- Hago un ls para ver que archivos hay dentro de la carpeta, esta el index.html
7. **root@usuario-OptiPlex-380:/home/joseluis# sudo nano /var/www/miWeb/index.html** --- Modifico el archivo con el editor nano para poner la frase: *Success! miWeb virtual host is working!*
8. **root@usuario-OptiPlex-380:/etc/apache2# cd /etc/apache2/sites-available** --- Entro en la carpeta sites-available y hago un ls para ver lo que contiene
9. **root@usuario-OptiPlex-380:/etc/apache2/sites-available# sudo cp 000-default.conf miWeb.conf** --- Pongo el archivo miWeb.conf
10. **root@usuario-OptiPlex-380:/etc/apache2/sites-available# sudo a2ensite miWeb.conf
Enabling site miWeb.conf** --- Activo el sitio miWeb.conf
11. **To activate the new configuration, you need to run:
  systemctl reload apache2** --- Recargo apache para que me actualice los cambios
12. **root@usuario-OptiPlex-380:/etc/apache2/sites-available# ifconfig** --- Verifico la ip de mi ordenador
13. **root@usuario-OptiPlex-380:/etc/apache2/sites-available# sudo nano miWeb.conf** --- Entro al archivo, modifico server admin y documentRoot, luego añado ServerName y ServerAlias
14. **Abro un explorador y pongo la url www.daw.ejercicio3.com** --- Se abre mi servidor apache con el html que he creado en index.html


![imagen](https://github.com/user-attachments/assets/9d1fee75-d881-4365-8322-088b7ccd82a0)
![imagen](https://github.com/user-attachments/assets/4e423345-7778-4cb8-b4f5-22752802ec88)






