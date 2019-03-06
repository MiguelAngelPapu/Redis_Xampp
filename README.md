# Instalación de Redis

[Entra ha esta url]: https://github.com/MicrosoftArchive/redis/releases	"Descargar la versión (3.2.100)"

------
![Instaladores](C:\Users\Miguel\Desktop\Instaladores.png)

------
## Tabla de contenido

| Archivos | Descripcion |
| ----------------------------------------------------- | -------------------- |
| ![Servidor](C:\Users\Miguel\Desktop\Servidor.png)                                                  | Este archivo contiene el servidor de redis y el cliente |
| ![Windows](C:\Users\Miguel\Desktop\Windows.png) | El ejecutable sirve para arrancar el servidor de redis desde Windows |

## Contenido del archivo 'Redis-x64-3.2.100.zip'

| #    | Pasos | Img |
| ---- | ----- | ----- |
|  1  | Crear una carpeta con el nombre 'Redis' en la unidad de disco principal  C:\ | ![Sitio](C:\Users\Miguel\Desktop\Sitio.png) |
| 2 | Extraer el contenido del archivo Redis-x64-3.2.100.zip dentro de la carpeta Redis | ![Extraer](C:\Users\Miguel\Desktop\Extraer.png) |

## Servidor de redis 'redis-server.exe'

![Redis server](C:\Users\Miguel\Desktop\redis_server.png)

------

![Puerto redis](C:\Users\Miguel\Desktop\Puerto_redis.png)

------

[^Nota]: NO CERRA LA CONSOLA DEL SERVIDOR  DE REDIS 'Para utilizar el cliente de redis tiene que estar ejecutando el servidor. Mas adelante configuraremos una variable del sistema de windows para no inicializar dos terminales'

------

## Cliente de redis 'redis-cli.exe'

![Redis cliente](C:\Users\Miguel\Desktop\redis_cli.png)

------

![Ip redis](C:\Users\Miguel\Desktop\Ip_redis.png)

```tex
//Ejecutar este framento de codigo para verificar si esta todo bien con el servidor
ping
```

![Conexion con redis](C:\Users\Miguel\Desktop\Conexion_redis.png)

------

## Versión de redis y del php

```tex
//Ejecutar este framento de codigo para saber la version de redis
info
```

![Versión de redis](C:\Users\Miguel\Desktop\Vercion_de_redis.png)

------

```php
<?php
    //Ejecutar este framento de codigo para saber que vercion de php estamos usando
    //Para descargar el ddl correspondiente
    echo phpinfo();
?>
```
![Vercion del php](C:\Users\Miguel\Desktop\Vercion_del_php.png)

------

[^Nota]: Descargar el dll según la version del Redis y PHP obtenida en las instrucciones dadas anteriormente.

# Instalación del dll para Xampp

[Entra ha esta url]: https://pecl.php.net/package/redis	"Descargar la extensión del xampp según la versión del redis y del php "

![Vercion del redis](C:\Users\Miguel\Desktop\ddl.png)

------

![Vercion del php](C:\Users\Miguel\Desktop\ddl2.png)



------

## Tabla de contenido dll

| Archivos | Descripcion |
| ----------------------------------------------------- | -------------------- |
| ![DDL](C:\Users\Miguel\Desktop\ddl3.png)                                                  | Este archivo contiene el ddl que nesecita el xampp para ejecutar los comados con php |

------

## Contenido del archivo 'php_redis-3.1.6-7.2-ts-vc15-x64'

| #    | Pasos | Img |
| ---- | ----- | ----- |
|  1  | Extraemos el el contenido y sacamos el dll | ![DDL](C:\Users\Miguel\Desktop\xampp.png) |
| 2 | Vamos a las extensiones del php en la carpeta xampp y alojamos el dll en la carpeta ext donde se encuentran todas las librerías de trabajo en php. El folder se encuentra en la ruta de instalación de Xampp (C:\xampp\php\ext) | ![DDL php](C:\Users\Miguel\Desktop\xampp_ddl.png) |
| 3 | Nos dirigimos al archivo php.ini para habilitar la extension del dll este se encuentra en el panel del xampp | ![php.ini](C:\Users\Miguel\Desktop\php_ini.png) |
| 4 | En el archivo php.ini copia y pega el nombre del dll con el atributo **extension=php_redis.dll** y guardamos | ![Extecion DDL](C:\Users\Miguel\Desktop\php_ini_ddl.png) |

[^Nota]: Reinicie el xampp para resetear la configuración. 

------
## Librería de redis 'php'

[Entra ha esta url]: https://github.com/nrk/predis	"Descargar la librería del php "

------
![Libreria php](C:\Users\Miguel\Desktop\libreria_php.png)

## Tabla de contenido

| Archivos | Descripcion |
| ----------------------------------------------------- | -------------------- |
| ![Libreria](C:\Users\Miguel\Desktop\libreria_php2.png)                                                  | Este archivo contiene la librería para utilizar en el sitio web 'php' |

------

## Contenido del archivo 'predis-1.1.zip'

| #    | Pasos | Img |
| ---- | ----- | ----- |
|  1  | Creamos una carpeta **prueba_redis** en el document root del xampp (C:\xampp\htdocs) | ![Sitio web](C:\Users\Miguel\Desktop\htdocs.png) |
| 2 | Dentro de la carpeta **prueba_redis** extraemos el contenido de archivo **predis-1.1.zip** | ![Sitio web libreria](C:\Users\Miguel\Desktop\htdocs2.png) |
| 3 | Creamos un archivo llamado **index.php** dentro de la carpeta **prueba_redis** | ![Sitio web index.php](C:\Users\Miguel\Desktop\htdocs3.png) |

## Ejecutamos la conexion con redis

[^Nota]: Abrimos un editor de texto favorito y colocamos el codigo de conexion

```php
<?php
    //Requerimos la libreria del php
    require 'predis-1.1/src/Autoloader.php';
    Predis\Autoloader::register();
    $conexion = new Predis\Client([
        'scheme' => 'tcp',
        'host'   => '127.0.0.1', //El host se cambia segun el redis-cli.exe
        'port'   => 6379,//El puerto por defecto redis-server.exe
    ]);
	//Comprobamos conexion
    echo "Conexion: ". $conexion->ping();//En la pagina web tiene que retornar un 'PONG'

	//El servidor del redis 'redis-server.exe' tiene que estar en ejecucion para la conexion con el php
?>
```

------
![Conexion](C:\Users\Miguel\Desktop\Conexion.png)

------

[^Nota]: Para mas información de los comandos con redis [https://github.com/nrk/predis]()

