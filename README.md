## DAW 1er Trimestre
### Repositorio del examen de Despliegue de aplicaciones web del primer trimestre

Este repositorio es el resultado del examen de los alumentos de la academia Agil de Castellón. Cursando el módulo Desarrollo de Aplicaciones Web en primera trimestre del segundo curso.
El examen consta de 4 partes de temario claramente diferenciadas y puntuadas en el examen que son: ***Markdown***, ***Apache***, ***Comandos SSH*** y ***GitHub***.
Los alumnos tuvimos un máximo de 3horas y media para realizar los 4 ejercicios propuesto por el profesor.

#### Indice y Puntuaciones del examen
* Realiza el test asignado (3 puntos).

* SSH + Command line (3 puntos).

* Virtualhost (2 puntos)

* Documentación + Github (2 puntos)

  ___

  
## Ejercicio 2

1. **ssh usuario@192.168.0.185** --- *Conectamos a la máquina remota facilitada por el profesor*
2. **usuario@192.168.0.185's password:** --- *Introducimos la contraseña que puso en la pizarra*
3. **touch  "/home/usuario/Escritorio/joseluismartinez.txt"** --- *Creamos el archivo con nuestro nombre en el Escritorio de la máquina del profesor*
4. **usuario@usuario-OptiPlex-380:~/Escritorio$ whoami     usuario** --- *Utilizamos el comando whoami para saber cual es mi usuario*
5. **usuario@usuario-OptiPlex-380:~/Escritorio$ nano "/home/usuario/Escritorio/joseluismartinez.txt"** --- *Utilizamos el editor nano para editar el archivo creado y poner usuario who *
6. **usuario@usuario-OptiPlex-380:~/Escritorio$ echo 'who'> joseluismartinez.txt** --- Metemos dentro del archivo el resultado de who

   
![imagen](https://github.com/user-attachments/assets/b1def598-b43e-437b-b218-9ccf7fcba614)
![imagen](https://github.com/user-attachments/assets/5f2be482-b839-40d1-b80c-b06fcf32dfe6)
![imagen](https://github.com/user-attachments/assets/154cd242-def9-43f9-9e1c-d4caa9adf57c)

___

## Ejercicio 3

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

___

Bibliografia

[digitalocean - tutorial apache](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04-es?authuser=0)  
[digitalocena - tutorial SSH](https://www.digitalocean.com/community/tutorials/how-to-use-ssh-to-connect-to-a-remote-server-es?authuser=0)  
[hostinger - comandos SSH](https://www.hostinger.es/tutoriales/linux-comandos?authuser=0)  











