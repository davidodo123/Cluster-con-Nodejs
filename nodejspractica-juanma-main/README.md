# Desplliegue cluster con NodeJS y Express #
    - Lo primero que vamos ha hacer es intalar nodejs ya que no esta instalado.
![Instalar Node.js](assets/img/instalarnodejs.png)

## Proyecto Sin cluster ##
- Hay que crear una carpeta para el proyecto, se inicia con npm init para crear una estructura de carpetas automaticamente.
![Creamos carpeta y hacemos un init](assets/img/init.png)
- Se Hace un npm install expres para instalar el proyecto: 
![Descargamos Express](assets/img/express.png)
- Despues de esto creamos con nano un archivo app.js y añadimos el siguiente contenido y se ejecuta node:
![Datos de la aplicación](assets/img/aplicacionDatos.png)
-En mi caso, sale un error, que sucede por que la instalacion de node es una version antigua, sale por predeterminado, asi que busco la version mas reciente
    - Borrar node.
    ![Borrar Node](assets/img/BorrarNode.png)
    - Reinstalarlo, con una version mas actual 
    ![Reinstalar](assets/img/Reinstalar.png)
    - Comprobamos
    ![Comprobamos versiones ](assets/img/comprobamos.png)
    - Borramos expres por si da fallos
    ![Borrar expres y instalarlo](assets/img/borramosexpress.png)
- Ya funcionaria y estaria la aplicacion escuchando por el puerto dicho "3000", para acceder tenemos que saber la ip y poner :3000
![Hello world](assets/img/Helloworld.png)
![Final Count](assets/img/finalcount.png)
![Final Count mas grande](assets/img/finalmasgrande.png)
-Vemos el tiempo que tarda, y a la vez abrimos otra pagina para ver como el valor sube 
![Tiempo del n mas grande](assets/img/tiempo1.png)
![Tiempo de la otra pagina](assets/img/tiempo2.png)
Como se ejecuta como unico proceso, sale asi.

## Con cluster
- Creamos el archivo con nano y añadimos lo siguiente 
![Segunda App](assets/img/segundaapp.png)
- Ejecutamos la app 
![Ejecutamos segunda App](assets/img/Ejecutamos2app.png)
- Comprobamos otra vez los tiempos.
![Lenta](assets/img/lenta.png)
![Rapida](assets/img/rapida.png)
(Esto es debido a que se crean varios procesos workers que comparten el mismo puerto, y las peticiones se distribuyen entre ellos, permitinedo atender a multiples solicitudes evitando bloqueos)