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
8. 

