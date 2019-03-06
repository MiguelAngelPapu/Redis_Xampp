>Un poco de historia ¿Que es redis? https://es.wikipedia.org/wiki/Redis
# Instalación de Redis

> Entrar ha esta url: https://github.com/MicrosoftArchive/redis/releases "Descargar la versión (3.2.100)"

------
![Instaladores](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Instaladores.png)

------
## Tabla de contenido

| Archivos | Descripcion |
| ----------------------------------------------------- | -------------------- |
| ![Servidor](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Servidor.png)                                                | Este archivo contiene el servidor de redis y el cliente |
| ![Windows](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Windows.png) | El ejecutable sirve para arrancar el servidor de redis desde Windows |

## Contenido del archivo 'Redis-x64-3.2.100.zip'

| #    | Pasos | Img |
| ---- | ----- | ----- |
|  1  | Crear una carpeta con el nombre 'Redis' en la unidad de disco principal  C:\ | ![Sitio](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Sitio.png) |
| 2 | Extraer el contenido del archivo Redis-x64-3.2.100.zip dentro de la carpeta Redis | ![Extraer](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Extraer.png) |

## Servidor de redis 'redis-server.exe'

![Redis server](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/redis_server.png)

------

![Puerto redis](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Puerto_redis.png)

------

> NO CERRA LA CONSOLA DEL SERVIDOR  DE REDIS 'Para utilizar el cliente de redis tiene que estar ejecutando el servidor. Mas adelante configuraremos una variable del sistema de windows para no inicializar dos terminales'

------

## Cliente de redis 'redis-cli.exe'

![Redis cliente](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/redis_cli.png)

------

![Ip redis](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Ip_redis.png)

```tex
//Ejecutar este framento de codigo para verificar si esta todo bien con el servidor
ping
```

![Conexion con redis](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Conexion_redis.png)

------

## Versión de redis y del php

```tex
//Ejecutar este framento de codigo para saber la version de redis
info
```

![Versión de redis](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Vercion_de_redis.png)

------

```php
<?php
    //Ejecutar este framento de codigo para saber que vercion de php estamos usando
    //Para descargar el ddl correspondiente
    echo phpinfo();
?>
```
![Vercion del php](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Vercion_del_php.png)

------

> Descargar el dll según la version del Redis y PHP obtenida en las instrucciones dadas anteriormente.

# Instalación del dll para Xampp

> Entrar ha esta url: https://pecl.php.net/package/redis "Descargar la extensión del xampp según la versión del redis y del php "

![Vercion del redis](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/ddl.png)

------

![Vercion del php](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/ddl2.png)



------

## Tabla de contenido dll

| Archivos | Descripcion |
| ----------------------------------------------------- | -------------------- |
| ![DDL](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/ddl3.png)                                                  | Este archivo contiene el ddl que nesecita el xampp para ejecutar los comados con php |

------

## Contenido del archivo 'php_redis-3.1.6-7.2-nts-vc15-x64'

| #    | Pasos | Img |
| ---- | ----- | ----- |
|  1  | Extraemos el el contenido y sacamos el dll | ![DDL](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/xampp.png) |
| 2 | Vamos a las extensiones del php en la carpeta xampp y alojamos el dll en la carpeta ext donde se encuentran todas las librerías de trabajo en php. El folder se encuentra en la ruta de instalación de Xampp (C:\xampp\php\ext) | ![DDL php](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/xampp_ddl.png) |
| 3 | Nos dirigimos al archivo php.ini para habilitar la extension del dll este se encuentra en el panel del xampp | ![php.ini](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/php_ini.png) |
| 4 | En el archivo php.ini copia y pega el nombre del dll con el atributo **extension=php_redis.dll** y guardamos | ![Extecion DDL](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/php_ini_ddl.png) |

> Reinicie el xampp para resetear la configuración. 

------
## Librería de redis 'php'

> Entrar ha esta url: https://github.com/nrk/predis "Descargar la librería del php "

------
![Libreria php](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/libreria_php.png)

## Tabla de contenido

| Archivos | Descripcion |
| ----------------------------------------------------- | -------------------- |
| ![Libreria](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/libreria_php2.png)                                                  | Este archivo contiene la librería para utilizar en el sitio web 'php' |

------

## Contenido del archivo 'predis-1.1.zip'

| #    | Pasos | Img |
| ---- | ----- | ----- |
|  1  | Creamos una carpeta **prueba_redis** en el document root del xampp (C:\xampp\htdocs) | ![Sitio web](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/htdocs.png) |
| 2 | Dentro de la carpeta **prueba_redis** extraemos el contenido de archivo **predis-1.1.zip** | ![Sitio web libreria](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/htdocs2.png) |
| 3 | Creamos un archivo llamado **index.php** dentro de la carpeta **prueba_redis** | ![Sitio web index.php](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/htdocs3.png) |

## Ejecutamos la conexion con redis

> Abrimos un editor de texto favorito y colocamos el codigo de conexion

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
![Conexion](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Conexion.png)

------

## Redis Base de datos 'comandos'

> Los comandos se ejecutan en el cliente de redis 'redis.cli.exe'

------
| Codigo                                                       | Ejemplo                                                      | Descripcion                                                  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| set  "Nombre de la llave"  "Descripcion de la llave"         | set  "computador" "PC"                                       | Guardar los datos en la ram                                  |
| get "nombre de la llave"                                     | get "computador"                                             | Buscar el dato por la llave                                  |
| keys *                                                       | keys *                                                       | Mostrar todos los datos                                      |
| exists "Nombrede la llave"                                   | exists "computador"                                          | Comprobar si existe un llave con este nombre                 |
| del "Nombrede la llave"                                      | del "computador"                                             | Eliminar el dato por la llave                                |
| mget "Nombrede la llave" "Descripcion de la llave" "Nombre de la llave" "Descripcion de la llave" | mget "computador" "PC" "computador2" "Portatil"              | Guardar varios datos a la vez                                |
| mset "Nombrede la llave" "Nombrede la llave"                 | mset "computador" "computador2"                              | Buscar varios datos por la llave                             |
| hmset "Nombrede la llave" "Nombre de la descripcion del componente" "valor"  "Nombre de la descripcion del componente" "valor" | hmset "computador" "ram" "4gb"  "pantalla" "5.5px" "procesador" "intel core i7" | Guardar datos y el nombre de los componentes y su valor      |
| hmget "Nombrede la llave" "Nombre de la descripcion del componente" "Nombre de la descripcion del componente" | hmget "computador" "ram" "pantalla"                          | Buscar dentro de la llave y de varios componentes            |
| hget "Nombrede la llave" "Nombre de la descripcion del componente" | hget "computador" "ram"                                      | Busca dentro de la llave y el componente                     |
| hgetall "Nombrede la llave"                                  | hgetall "computador"                                         | Buscar por la llave  todos los componentes                   |
| hdel "Nombrede la llave" "Nombre de la descripcion del componente" | hdel "computador" "ram"                                      | Eliminar el componente segun la llave                        |
| lpush "Nombrede la llave" "Subcategoria"                     | lpush "computador" "asus"                                    | Crea un paquete y sus categorias ('Agregar otra subcategoria repetir la llave pero otro subategoria ') |
| rpush "Nombrede la llave" "Subcategoria"                     | rpush "computador" "php"                                     | Crea un paquete y sus categorias ('Agregar otra subcategoria repetir la llave pero otro subategoria ')  NOTA= Nose cual es la diferesncia |
| lrange "Nombrede la llave" 0 1                               | lrange "computador" 0 1                                      | Busca las subcategorias de la llave y mustra los  primeros 0 - 1 |
| lindex "Nombrede la llave" 0                                 | lindex "computador" 0                                        | Busca las subcategoriaspor el indice segun la llave          |
| sadd "Nombrede la llave" "value" "value" "value"             | sadd "celulares" "huawei" "lenovo" "xiaomi"                  | Guarda varios datos a la vez segun la llave                  |
| smembers "Nombrede la llave"                                 | smembers "celulares"                                         | Busca todo los registros segun la llave                      |
| zadd "Nombrede la llave" "value" "Subcategoria"              | zadd "celulares" 3 "huawei"                                  | Guarda la subcategoria y cuantos hay segun la llave          |
| zrange "Nombrede la llave" 0 1                               | zrange "celulares" 0 1                                       | Busca las subcategorias de la llave y mustra los  primeros 0 - 1 |
| zrange "Nombrede la llave" 0 1 withscores                    | zrange "celulares" 0 1 withscores                            | Busca las subcategorias de la llave y mustra los  primeros 0 - 1 y muestra el valor asignado |

> Para mas información de los comandos con redis [https://github.com/nrk/predis]

## Redis Base de datos 'comandos'

> Los comandos se ejecutan el cliente de redis 'redis.cli.exe'

------

| Codigo                                                       | Ejemplo                                                      | Descripcion                                                  |
| :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| set  "Nombre de la llave"  "Descripcion de la llave"         | set  "computador" "PC"                                       | Guardar los datos en la ram                                  |
| get "nombre de la llave"                                     | get "computador"                                             | Buscar el dato por la llave                                  |
| keys *                                                       | keys *                                                       | Mostrar todos los datos                                      |
| exists "Nombrede la llave"                                   | exists "computador"                                          | Comprobar si existe un llave con este nombre                 |
| del "Nombrede la llave"                                      | del "computador"                                             | Eliminar el dato por la llave                                |
| mget "Nombrede la llave" "Descripcion de la llave" "Nombre de la llave" "Descripcion de la llave" | mget "computador" "PC" "computador2" "Portatil"              | Guardar varios datos a la vez                                |
| mset "Nombrede la llave" "Nombrede la llave"                 | mset "computador" "computador2"                              | Buscar varios datos por la llave                             |
| hmset "Nombrede la llave" "Nombre de la descripcion del componente" "valor"  "Nombre de la descripcion del componente" "valor" | hmset "computador" "ram" "4gb"  "pantalla" "5.5px" "procesador" "intel core i7" | Guardar datos y el nombre de los componentes y su valor      |
| hmget "Nombrede la llave" "Nombre de la descripcion del componente" "Nombre de la descripcion del componente" | hmget "computador" "ram" "pantalla"                          | Buscar dentro de la llave y de varios componentes            |
| hget "Nombrede la llave" "Nombre de la descripcion del componente" | hget "computador" "ram"                                      | Busca dentro de la llave y el componente                     |
| hgetall "Nombrede la llave"                                  | hgetall "computador"                                         | Buscar por la llave  todos los componentes                   |
| hdel "Nombrede la llave" "Nombre de la descripcion del componente" | hdel "computador" "ram"                                      | Eliminar el componente segun la llave                        |
| lpush "Nombrede la llave" "Subcategoria"                     | lpush "computador" "asus"                                    | Crea un paquete y sus categorias ('Agregar otra subcategoria repetir la llave pero otro subategoria ') |
| rpush "Nombrede la llave" "Subcategoria"                     | rpush "computador" "php"                                     | Crea un paquete y sus categorias ('Agregar otra subcategoria repetir la llave pero otro subategoria ')  NOTA= Nose cual es la diferesncia |
| lrange "Nombrede la llave" 0 1                               | lrange "computador" 0 1                                      | Busca las subcategorias de la llave y mustra los  primeros 0 - 1 |
| lindex "Nombrede la llave" 0                                 | lindex "computador" 0                                        | Busca las subcategoriaspor el indice segun la llave          |
| sadd "Nombrede la llave" "value" "value" "value"             | sadd "celulares" "huawei" "lenovo" "xiaomi"                  | Guarda varios datos a la vez segun la llave                  |
| smembers "Nombrede la llave"                                 | smembers "celulares"                                         | Busca todo los registros segun la llave                      |
| zadd "Nombrede la llave" "value" "Subcategoria"              | zadd "celulares" 3 "huawei"                                  | Guarda la subcategoria y cuantos hay segun la llave          |
| zrange "Nombrede la llave" 0 1                               | zrange "celulares" 0 1                                       | Busca las subcategorias de la llave y mustra los  primeros 0 - 1 |
| zrange "Nombrede la llave" 0 1 withscores                    | zrange "celulares" 0 1 withscores                            | Busca las subcategorias de la llave y mustra los  primeros 0 - 1 y muestra el valor asignado |

> Para mas información de los comandos con redis [https://github.com/nrk/predis]

## Contenido del archivo 'Redis-x64-3.2.100.exe' (OPCIONAL)

> Advertencia esta paso es opcional ya que al prender el equipo siempre se ejecutara el redis del servidor

------

![Redis ](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Instalacion_servidor.png)

![Redis ](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Instalacion_servidor2.png)

![Redis ](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Instalacion_servidor3.png)

![Redis ](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Instalacion_servidor4.png)

![Redis ](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Instalacion_servidor5.png)

![Redis ](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Instalacion_servidor6.png)

![Redis ](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/Instalacion_servidor7.png)

## Asignación de una variable del sistema 'redis-cli.exe'

| #    | Pasos                                                        | img                                                          |
| :--- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 1    | Entramos a equipo le damos clic derecho al menú **'Este equipo>propiedades'** | ![Variable Sitema](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/variable_sistema.png) |
| 2    | Una vez dado click no redirige ha la ventana de sistema buscamos en la parte izquierda de menú la opción que dice Configuración avanzada del sistema | ![Variable Sitema](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/variable_sistema2.png) |
| 3    | Nos saldrá otra ventana pero esta vez propiedades del sistema buscamos la opción variables de entorno  que se encuentra el parte inferior de la ventana | ![Variable Sitema](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/variable_sistema3.png) |
| 4    | Entramos en la opción del path y configuramos una variable de acceso | ![Variable Sitema](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/variable_sistema4.png) |
| 5    | Buscamos la ruta donde alojamos la el servidor del redis y el cliente **'C:\Redis'** y de damos aceptar en todas la ventanas que abrimos | ![Variable Sitema](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/variable_sistema5.png) |
| 6    | Para comprobar si la variable esta asignada abrimos el **CMD o símbolo del sistema** y escribimos el comando **'redis-cli'** y se ejecutara el cliente de redis si no se activa tendrás que ejecutar primero el **'redis-server'** en caso que no hayas saltado el paso **Contenido del archivo 'Redis-x64-3.2.100.exe' (OPCIONAL)** o reiniciar el equipo | ![Variable Sitema](https://github.com/MiguelAngelPapu/Redis_Xampp/blob/master/img/variable_sistema7.png) |

> Para utilizar la consola de redis escribir los comandos **'redis-cli'**  para utilizarlo directamente, pero si en caso que hayas saltado **Contenido del archivo 'Redis-x64-3.2.100.exe' (OPCIONAL)** primero ejecutar el comando **'redis-server'**  desde el **CMD** Windows.
