# Tarea03-Docker

Empezamos instalando alpine 3.22 para esto hay que usar el siguiente comando:

docker pull alpine:3.22  -->  descargar alpine 3.22 sin crear contenedor

![captura](/Capturas/Captura1.png)

Luego revisamos si esta instalado con el comando:
docker images -->  revisamos que tenemos alpine 3.22 instalado

![captura](/Capturas/Captura2.png)

Después de esto creamos el docker sin nombre y sin iniciarlo con el siguiente comando
docker create alpine:3.22 --> creamos el docker sin iniciarlo y sin nombre

![captura](/Capturas/Captura3.png)

Luego con este oro comando podremos comrobar que se ha creado
docker ps -a --> nos enseña todos los dockers, el -a nos permite ver los inactivos

![captura](/Capturas/Captura4.png)


Con este otro comando inciamos y creamos un docker con el nombre dam_alp1 con sh

docker run -it --name dam_alp1 alpine:3.22 sh --> creamos el docker
--name --> indica el nombre que le ponemos
sh --> para indicar que lo hacemos con shell 
it --> nos permite escribir dentro desde la terminal

![captura](/Capturas/Captura5.png)

Hacemos un ip a y esta seria su ip

![captura](/Capturas/Captura6.png)


Una vez hecho el ping a google veremos que si funciona 

![captura](/Capturas/Captura7.png)

Al hacer el ping al otro docker, creado con el mismo comando de antes,
veremos que por el nombre va a dar error, pero con la ip todo funcionara perfectamente

![captura](/Capturas/Captura9.png)
![captura](/Capturas/Captura10.png)

Para ver el almacenamiento tenemos que usar este comentario y quedaria asi

docker stats --> te permite ver el espacio de almacenamiento

![captura](/Capturas/Captura11.png)

Una vez haber entrado en los dockers y haber salido usando exit, apagando el docker,
veremos que no hay ninguna diferencia

![captura](/Capturas/Captura12.png)

Para ver cuantas imagenes y containers tenemos usaremos el siguiente comando, tambien nos dira el uso del disco
docker system df --> muestra la cantidad de imagenes y containers que hay el df indica el uso de disco

![captura](/Capturas/Captura13.png)


##Posible error 

Cada vez que crees un docker hay que especificar la version de alpine ya que si no lo haces y simplemente pones 
alpine se instalara y usara la ultima version, aunque esto no sea un error es algo que hay que tener en cuenta.
